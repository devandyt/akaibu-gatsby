---
id: 10-render-gatsby-image-setup
title: Render gatsby-image Setup
sidebar_label: Render gatsby-image Setup
---

To compare the difference between react image, gatsby fixed image, and gatsby fluid image, we will create a new images component.

_components/examples/images.js_

```js
import React from "react"

const Images = () => {
  return <div>hello from images!</div>
}

export default Images
```

_pages/images.js_

```js
import React from "react"
import Layout from "../components/layout"

const images = () => {
  return (
    <Layout>
      <Images />
    </Layout>
  )
}

export default images
```

Navbar.js

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
                <li>
                    <Link to "/images">Images</Link>
                </li>
            </ul>
        </nav>
    )
}

export default Navbar
```

Now we import what we need.

```js
import React from "react"
import { graphql, useStaticQuery } from "gatsby"
import img from "../images/image-4.jpeg"
import Image from "gatsby-image"

const Images = () => {
  return (
    <section className="images">
      <article className="single-image">
        <h3>basic image</h3>
      </article>
      <article className="single-image">
        <h3>fixed image/blur</h3>
      </article>
      <article className="single-image">
        <h3>fluid image/svg</h3>
      </article>
    </section>
  )
}

export default Images
```

Add some css for image.

_layout.css_

```css
.images {
  text-align: center;
  text-transform: capitalize;
  width: 80vw;
  margin: 0 auto 10rem auto;
}
.single-image {
  border: 3px solid red;
  padding: 1rem 0;
}
@media screen and (min-width: 992) {
  .images {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    column-gap: 1rem;
  }
}
```

Finally we can set up our query.

```js
import React from "react"
import { graphql, useStaticQuery } from "gatsby"
import img from "../images/image-4.jpeg"
import Image from "gatsby-image"

const getImages = graphql`
  {
    fixed: file(relativePath: { eq: "image-3.jpeg" }) {
      childImageSharp {
        fixed(width: 300, height: 400) {
          src
        }
      }
    }
    fluid: file(relativePath: { eq: "image-4.jpeg" }) {
      childImageSharp {
        fluid {
          src
        }
      }
    }
  }
`

const Images = () => {
  return (
    <section className="images">
      <article className="single-image">
        <h3>basic image</h3>
      </article>
      <article className="single-image">
        <h3>fixed image/blur</h3>
      </article>
      <article className="single-image">
        <h3>fluid image/svg</h3>
      </article>
    </section>
  )
}

export default Images
```
