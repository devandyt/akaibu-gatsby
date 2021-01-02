---
id: 12-query-keyword-and-name
title: Query Keyword and Name
sidebar_label: Query Keyword and Name
---

Often, you will find query keyword followed by a query name added to a graphql query.

```js
const getData = graphql`
  query FirstQuery () {
    site {
      info: siteMetadata {
        person {
          age
          name
        }
        author
        data
        description
        title
      }
    }
  }
`
```

Kind in mind that query names must be unique. You cannot have two queries with teh same name even though they are in a different component that is using either a page or static query.

When we start using variables, we will use query names more. The parenthesis after query name is for passing in varaibles.
