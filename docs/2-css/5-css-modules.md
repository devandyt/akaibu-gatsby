---
id: 5-css-modules
title: CSS Modules
sidebar_label: CSS Modules
---

With CSS Modules, you can use a common class name and use it on different pages as unique classes. They scope CSS locally to that file.

File name now ends with modules.css.

For blog.js we make blog.module.css

```css
.page {
  background: green;
}
.page h1 {
  color: blue;
}
.text {
  text-transform: capitalize;
}
```

_blog.js_

```jsx
import React from "react"
import Layout from "../components/layout"
import styles from "../components/blog.module.css"

export const blog = () => {
  return (
    <Layout>
      <div className={styles.page}>
        <h1>Our blog page</h1>
        <p className={styles.text}>some text</p>
      </div>
    </Layout>
  )
}

export default blog
```

Import products.module.css into products.js

```css
.page {
  background: yellow;
}
.page h1 {
  color: red;
}
.text {
  text-transform: uppercase;
}
```

_products.js_

```jsx
import React, { Component } from "react"
import Layout from "../components/layout"
import styles from "../components/products.module.css"

export default class products extends Components {
  render() {
    return (
      <Layout>
        <div className={styles.page}>
          <h1>Our products page</h1>
          <p className={styles.text}>some text</p>
        </div>
      </Layout>
    )
  }
}
```

The javascript object styles contains the css properties with unqiue suffix, so we can just refer to it without worry of clashing.
