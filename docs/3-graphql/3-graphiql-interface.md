---
id: 3-graphiql-interface
title: GraphQL Interface
sidebar_label: GraphQL Interface
---

## The GraphiQL Interface

Open GraphiQL at http://localhost:8000/\_\_graphql

On the left pane is where you set up your queries.
On the right we will get our queried data or an error.
On the bottom left we also have the query variable pane used for more complex queries.

At the top we have some buttons:

1. Play button - run queries (`Ctrl-Enter`).
2. Prettify - format your queries (`Shift-Ctrl-P`)
3. History - toggle query history
4. Explorer - toggle query library
5. Code Explorer - Shows code you would need in your component

## A Basics GraphQL Setup

On the left pane in GraphiQL.

```graphql
{
  allStrapiProducts {
    nodes {
      title
      url
      size
      image {
        childImageSharp {
          fluid(maxWidth: 600)
          src
        }
      }
    }
  }
}
```

In the above, we are looking for a product, unlink REST API where you are dumped the entire object, we are immediately being very specific about which product.

We need to specify which fields (object properties) we are querying.

nodes represent all products and from those products what do I want to get back, title, url, size, and image.

if the field has sub-fields, then we need to drill down even more.

As a result, we get only the specific data we are looking for.

We can only setup the query if we have installed the plugins, which makes our project more manageable.
