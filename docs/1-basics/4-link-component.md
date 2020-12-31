---
id: 4-link-component
title: Link Component
sidebar_label: Link Component
---

## Navigation

- For **external** links, use html `<a>` element.
- For **internal** links, use react `<Link>` component.

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

The `<Link>` component ensures only the changed parts are reloaded when navigating the site. This makes the site super fast and smooth.
