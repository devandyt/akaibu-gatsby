---
id: 4-query-arguments
title: Query Arguments
sidebar_label: Query Arguments
---

Arguments can be used on any queries and they allow you to be more specific about data you are getting back.

For example, I can limit my query response to only 1 item or skip the first item or filter for specific items.

In Graphiql, consider the following example, we can limit our results to 3.

```graphql
{
  allFile(limit: 3) {
    totalCount
    nodes {
      size
      birthTime
      absolutePath
    }
  }
}
```

We can skip the first item.

```graphql
{
  allFile(skip: 1) {
    totalCount
    nodes {
      size
      birthTime
      absolutePath
    }
  }
}
```

We can sort our response based on file size with largest first.

```graphql
{
  allFile(sort: { fields: size, order: DESC }) {
    totalCount
    nodes {
      size
      birthTime
      absolutePath
    }
  }
}
```

We can filter based on a field. Create copy folder inside images folder and place some images inside. The response for the below query will only show files in our copy folder.

```graphql
{
  allFile(filter: { relativeDirectory: { eq: "copy" } }) {
    totalCount
    nodes {
      size
      birthTime
      absolutePath
    }
  }
}
```

:::note
The above arguments can be used in combination by seperating them with comma, e.g. `allFile(limit: 4, skip: 2)`
:::
