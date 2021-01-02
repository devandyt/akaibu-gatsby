---
id: 13-staticquery-component
title: staticQuery Component
sidebar_label: staticQuery Component
---

Before React hooks, data is retrieved using the staticQuery component.

Create component HeaderStatic.js. Notice in this case we are important the whole React component, not a react hook. We then use the component and added query prop to pass in our query. Whatever is returned in the data function that is passed into render prop will be rendered.

_examples/HeaderStatic.js_

```js
import React from "react"
import { staticQuery, graphql } from "gatsby"

const ComponentName = () => (
  <StaticQuery
    query={graphql`
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
    `}
    render={(data) => <pre>{JSON.stringify(data, null, 4)}</pre>}
  ></StaticQuery>
)
```

In examples.js, import HeaderStatic.

```js
import React from "react"
import Header from "../examples/Header"
import HeaderStatic from "../examples/HeaderStatic"
import Layout from "../components/layout"

const examples = () => {
  return (
    <Layout>
      <h1>hello from examples page</h1>
      <Header />
      <HeaderStatic />
    </Layout>
  )
}

export default examples
```

To render the description we can change what the data function returns.

```js
import React from "react"
import { staticQuery, graphql } from "gatsby"

const ComponentName = () => (
  <StaticQuery
    query={graphql`
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
    `}
    render={(data) => <h4>{data.site.info.description}</h4>}
  ></StaticQuery>
)
```

This method of using StaticQuery is not really used anymore.
