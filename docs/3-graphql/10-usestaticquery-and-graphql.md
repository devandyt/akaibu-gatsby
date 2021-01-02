---
id: 10-usestaticquery-and-graphql
title: useStaticQuery and GraphQL
sidebar_label: useStaticQuery and GraphQL
---

To start off, import Layout component into examples.js

```js
import React from "react"
import Header from "../examples/Header"
import Layout from "../components/layout"

const examples = () => {
  return (
    <Layout>
      <h1>hello from examples page</h1>
      <Header />
    </Layout>
  )
}

export default examples
```

Delete everything in Header.js. We will create useStaticQuery from scratch.

```js
import React from "react"
import { useStaticQuery, graphql } from "gatsby"

const Header = () => {
  return (
    <div>
      <h1>this is our heading</h1>
    </div>
  )
}

export default Header
```

Create variable getData to store our query.

```js
import React from "react"
import { useStaticQuery, graphql } from "gatsby"

const getData = graphql`
  {
    site {
      siteMetadata {
        person {
          age
          name
        }
      }
      author
      data
      description
      title
    }
  }
`

const Header = () => {
  return (
    <div>
      <h1>this is our heading</h1>
    </div>
  )
}

export default Header
```

Create variable store data from query. Console log data to see we back get an object with site, siteMetadata etc...

```js
import React from "react"
import { useStaticQuery, graphql } from "gatsby"

const getData = graphql`
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
`

const Header = () => {
  const data = useStaticQuery(getData)
  console.log(data)

  return (
    <div>
      <h1>this is our heading</h1>
    </div>
  )
}

export default Header
```

From this point on, it's just javascript to access and render the data. We can destructure data in multiple ways.

Method 1: the long way

```js
const Header = () => {
  const data = useStaticQuery(getData)

  return (
    <div>
      <h1>title: {data.site.siteMetadata.title}</h1>
      <h1>name: {data.site.siteMetadata.person.name}</h1>
    </div>
  )
}
```

Method 2: object destructuring

```js
const Header = () => {
  const {
    site: {
      siteMetadata: {
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
}
```
