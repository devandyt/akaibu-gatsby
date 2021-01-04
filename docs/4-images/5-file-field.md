---
id: 5-file-field
title: file Field
sidebar_label: file Field
---

The source file system plugin also makes available the file field in GraphQL. While the allFile field will give you all files in a directory, the file field gives you 1 file.

To showcase, consider the below example, where you will get a 1 item repsonse back:

```graphql
{
  file {
    size
    relativePath
  }
}
```

The issue here is that you cannot really control which file you get back.

To specify which file you get back, you can use arguments.

```graphql
{
  file(relativePath: { eq: "copy/image-1.jpeg" }) {
    size
    relativePath
  }
}
```

When creating up pags dynamically we will rely heavily on single item fields like this file field.
