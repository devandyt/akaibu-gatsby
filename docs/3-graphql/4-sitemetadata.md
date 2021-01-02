---
id: 4-sitemetadata
title: SiteMetadata
sidebar_label: SiteMetadata
---

To demostrate write queries, let's first add some simple data we can query to our project in the form of siteMetadata. This data can be set up in gatsby-config.js

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
  plugins: [`gatsby-plugin-styled-components`],
}
```

Restart the development server.
