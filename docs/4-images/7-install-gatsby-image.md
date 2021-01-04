---
id: 7-install-gatsby-image
title: Install gatsby-image
sidebar_label: Install gatsby-image
---

Gatsby offers great image optimization options with the gatsby-image plugin.

Download gatsby-image plugin.  
https://www.gatsbyjs.com/plugins/?=gatsby-image

Note that as well as gatsby-image, you also need to install gatsby-transformer-sharp and gatsby-plugin-sharp, and including them in gatsby-config.

_gatsby-config.js_

```js
module.export = {
  siteMetadata: {
    title: "Gatsby Tutorial",
    description: "some text",
    author: "@johndoe",
    data: ["item 1", "item 2"],
    person: { name: "peter", age: "32" },
  },
  plugins: [
    `gatsby-plugin-styled-components`,
    `gatsby-transformer-sharp`,
    `gatsby-plugin-sharp`,
    {
      resolve: `gatsby-source-filesystem`,
      options: {
        name: `images`,
        path: `${__dirname}/src/images/`,
      },
    },
  ],
}
```

Restart dev server.
