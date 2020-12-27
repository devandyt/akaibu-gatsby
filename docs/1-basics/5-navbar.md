---
id: 5-navbar
title: Navbar
sidebar_label: Navbar
---

## Setting Up

No point in hardcoding links on every page. We need a way to reuse the links on all pages.

By convension, usually you set up a /src/components/ folder to store your components.

Create Navbar.js component inside the folder.

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

Next we need to use this component in our pages.

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

## Practice 1

Try adding Navbar components to the blog and products pages.
