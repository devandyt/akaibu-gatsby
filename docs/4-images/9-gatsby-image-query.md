---
id: 9-gatsby-image-query
title: gatsby-image Query
sidebar_label: gatsby-image Query
---

Let's try to set a query looking for two images, one fixed image and one fluid image.

Open GraphiQL and consider the following example.

```graphql
{
  fixed: file(relativePath: { eq: "image-3.jpeg" }) {
    childImageSharp {
      fixed {
        src
      }
    }
  }
}
```

we successfaully got back image number 3 in our response.

Now let's try get back image number 4 as a fluid image within the same query.

```graphql
{
  fixed: file(relativePath: { eq: "image-3.jpeg" }) {
    childImageSharp {
      fixed {
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
```

We get both images now. Please note that in our actual query, we replace src with fragments to get the useful fields.

We can set the width and height for fixed image query and likewise set maxWidth for fluid image queries.

```graphql
{
  fixed: file(relativePath: { eq: "image-3.jpeg" }) {
    childImageSharp {
      fixed(width: 300, height: 400) {
        src
      }
    }
  }
}
```
