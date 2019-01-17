---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - http

toc_footers:

includes:
  - errors

search: true
---

# Introduction

Welcome to the Rover API! You can use our API to access Rover API endpoints, which can get information on various data in our database.

We have language bindings in JavaScript! You can view code examples in the dark area to the right.

# Posts API

## Get all posts

> Response JSON structure:

```json
[
  {
    "id": 1,
    "title": "Happy 2019",
    "featured_image": "https://rover.jetek.com.au/images/1.png",
    "content": "<p>We casually associate traveling to escaping, and during these last years of traveling a lot I had trouble acknowledging how much of it was actually about running away</p>",
    "excerpt": "To put it kindly, 2018 was kind of mixed bag for me......"
    "author": {
      "id": 1,
      "name": "Isabella Brown",
      "avatar": "https://rover.jetek.com.au/images/guides/1.png"
    }
    "city": {
      "id": 1,
      "name": "Sydney",
      "country": "Australia"
    }
    "category": {
      "id": 1,
      "name": "Food"
    }
    "tags": [
       {
         "id": 1, 
         "name": "Food"
       },
       {
         "id": 2, 
         "name": "Australia"
       }
    ]
    "publish_date": 'JANUARY 6, 2019'
    "publish_date_differ": 'Two weeks ago'
    "is_top": 1
    "is_front": 1
    "view_count": 98780
  },
  {
    "id": 2,
    "title": "16 days in Beijing, China",
    "featured_image": "https://rover.jetek.com.au/images/2.png",
    "content": "<p>We casually associate traveling to escaping, and during these last years of traveling a lot I had trouble acknowledging how much of it was actually about running away</p>",
    "excerpt": "The truth is, Beijing is a trip in itself......"
    "author": {
      "id": 2,
      "name": "Emily Wilson",
      "avatar": "https://rover.jetek.com.au/images/guides/2.png"
    }
    "city": {
      "id": 6,
      "name": "Beijing",
      "country": "China"
    }
    "category": {
      "id": 1,
      "name": "Culture"
    }
    "tags": [
       {
         "id": 1, 
         "name": "Culture"
       },
       {
         "id": 2, 
         "name": "China"
       }
    ]
    "publish_date": 'JANUARY 12, 2019'
    "publish_date_differ": 'Three days ago'
    "is_top": 1
    "is_front": 1
    "view_count": 999999
  }
]
```

This endpoint retrieves all posts.

### HTTP Request

`GET https://rover.jetek.com.au/api/v1/posts`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
city | int | If set to 0, the result will also include all cities.
limit | int | result count.

<aside class="notice">
Remember — limit is required!
</aside>

## Get top posts

> Response JSON structure:

```json
[
  {
    "id": 1,
    "title": "Happy 2019",
    "featured_image": "https://rover.jetek.com.au/images/1.png",
    "content": "<p>We casually associate traveling to escaping, and during these last years of traveling a lot I had trouble acknowledging how much of it was actually about running away</p>",
    "excerpt": "To put it kindly, 2018 was kind of mixed bag for me......"
    "author": {
      "id": 1,
      "name": "Isabella Brown",
      "avatar": "https://rover.jetek.com.au/images/guides/1.png"
    }
    "city": {
      "id": 1,
      "name": "Sydney",
      "country": "Australia"
    }
    "category": {
      "id": 1,
      "name": "Food"
    }
    "tags": [
       {
         "id": 1, 
         "name": "Food"
       },
       {
         "id": 2, 
         "name": "Australia"
       }
    ]
    "publish_date": 'JANUARY 6, 2019'
    "publish_date_differ": 'Two weeks ago'
    "is_top": 1
    "is_front": 1
    "view_count": 98780
  },
  {
    "id": 2,
    "title": "16 days in Beijing, China",
    "featured_image": "https://rover.jetek.com.au/images/2.png",
    "content": "<p>We casually associate traveling to escaping, and during these last years of traveling a lot I had trouble acknowledging how much of it was actually about running away</p>",
    "excerpt": "The truth is, Beijing is a trip in itself......"
    "author": {
      "id": 2,
      "name": "Emily Wilson",
      "avatar": "https://rover.jetek.com.au/images/guides/2.png"
    }
    "city": {
      "id": 6,
      "name": "Beijing",
      "country": "China"
    }
    "category": {
      "id": 1,
      "name": "Culture"
    }
    "tags": [
       {
         "id": 1, 
         "name": "Culture"
       },
       {
         "id": 2, 
         "name": "China"
       }
    ]
    "publish_date": 'JANUARY 12, 2019'
    "publish_date_differ": 'Three days ago'
    "is_top": 1
    "is_front": 1
    "view_count": 999999
  }
]
```

This endpoint retrieves top posts.

### HTTP Request

`GET https://rover.jetek.com.au/api/v1/posts`

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
city | int | If set to 0, the result will also include all cities.
top | int | result count.

<aside class="notice">
Remember — top is required!
Empty dataset will return if no data available.
</aside>

## Get a specific post

> Response JSON structure:

```json
{
    "id": 2,
    "title": "16 days in Beijing, China",
    "featured_image": "https://rover.jetek.com.au/images/2.png",
    "content": "<p>We casually associate traveling to escaping, and during these last years of traveling a lot I had trouble acknowledging how much of it was actually about running away</p>",
    "excerpt": "The truth is, Beijing is a trip in itself......"
    "author": {
      "id": 2,
      "name": "Emily Wilson",
      "avatar": "https://rover.jetek.com.au/images/guides/2.png"
    }
    "city": {
      "id": 6,
      "name": "Beijing",
      "country": "China"
    }
    "category": {
      "id": 1,
      "name": "Culture"
    }
    "tags": [
       {
         "id": 1, 
         "name": "Culture"
       },
       {
         "id": 2, 
         "name": "China"
       }
    ]
    "publish_date": 'JANUARY 12, 2019'
    "publish_date_differ": 'Three days ago'
    "is_top": 1
    "is_front": 1
    "view_count": 999999
}
```

This endpoint retrieves a specific post.

### HTTP Request

`GET https://rover.jetek.com.au/api/v1/posts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the post to retrieve

