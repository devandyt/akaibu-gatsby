---
id: 3-allfile-field
title: allFile Field
sidebar_label: allFile Field
---

In GraphiQL, set up the following query knowing that we now have access to allFile field.

:::note
Use `ctrl + Space` to show suggestions of sub-fields.
:::

```graphql
{
  allFile {
    totalCount
    edges {
      node {
        size
        birthTime
        absolutePath
      }
    }
  }
}
```

edges and nodes both represent items (collection of things), and once you drill down you then work with the one specific thing. edge is the old way.

with edges we can access the collection of things.

Once we run the query, the images will show up in the results pane. Remember we set the plugin to point to our images folder in gatsby-config.js.

However, it is better to use nodes instead of edges, which produces the same results, so that we can skip one level of field.

```graphql
{
  allFile {
    totalCount
    nodes {
      size
      birthTime
      absolutePath
    }
  }
}
```
