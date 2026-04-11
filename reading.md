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

<div id="primary-filters" class="global-filters" style="text-align: center; margin-bottom: 0.5rem;"></div>

<div id="secondary-filters" class="global-filters" style="text-align: center; margin-bottom: 3rem;"></div>

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

  const randomizedReadings = shuffleArray([...allReadings]);
  
  let currentIndex = 0;
  const itemsPerLoad = 5;
  const container = document.getElementById('random-reading-list');
  const loadMoreBtn = document.getElementById('load-more-btn');
  
  // Categorized Filter Arrays
  const topCategories = ["Privacy", "Machine Learning", "Economics", "Philosophy", "History", "Mathematics"];
  const extraTypes = ["Book", "Article"];
  const extraEras = ["1820s", "1870s", "1920s", "2010s", "2020s"];
  
  // State variables for multidimensional filtering
  let activeTopics = [];
  let activeTypes = [];
  let activeEras = [];

  const primaryContainer = document.getElementById('primary-filters');
  const secondaryContainer = document.getElementById('secondary-filters');

  function renderFilters() {
    // Render Primary Topics
    primaryContainer.innerHTML = topCategories.map(tag => {
      const activeClass = activeTopics.includes(tag) ? 'active-tag' : '';
      return `<button class="tag filter-btn ${activeClass}" onclick="toggleFilter('${tag}', 'topic')">${tag}</button>`;
    }).join(' ');

    // Render Secondary Types and Eras
    let extraHtml = extraTypes.map(tag => {
      const activeClass = activeTypes.includes(tag) ? 'active-tag' : '';
      return `<button class="tag filter-btn secondary-tag ${activeClass}" onclick="toggleFilter('${tag}', 'type')">${tag}</button>`;
    }).join(' ');
    
    extraHtml += `<span style="margin: 0 1rem; color: #ccc;">|</span>`; // Visual separator
    
    extraHtml += extraEras.map(tag => {
      const activeClass = activeEras.includes(tag) ? 'active-tag' : '';
      return `<button class="tag filter-btn secondary-tag ${activeClass}" onclick="toggleFilter('${tag}', 'era')">${tag}</button>`;
    }).join(' ');

    secondaryContainer.innerHTML = extraHtml;
  }

  window.toggleFilter = function(value, category) {
    if (category === 'topic') {
      if (activeTopics.includes(value)) activeTopics = activeTopics.filter(t => t !== value);
      else activeTopics.push(value);
    } else if (category === 'type') {
      if (activeTypes.includes(value)) activeTypes = activeTypes.filter(t => t !== value);
      else activeTypes.push(value);
    } else if (category === 'era') {
      if (activeEras.includes(value)) activeEras = activeEras.filter(t => t !== value);
      else activeEras.push(value);
    }
    
    container.innerHTML = '';
    currentIndex = 0;
    
    renderFilters(); 
    renderItems();   
  };

  function renderItems() {
    let arrayToRender = randomizedReadings.filter(item => {
      // Must match ALL active topics (AND logic)
      const matchTopic = activeTopics.length === 0 || activeTopics.every(t => item.tags && item.tags.includes(t));
      // Must match ANY active type (OR logic within types)
      const matchType = activeTypes.length === 0 || activeTypes.includes(item.type);
      // Must match ANY active era (OR logic within eras)
      const matchEra = activeEras.length === 0 || activeEras.includes(item.era);
      
      return matchTopic && matchType && matchEra;
    });

    if (arrayToRender.length === 0) {
      container.innerHTML = `
        <div class="empty-state fade-in" style="text-align: center; padding: 4rem 1rem;">
          <p style="color: #666; font-size: 1.1rem; margin-bottom: 1.5rem;">No readings found for that specific combination of filters.</p>
          <button onclick="clearFilters()" class="load-more-btn">Clear Filters</button>
        </div>
      `;
      if (loadMoreBtn) loadMoreBtn.style.display = 'none';
      return; 
    }

    const batch = arrayToRender.slice(currentIndex, currentIndex + itemsPerLoad);
    let htmlContent = '';

    batch.forEach(item => {
      let tagsHtml = '';
      if (item.tags && item.tags.length > 0) {
        const tagSpans = item.tags.map(tag => {
          const activeClass = activeTopics.includes(tag) ? 'active-tag' : '';
          return `<span class="tag ${activeClass}" onclick="toggleFilter('${tag}', 'topic')">${tag}</span>`;
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
          htmlContent += `<p class="meta"><strong>${item.author}</strong> &mdash;`; 
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
          <div class="reading-item-metadata" style="display: flex; justify-content: space-between; align-items: center; margin-top: 1rem;">
            ${tagsHtml}
            <span style="font-size: 0.85rem; color: #888;">
              ${item.type ? item.type : ''} ${item.type && item.era ? '•' : ''} ${item.era ? item.era : ''}
            </span>
          </div>
        </article>
      `;
    });

    container.insertAdjacentHTML('beforeend', htmlContent);
    currentIndex += itemsPerLoad;

    if (currentIndex >= arrayToRender.length) {
      if(loadMoreBtn) loadMoreBtn.style.display = 'none';
    } else {
      if(loadMoreBtn) loadMoreBtn.style.display = 'inline-block';
    }
  }

  window.clearFilters = function() {
    activeTopics = [];
    activeTypes = [];
    activeEras = [];
    container.innerHTML = '';
    currentIndex = 0;
    
    renderFilters();
    renderItems();
  };

  renderFilters();
  renderItems();

  if (loadMoreBtn) {
    loadMoreBtn.addEventListener('click', renderItems);
  }
</script>
