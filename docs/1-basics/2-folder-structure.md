---
id: 2-folder-structure
title: Folder Structure
sidebar_label: Folder Structure
---

## Summary

| File / Folder      | Description                                                                                                                |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| _.cache_           | Store cache. No need to edit and will be regenerated every time you run `gatsby develop`. Deleted when run `gatsby clean`. |
| _node_modules/_    | Node dependencies. No need to edit and will be regenerated every time you run `gatsby develop`.                            |
| _public/_          | Production ready application. Generated when run `gatsby build`. Deleted when run `gatsby clean`.                          |
| _src/_             | Where we do most development. Setup pages, components, and queries etc...                                                  |
| _static/_          | Place our assets and automatically be avaiable to /public. Assets place here will not be processed by Gatsby.              |
| _.gitignore_       | Specifies which files to ignore when pushing to Github.                                                                    |
| _.prettierignore_  | Used by prettier package that comes with Gatsby.                                                                           |
| _gatsby-config.js_ | Setup plugins to extend application.                                                                                       |
| _package.json_     | Manifest file for the application.                                                                                         |
