---
title: Dataset Advanced Configuration
keywords: documentation
last_updated: October 15th, 2020
tags: [getting-started]
sidebar: mydoc_sidebar
layout: doc
---

Welcome in the Advanced Configuration. This section of the documentation is specifically designed for proficient and expert users.


## Sorting rulesa

In this example, we provide the instructions for sorting the results of the query
```javascript

{
   "when" : "!query.isSorted()",
   "order" : "PRICE" 
},
{
   "when" : "!query.isSortedByMeasure()",
   "order" : "PRICE ASC" 
},
{
   "when" : "!query.isSortedByDimension()",
   "order" : "PLACE DESC" 
},

{
   "when" : "!query.isSortedBy('place')",
   "order" : "PRICE DESC, PLACE ASC" 
}

```
## Filters

Filters are powerful tools that can be used to restrict access to some data. For example if you are a manager in a company and would like one of your employees to access just the data that is related to himself, you could achieve that by defining a simple filter as in the picture:

<p align="center">
  <img src="https://github.com/Edoardoba/test/blob/main/media/filters-example.PNG" width="650" />
</p>

For example in the above use case we are specifying that if the user login email is *employee@yourcompany.com* then just show him the records where *name=John* and *surname=Doe*. This obviously is a rather simple example of the definition of a filter, more complex ones can be build in order to guarantee the proper flexibility to your dataset. If you would like to have a deeper overview of filters you can watch (this resource)[filters]

**Example with user defined security:**

This is an example of an advanced filter that could be applied to the dataset.
```javascript

[
    {
        "when": "(user.username == "myuser@mymail.com2") && (user.details.user_type != null)",
        "then": "CASE WHEN '{{user.details.user_type}}' <> 'DIR' THEN AGENZIA IN ( SELECT agenzia_cod FROM VIEW_USERS WHERE user_id = '{{user.details.custom_id}}') WHEN '{{user.details.user_type}}' = 'DIR' THEN 1=1 ELSE 1 <> 1 END"
    }
]

```

This filters only returns the cases that satisfy the conditions specified in the where clause.
