---
id: 11-field-alias
title: Field Alias
sidebar_label: Field Alias
---

For long field names, there is a way to make them shorter by using alias.

```graphql
query MyQuery {
  site {
    info: siteMetadata {
      person {
        age
        name
      }
      author
      data
      description
      title
    }
  }
}
```

In the response, you will see now we get info instead of siteMetadata.

```js
{
    "data": {
        "site": {
            "info": {
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

Try it out in examples.js. Remember to refer to the alias when accessing the data using both the long way and destructuring.

```js
import React from "react"
import { useStaticQuery, graphql } from "gatsby"

const getData = graphql`
  {
    site {
      info: siteMetadata {
        person {
          age
          name
        }
        author
        data
        description
        title
      }
    }
  }
`

const Header = () => {
  const {
    site: {
      info: {
        title,
        person: { name },
      },
    },
  } = useStaticQuery(getData)

  return (
    <div>
      <h1>title: {title}</h1>
      <h1>name: {name}</h1>
    </div>
  )

export default Header
```
