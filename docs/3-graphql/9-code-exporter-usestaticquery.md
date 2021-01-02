---
id: 9-code-exporter-usestaticquery
title: Code Exporter useStaticQuery
sidebar_label: Code Explorter useStaticQuery
---

Toggle open Code Exported in GraphiQL and consider the following query result. Make use StaticQuery hook is selected.

Copy the query result into a new file _examples/Header.js_.

```js
import React from "react"
import { useStaticQuery, graphql } from "gatsby"

const ComponentName = () => {
  const data = useStaticQuery(graphql`
    {
      site {
        siteMetadata {
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
  `)
  return <pre>{JSON.stringify(data, null, 4)}</pre>
}

export default ComponentName
```

In examples.js, import Header.js

```js
import React from "react"
import Header from "../examples/Header"

const examples = () => {
  return (
    <div>
      <h1>hello from examples page</h1>
      <Header />
    </div>
  )
}
```

What we are just rendering is the query result we see in the sandbox `<pre>{JSON.stringify(data, null, 4)}</pre>`.

```js
import React from "react"
import { useStaticQuery, graphql } from "gatsby"

const ComponentName = () => {
  const data = useStaticQuery(graphql`
    {
      site {
        siteMetadata {
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
  `)
  return <pre>{JSON.stringify(data, null, 4)}</pre>
}
```

To grab and display our data, we need to drill down the data object. For example, `<h1>{data.site.siteMetadata.person.name}</h1>`.

```js
import React from "react"
import { useStaticQuery, graphql } from "gatsby"

const ComponentName = () => {
  const data = useStaticQuery(graphql`
    {
      site {
        siteMetadata {
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
  `)
  return (
    <div>
      <h2>{data.site.siteMetadata.person.name}</h2>
      <h2>{data.site.siteMetadata.person.age}</h2>
    </div>
  )
}
```
