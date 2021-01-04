---
id: 6-sourceinstancename
title: sourceInstanceName
sidebar_label: sourceInstanceName
---

When setting up gatsby-source-filesystem plugin, the name property is important.

Create a new folder in src folder src/posts/.

Create two dummy files in the new folder (post.ext and post-2.txt).

In gatsby-config.js, we are currently not sourcing the new files in the posts folder.

We need to tell the plugin to look for them.

We could change our name property to look for the entire src/ folder, but that will be too many unneeded files and requires too much filtering when writing the query.

A better way would to create another instance of our plugin that points to posts/ folder.

```js
plugins: [
  `gatsby-plugin-styled-components`,
  {
    resolve: `gatsby-source-filesystem`,
    options: {
      name: `images`,
      path: `${__dirname}/src/images/`,
    },
  },
  {
    resolve: `gatsby-source-filesystem`,
    options: {
      name: `posts`,
      path: `${__dirname}/src/posts/`,
    },
  },
]
```

Restart the dev server.

In GraphiQL, set up a new query. Notice that we now get back all files in both the images and posts folders.

```graphql
query MyQuery {
  allFile {
    totalCount {
      nodes {
        absolutePath
        size
      }
    }
  }
}
```

If I only want to search for files in posts folders.

```graphql
query MyQuery {
  allFile(filter: { sourceInstanceName: { eq: "posts" } }) {
    totalCount {
      nodes {
        absolutePath
        size
      }
    }
  }
}
```
