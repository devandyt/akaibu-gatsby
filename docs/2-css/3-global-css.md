---
id: 3-global-css
title: Global CSS
sidebar_label: Global CSS
---

## Global CSS

This option involves creating a seperate CSS file and then apply it to an engolfing JSX element. It makes sense to apply it to the layout component because it wraps all the pages.

Create the css file.

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
```

We can then import the css in our layout component to apply the css.

_components/layout.js_

```jsx
import React from "react"
import Navbar from "./Navbar"
import Footer from "./Footer"
import "./layout.css"

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
Global styles gets override by inline styles.
:::
