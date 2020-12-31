---
id: 5-navbar
title: Navbar
sidebar_label: Navbar
---

## Setting Up

Hardcoding links on every page is a bad idea. Create a **Navbar** component instead.

Create component _Navbar.js_ inside a new folder _src/components/_.

_components/Navbar.js_

```jsx
import React from "react"
import {Link} from "Gatsby"

const Navbar = () => {
    return (
        <nav>
            <ul>
                <li>
                    <Link to "/">Home</Link>
                </li>
                <li>
                    <Link to "/blog/">Blog</Link>
                </li>
                <li>
                    <Link to "/products">Products</Link>
                </li>
            </ul>
        </nav>
    )
}

export default Navbar
```

We can reuse this **Navbar** component in our pages.

_pages/index.js_

```jsx
import React from "react"
import { Link } from "gatsby"
import Navbar from "../components/Navbar"

export default () => (
  <div>
    <Navbar />
    Hello world!
    <div>
      <Link to="/blog/">blog page</Link>
    </div>
    <a href="https://www.gatsbyjs.org">gatsby docs</a>
  </div>
)
```

## Challenge

Add the new **Navbar** component to the blog and products pages.

_blog.js_

```jsx
import React from "react"
import Navbar from "../components/Navbar"

export const blog = () => {
  return (
    <div>
      <Navbar />
      <h1>Our blog page</h1>
    </div>
  )
}

export default blog
```

_products.js_

```jsx
import React, { Component } from "react"

export default class products extends Components {
  render() {
    return (
      <div>
        <Navbar />
        <h1>Our products page</h1>
      </div>
    )
  }
}
```
