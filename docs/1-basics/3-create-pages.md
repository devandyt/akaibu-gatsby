---
id: 3-create-pages
title: Create Pages
sidebar_label: Create Pages
---

## Simple Page Setup

Creating pages in Gatsby is easy, just create files in /pages folder. By convention, the root page is _index.js_.

> _index.js_ for **home** page  
> _About.js_ for **about** page  
> _Contact.js_ for **contact** page

:::note
These file names show up in the URL, e.g. http://localhost:8000/about
:::

## Familiarity

Open _pages/index.js_, all we need to do to create a page is to create a react component and then `export default`.

_index.js_

```jsx
import React from "react"

export default () => <div>Hello world!</div>
```

Whatever we return from our component will be displayed in our page.

:::note
This could be a class based component or a functional component. With arrival of react hooks, we use mostly functional components for both component and page component in Gatsby.
:::

## Practice 1

Inside /pages folder, create blog.js and products.js for the blog and products pages, respectively.

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

Navigate to https://localhost:8000/blog and https://localhost:8000/products to see the pages.

## 404 Page

Simply create a file _404.js_ to represent all error pages.

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

The error page can only be seen when application is deployed.

:::note
Use the following shortcuts to quickly create component snippets:  
`rafce` - unnamed arrow functional component  
`rfc` - named functional component  
`rcc` - named class-based component
:::
