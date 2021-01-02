---
id: 6-styled-components
title: Styled Components
sidebar_label: Styled Components
---

Similar to CSS modules, styled components scopes CSS to a particular component, thus avoiding name collisions.

1. Styled components require plugin install.
   https://www.gatsbyjs.cn/packages/gatsby-plugin-styled-components/

2. Setup plugin in gatsby-config.js

```js
module.export = {
  plugins: [`gatsby-plugin-styled-components`],
}
```

3. Restart for Gatsby dev server.

Once installed, we can start by creating a component.
_components_/button.js

```js
import styled from "styled-components"

export const ExampleButton = styled.button`
  background: green;
  color: orange;
  font-size: 2rem;
`
```

We can now use this component with these specific styles.

_index.js_

```jsx
import React from "react"
import Layout from "../components/layout"
import { ExampleButton } from "../components/button"

export default () => (
  <Layout>
    <h1 style={{ color: "red", textTransform: "uppercase" }}>Hello world!</h1>
  </Layout>
  <ExampleButton>click me</ExampleButton>
)
```
