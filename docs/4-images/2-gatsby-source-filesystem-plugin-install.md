---
id: 2-gatsby-source-filesystem-plugin-install
title: gatsby-source-fileSystem Plugin Install
sidebar_label: gatsby-source-fileSystem Plugin Install
---

We need to install some plugins to make use of Gatsby optimization.

First install the source-filesystem plugin, for sourcing data into your Gatsby application from your local filesystem.:

_gatsby-source-filesystem_  
https://www.gatsbyjs.com/plugins/gatsby-source-filesystem/?=source

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

Restart the dev server.

Once installed, we will have access to allFile field which basically allows you to get specific file in a folder.

:::note
Since this is a node.js file, `__dirname` points to the directory where the file is located.
:::
