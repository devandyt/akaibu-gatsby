---
id: 4-naming-issue
title: Naming Issue
sidebar_label: Naming Issue
---

## The Problem

While global styles are useful, as your project gets bigger it will be annoying to keep coming up with unique class names.

_components/layout.css_

```css
@import url("https://fonts.googleapis.com/css?family=Roboto&display=swap");
body {
  font-family: "Roboto", sans-serif;
}
h1 {
  color: blue;
  text-transform: capitalize;
}
.blog-text {
  color: red;
  line-height: 0.5;
}
.products-text {
  color: green;
  line-height: 3;
}
```

_blog.js_

```jsx
import React from "react"
import Layout from "../components/layout"

export const blog = () => {
  return (
    <Layout>
      <div>
        <h1>Our blog page</h1>
        <p className="blog-text">some text</p>
      </div>
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
        <div>
          <h1>Our products page</h1>
          <p className="products-text">some text</p>
        </div>
      </Layout>
    )
  }
}
```

## The Solution

Use CSS Modules.
