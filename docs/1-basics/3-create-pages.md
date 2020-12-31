---
id: 3-create-pages
title: Create Pages
sidebar_label: Create Pages
---

## Simple Page Setup

Creating pages is easy, just create files in _pages/_. By convention, the root page is _index.js_.

> _index.js_ for **http://localhost:8000/**  
> _About.js_ for **http://localhost:8000/about**  
> _Contact.js_ for **http://localhost:8000/contact**

## Familiarity

In _pages/index.js_, we see a page is basically a **react component** with `export default`.

_index.js_

```jsx
import React from "react"

export default () => <div>Hello world!</div>
```

Whatever we return from our component will be displayed.

:::note
We can use either a **class-based** component or a **functional** component. However, with **react hooks**, you will most likely use the latter.
:::

## Create Pages

Inside **pages/**., create _blog.js_ and _products_.js for the **blog** and **products** pages, respectively.

_blog.js_

```jsx
import React from "react"

export const blog = () => {
  return (
    <div>
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
        <h1>Our products page</h1>
      </div>
    )
  }
}
```

Navigate to **https://localhost:8000/blog** and **https://localhost:8000/products** to see the pages.

## 404 Page

Create _404.js_ for all **error** pages.

_404.js_

```jsx
import React from "react"

export default function error() {
  return (
    <div>
      <h1>Our error page</h1>
    </div>
  )
}
```

The error page only displays when application is **deployed** in production.

:::note
Use the following shortcuts to quickly create component snippets:  
`rafce` - unnamed **arrow** functional component  
`rfc` - named **functional** component  
`rcc` - named **class-based** component
:::
