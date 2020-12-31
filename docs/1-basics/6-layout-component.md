---
id: 6-layout-component
title: Layout Component
sidebar_label: Layout Component
---

## Layout Component

Adding the same components to every page does not scale up very well. Common components can first be grouped together as one layout component. Unique content from each page can be passed as children prop to the layout component.

_components/layout.js_

```jsx
import React from "react"
import Navbar from "./Navbar"
import Footer from "./Footer"

const layout = ({ children }) => {
  return (
    <>
      <Navbar />
      <main>{children}</main>
      <Footer />
    </>
  )
}

export default layout
```

:::note
We can use react fragent `<>` instead of `<div>` to as the parent element to avoid placing too many `<div>` elements.
:::

The layout component can then be used as the parent element on the desired pages.

_index.js_

```jsx
import React from "react"
import Layout from "../components/layout"

export default () => (
  <Layout>
    <h1>Hello world!</h1>
  </Layout>
)
```

## Challange

Use the new layout component in blog and products pages.

_blog.js_

```jsx
import React from "react"
import Layout from "../components/layout"

export const blog = () => {
  return (
    <Layout>
      <h1>Our blog page</h1>
    </Layout>
  )
}

export default blog
```

_products.js_

```jsx
import React, { Component } from "react"
import Layout from "../components/layout"

export default class products extends Components {
  render() {
    return (
      <Layout>
        <h1>Our products page</h1>
      </Layout>
    )
  }
}
```
