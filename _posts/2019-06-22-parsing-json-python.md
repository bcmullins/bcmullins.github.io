---
layout: post
title: Parsing Nested JSON Records in Python
categories: Helpful
mathjax: true
---

JSON is the typical format used by web services for message passing that's also relatively human-readable. Despite being more human-readable than most alternatives, JSON objects can be quite complex. For analyzing complex JSON data in Python, there aren't clear, general methods for extracting information (see [here](https://realpython.com/python-json/) for a tutorial of working with JSON data in Python). This post provides a solution if one knows the path through the nested JSON to the desired information.

## Motivating Example
Suppose you have the following JSON record:
{% highlight JSON %}
{
  "employees":
    [
      {
        "name": "Alice",
        "role": "dev",
        "nbr": 1
      },
      {
        "name": "Bob",
        "role": "dev",
        "nbr": 2
      }
    ],
  "firm":
    {
      "name": "Charlie's Waffle Emporium",
      "location": "CA"
    }
}
{% endhighlight %}

This record has two keys at the top level: _employees_ and _firm_. The value for the _employees_ key is a list of two objects of the same schema; each object has the keys _name_, _role_, and _nbr_. The value for the _firm_ key is an object with the keys _name_ and _location_.

Suppose you want to extract the names of the employees. This record will give problems for approaches that just search through key names, since the name of the firm will be returned as well.

## Solution
Calling the *extract_element_from_json* function on the above record delivers the desired result:
{% highlight Python %}
data = {"employees":[{"name": "Alice", "role": "dev", "nbr": 1}, {"name": "Bob", "role": "dev", "nbr": 2}], "firm":{"name": "Charlie's Waffle Emporium", "location": "CA"}}

extract_element_from_json(data, ["employees", "name"])
>> ['Alice', 'Bob']
{% endhighlight %}


## Under the Hood
This function nests into the record(s) in _obj_ according to the keys specified in _path_ to retrieve the desired information. When a list is encountered as the value of a key in _path_, this function splits and continues nesting on each element of the encountered list in a depth-first manner. This is how both 'Alice' and 'Bob' are returned; since the value of _employees_ is a list, the nesting is split on both of its elements and each of the values for _name_ are appended to the output list.

If _obj_ is a single dictionary/JSON record, then this function returns a list containing the desired information, and if _obj_ is a list of dictionaries/JSON records, then this function returns a list of lists containing the desired information.

If any element of _path_ is missing from the corresponding level of the nested dictionary/JSON, then this function returns a _None_ .

Below is the full function (inspired/motivated from what's discussed [here](https://hackersandslackers.com/extract-data-from-complex-json-python/)):

{% highlight Python %}
def extract_element_from_json(obj, path):
    '''
    Extracts an element from a nested dictionary or
    a list of nested dictionaries along a specified path.
    If the input is a dictionary, a list is returned.
    If the input is a list of dictionary, a list of lists is returned.
    obj - list or dict - input dictionary or list of dictionaries
    path - list - list of strings that form the path to the desired element
    '''
    def extract(obj, path, ind, arr):
        '''
            Extracts an element from a nested dictionary
            along a specified path and returns a list.
            obj - dict - input dictionary
            path - list - list of strings that form the JSON path
            ind - int - starting index
            arr - list - output list
        '''
        key = path[ind]
        if ind + 1 < len(path):
            if isinstance(obj, dict):
                if key in obj.keys():
                    extract(obj.get(key), path, ind + 1, arr)
                else:
                    arr.append(None)
            elif isinstance(obj, list):
                if not obj:
                    arr.append(None)
                else:
                    for item in obj:
                        extract(item, path, ind, arr)
            else:
                arr.append(None)
        if ind + 1 == len(path):
            if isinstance(obj, list):
                if not obj:
                    arr.append(None)
                else:
                    for item in obj:
                        arr.append(item.get(key, None))
            elif isinstance(obj, dict):
                arr.append(obj.get(key, None))
            else:
                arr.append(None)
        return arr
    if isinstance(obj, dict):
        return extract(obj, path, 0, [])
    elif isinstance(obj, list):
        outer_arr = []
        for item in obj:
            outer_arr.append(extract(item, path, 0, []))
        return outer_arr
{% endhighlight %}

## Update
This post is featured in Issue #374 of [PyCoder's Weekly](https://pycoders.com/issues/374). 
