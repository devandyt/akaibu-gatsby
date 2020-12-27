---
id: 4-link-component
title: Link Component
sidebar_label: Link Component
---

## Navigation

We could always use an html `<a>` element, but this method reloads the whole page when loading a new page.

`pages/index.js`

```jsx
import React from "react"

export default () => (
  <div>
    Hello world!
    <div>
      <a href="/blog/">blog page</a>
    </div>
    <a href="https://www.gatsbyjs.org">gatsby docs</a>
  </div>
)
```

That is why we should use the `<Link>` element, which only reloads the changes. However, external links will still use the html `<a>` method.

`pages/index.js`

```jsx
import React from "react"
import { Link } from "gatsby"

export default () => (
  <div>
    Hello world!
    <div>
      <Link to="/blog/">blog page</Link>
    </div>
    <a href="https://www.gatsbyjs.org">gatsby docs</a>
  </div>
)
```
