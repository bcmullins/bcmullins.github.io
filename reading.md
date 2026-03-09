---
layout: default
title: "Reading Recommendations"
permalink: /reading/
mathjax: true
---

<div class="reading-header">
  <h1>Reading Recommendations</h1>
  <p>A curated selection of books and articles for curious readers covering machine learning, economics, history, philosophy, and more.</p>
</div>

<div id="random-reading-list" class="reading-list"></div>

<div class="button-container" style="text-align: center; margin-top: 2rem; margin-bottom: 4rem;">
  <button id="load-more-btn" class="load-more-btn">Load 5 More</button>
</div>

<script>
  const allReadings = {{ site.data.reading | jsonify }};

  function shuffleArray(array) {
    for (let i = array.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [array[i], array[j]] = [array[j], array[i]];
    }
    return array;
  }

  // Shuffle the master list once when the page loads
  const randomizedReadings = shuffleArray([...allReadings]);
  
  // State variables
  let currentIndex = 0;
  const itemsPerLoad = 5;
  const container = document.getElementById('random-reading-list');
  const loadMoreBtn = document.getElementById('load-more-btn');
  
  // Track active tags in an array
  let activeTags = [];

  function renderItems() {
    let arrayToRender = randomizedReadings;
    
    // "AND" LOGIC: Show item ONLY if it contains EVERY active tag
    if (activeTags.length > 0) {
      arrayToRender = randomizedReadings.filter(item => 
        item.tags && activeTags.every(tag => item.tags.includes(tag))
      );
    }

    // EMPTY STATE: If the filter combination yields zero results
    if (arrayToRender.length === 0) {
      container.innerHTML = `
        <div class="empty-state fade-in" style="text-align: center; padding: 4rem 1rem;">
          <p style="color: #666; font-size: 1.1rem; margin-bottom: 1.5rem;">No readings found for that specific combination of tags.</p>
          <button onclick="clearFilters()" class="load-more-btn">Clear Filters</button>
        </div>
      `;
      if (loadMoreBtn) loadMoreBtn.style.display = 'none';
      return; // Exit the function early so we don't try to render an empty batch
    }

    // Grab the next batch
    const batch = arrayToRender.slice(currentIndex, currentIndex + itemsPerLoad);
    let htmlContent = '';

    batch.forEach(item => {
      let tagsHtml = '';
      if (item.tags && item.tags.length > 0) {
        const tagSpans = item.tags.map(tag => {
          const activeClass = activeTags.includes(tag) ? 'active-tag' : '';
          return `<span class="tag ${activeClass}" onclick="toggleTag('${tag}')">${tag}</span>`;
        }).join('');
        tagsHtml = `<div class="tags">${tagSpans}</div>`;
      }

      htmlContent += `
        <article class="reading-item fade-in">
          <header>`;

      if (item.url) {
          htmlContent += `<h2><a href="${item.url}" target="_blank" rel="noopener">${item.title}</a></h2>`;
      } else {
          htmlContent += `<h2>${item.title}</h2>`;
      }
      
      if (item.author) {
          htmlContent += `
            <p class="meta"><strong>${item.author}</strong> &mdash;`; 
      }
      
      if (item.publication) {
          htmlContent += ` ${item.publication} &mdash;`;
      }

      htmlContent += ` ${item.year}</p>
          </header>`;

      if (item.context) {
          htmlContent += `
          <div class="context">
            <p>Discussed in <a href="{{ site.url }}/${item.contextlink}">${item.context}</a></p>
          </div>`;
      }
          
      if (item.quote) {
          htmlContent += `
          <blockquote class="pull-quote">
              <p>"${item.quote}"</p>
          </blockquote>`;
      }

      if (item.commentary) {
          htmlContent += `
          <div class="commentary">
              <p>${item.commentary}</p>
          </div>`;
      }
      
      htmlContent += `
          ${tagsHtml}
        </article>
      `;
    });

    // Append the new items
    container.insertAdjacentHTML('beforeend', htmlContent);
    currentIndex += itemsPerLoad;

    // Show or hide the Load More button based on the remaining items
    if (currentIndex >= arrayToRender.length) {
      if(loadMoreBtn) loadMoreBtn.style.display = 'none';
    } else {
      if(loadMoreBtn) loadMoreBtn.style.display = 'inline-block';
    }
  }

  // Toggle function to add/remove tags from the array
  window.toggleTag = function(tag) {
    if (activeTags.includes(tag)) {
      activeTags = activeTags.filter(t => t !== tag);
    } else {
      activeTags.push(tag);
    }
    
    // Clear the current list and reset the index
    container.innerHTML = '';
    currentIndex = 0;
    
    // Re-render
    renderItems();
  };

  // Helper function to quickly clear all filters from the empty state
  window.clearFilters = function() {
    activeTags = [];
    container.innerHTML = '';
    currentIndex = 0;
    renderItems();
  };

  // Run the function once to load the initial 5 items
  renderItems();

  if (loadMoreBtn) {
    loadMoreBtn.addEventListener('click', renderItems);
  }
</script>