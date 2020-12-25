---
id: 3-create-pages
title: Create Pages
sidebar_label: Create Pages
---

## Simple Page Setup

Creating pages in Gatsby is easy, just create files in /pages folder. By convention, the root page is _index.js_.

> _index.js_ for **Home Page**  
> _About.js_ for **About Page**  
> _Contact.js_ for **Contact Page**  
> etc...

:::note

Note: These file names show up in the URL, e.g. http://localhost:8000/about

:::

## Familiarity

Open _pages/index.js_, notice that it is a react component with `export default.`

```js
import React from "react";

export default () => <div>Hello world!</div>;
```
