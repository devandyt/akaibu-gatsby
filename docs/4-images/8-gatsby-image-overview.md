---
id: 8-gatsby-image-overview
title: gatsby-image Overview
sidebar_label: gatsby-image Overview
---

Large and unoptimized images will slow down your website. Gatsby image does the hard work for you.

To use it, we first need to import Img component from gatsby-image.

Whenever we want to render an image, we would pass in our Img component.

This Img component looks for two props, either for a fixed prop (for fixed image size) or a fluid prop (for responsive image size).

The prop then takes in data from our GraphQL query.

:::note
The image type chosen at query stage must match with the type of prop you use. For example, choosing fixed when creating the query means you can only have fixed prop.
:::

Gatsby image also support fragments which are basically part of a query that can be used in multiple queries.

Note you cannot test fragments in the sandbox.
