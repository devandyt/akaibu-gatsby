---
id: 8-example-setup
title: Example Setup
sidebar_label: Example Setup
---

To keep things tidy, restructure the project by creating the folders.

Create the following folder and files.
_src/examples/_
_pages/examples.js_

```js
import React from "react"

const examples = () => {
  return (
    <div>
      <h1>hello from examples page</h1>
    </div>
  )
}

export default examples
```

Add examples page to the navbar.

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
                <li>
                    <Link to "/examples">Examples</Link>
                </li>
            </ul>
        </nav>
    )
}

export default Navbar
```
