---
id: 1-gatsby-and-graphql-intro
title: Gatsby and GraphQL Intro
sidebar_label: Gatsby and GraphQL Intro
---

## Data in Gatsby

A website has four parts: HTML, CSS, JS, and data. The first half of the tutorial focused on the first three. Now let’s learn how to use data in Gatsby sites.

## What is data?

A very computer science-y answer would be: data is things like "strings", integers (42), objects ({ pizza: true }), etc.

For the purpose of working in Gatsby, however, a more useful answer is “everything that lives outside a React component”.

So far, you’ve been writing text and adding images directly in components. Which is an excellent way to build many websites. But, often you want to store data outside components and then bring the data into the component as needed.

If you’re building a site with WordPress (so other contributors have a nice interface for adding & maintaining content) and Gatsby, the data for the site (pages and posts) are in WordPress and you pull that data, as needed, into your components.

Data can also live in file types like Markdown, CSV, etc. as well as databases and APIs of all sorts.

> Gatsby’s data layer lets you pull data from these (and any other source) directly into your components — in the shape and form you want.

## Using Unstructured Data vs GraphQL

### Do I have to use GraphQL and source plugins to pull data into Gatsby sites?

Absolutely not! You can use the node createPages API to pull unstructured data into Gatsby pages directly, rather than through the GraphQL data layer. This is a great choice for small sites, while GraphQL and source plugins can help save time with more complex sites.

See the Using Gatsby without GraphQL guide to learn how to pull data into your Gatsby site using the node createPages API and to see an example site!

### When do I use unstructured data vs GraphQL?

If you’re building a small site, one efficient way to build it is to pull in unstructured data as outlined in this guide, using createPages API, and then if the site becomes more complex later on, you move on to building more complex sites, or you’d like to transform your data, follow these steps:

Check out the Plugin Library to see if the source plugins and/or transformer plugins you’d like to use already exist
If they don’t exist, read the Plugin Authoring guide and consider building your own!

### How Gatsby’s data layer uses GraphQL to pull data into components

There are many options for loading data into React components. One of the most popular and powerful of these is a technology called GraphQL.

GraphQL was invented at Facebook to help product engineers pull needed data into components.

GraphQL is a **q**uery **l**anguage (the QL part of its name). If you’re familiar with SQL, it works in a very similar way. Using a special syntax, you describe the data you want in your component and then that data is given to you.

Gatsby uses GraphQL to enable components to declare the data they need.
