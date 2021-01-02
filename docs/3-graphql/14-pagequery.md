---
id: 14-pagequery
title: pageQuery
sidebar_label: pageQuery
---

Although you can use StaticQuery for page components, you cannot setup PageQuery for components. The benefit of PageQuery is you can pass in varaiables. It also allows you to setup pages automatically or dynamically.

In examples.js, create a PageQuery.

```js
import React from "react"
import Header from "../examples/Header"
import HeaderStatic from "../examples/HeaderStatic"
import Layout from "../components/layout"
import { graphql } from "gatsby"

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

By default, Gatsby provides a bunch of props to the page component. Console logging displays the punch of properties.

```js
import React from "react"
import Header from "../examples/Header"
import HeaderStatic from "../examples/HeaderStatic"
import Layout from "../components/layout"
import { graphql } from "gatsby"

const examples = (props) => {
  console.log(props)
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

The property we are looking for is data, but to get it we need to setup a graphql query first and must export that variable.

```js
import React from "react"
import Header from "../examples/Header"
import HeaderStatic from "../examples/HeaderStatic"
import Layout from "../components/layout"
import { graphql } from "gatsby"

const examples = (props) => {
  console.log(props)
  return (
    <Layout>
      <h1>hello from examples page</h1>
      <Header />
      <HeaderStatic />
    </Layout>
  )
}

export const data = graphql`
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
export default examples
```

Note we have the data property. From this point on, how we access and render the data is exactly the same as before.

```js
import React from "react"
import Header from "../examples/Header"
import HeaderStatic from "../examples/HeaderStatic"
import Layout from "../components/layout"
import { graphql } from "gatsby"

const examples = ({ data }) => {
  const {
    site: {
      info: { author },
    },
  } = data
  return (
    <Layout>
      <h1>hello from examples page</h1>
      <Header />
      <HeaderStatic />
      <h5>author: {author}</h5>
    </Layout>
  )
}

export const data = graphql`
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
`
export default examples
```
