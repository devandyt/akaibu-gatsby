---
id: 2-gatsby-datalayer
title: Gatsby Datalayer
sidebar_label: Gatsby Datalayer
---

Gatsby is built on react, so a project will consist of components (pages, title, heading etc...), of which some may render data (API's, Headless CMS, JSON, Markdown, SiteMetaData etc...). To access this data, Gatsby uses GraphQL.

GraphQL is the syntax of how to ask for data and uses type system to describe the data

We create and test our queries using the sandbox IDE GraphiQL.

We can display and render our data using `<StaticQuery> or <PageQuery>`.

`<StaticQuery>` for any components
`<PageQuery>` only for page components but can accept variables.
