---
id: 2-inline-css
title: Inline CSS
sidebar_label: Inline CSS
---

## Inline-Styles

Most basic option where you write your styles in JSX elements using javascript. This option is only useful when adding styles to a particular element.

_index.js_

```jsx
import React from "react"
import Layout from "../components/layout"

export default () => (
  <Layout>
    <h1 style={{ color: "red", textTransform: "uppercase" }}>Hello world!</h1>
  </Layout>
)
```

:::note
Some of the css property names are different because javascript does not support hythens. For example, CSS class becomes className.
:::
