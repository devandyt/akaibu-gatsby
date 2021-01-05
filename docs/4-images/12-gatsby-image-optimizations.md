---
id: 12-gatsby-image-optimizations
title: gatsby-image Optimizations
sidebar_label: gatsby-image Optimizations
---

So why go through the trouble to use gatsby-image, well, straight out of the box gatsby-images provides many benefits.

## Problem

Large, unoptimized images dramatically slow down your site.

But creating optimized images for websites has long been a thorny problem. Ideally you would:

Resize large images to the size needed by your design.
Generate multiple smaller images so smartphones and tablets don’t download desktop-sized images.
Strip all unnecessary metadata and optimize JPEG and PNG compression.
Efficiently lazy load images to speed initial page load and save bandwidth.
Use the “blur-up” technique or a ”traced placeholder” SVG to show a preview of the image while it loads.
Hold the image position so your page doesn’t jump while images load.
Doing this consistently across a site feels like a task that can never be completed. You manually optimize your images and then… several images are swapped in at the last minute or a design-tweak shaves 100px of width off your images.

Most solutions involve a lot of manual labor and bookkeeping to ensure every image is optimized.

This isn’t ideal. Optimized images should be easy and the default.

gatsby-image takes care of the above problems.
