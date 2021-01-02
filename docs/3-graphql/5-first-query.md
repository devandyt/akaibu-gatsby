---
id: 5-first-query
title: First Query
sidebar_label: First Query
---

With our siteMetadata set up, we can now query it.

Open GraphiQL at http://localhost:8000/\_\_graphql

If we try to query our site we get an error because there are sub-fields.

```graphql
{
  site
}
```

Likewise, because siteMetadata also have sub-fields, we are required to dig deeper.

```graphql
{
  site {
    siteMetadata
  }
}
```

Finally, we have our deepest set of fields and we have to query at least one.

```graphql
{
  site {
    siteMetadata {
      title
    }
  }
}
```

The response we can back is a data object. Inside the data object, we get back what looks like our query, but we now also get back the property values.

```js
{
    "data": {
        "site": {
            "siteMetadata": {
                "title": "Gatsby Tutorial"
            }
        }
    }
}
```

If we want all the properties we can add the remaining ones, however, person has sub-fields, so need to specify.

```graphql
{
  site {
    siteMetadata {
      title
      description
      author
      data
      person {
        name
        age
      }
    }
  }
}
```

Resulting response.

```js
{
    "data": {
        "site": {
            "siteMetadata": {
                "title:": "Gatsby Tutorial",
                "description": "some text",
                "author": "@johndoe",
                "data": [
                    "item 1",
                    "item 2"
                ],
                "person": {
                     "name": "peter",
                     "age": "32"
                }
            }
        }
    }
}
```
