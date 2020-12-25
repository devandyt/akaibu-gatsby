---
id: 2-folder-structure
title: Folder Structure
sidebar_label: Folder Structure
---

## Summary

| File / Folder    | Description                                                                                                                |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------- |
| .cache           | Store cache. No need to edit and will be regenerated every time you run `gatsby develop`. Deleted when run `gatsby clean`. |
| /node_modules    | Node dependencies. No need to edit and will be regenerated every time you run `gatsby develop`.                            |
| /public          | Production ready application. Generated when run `gatsby build`. Deleted when run `gatsby clean`.                          |
| /src             | Where we do most development. Setup pages, components, and queries etc...                                                  |
| /static          | Place our assets and automatically be avaiable to /public. Assets place here will not be processed by Gatsby.              |
| .gitignore       | Specifies which files to ignore when pushing to Github.                                                                    |
| .prettierignore  | Used by prettier package that comes with Gatsby.                                                                           |
| gatsby-config.js | Setup plugins to extend application.                                                                                       |
| package.json     | Manifest file for the application.                                                                                         |
