---
id: 1-install
title: Install
sidebar_label: Install
slug: /
---

## Official Docs

Visit https://www.gatsbyjs.com/docs/tutorial/part-zero/ to learn more.

## Steps for macOS

1. Install Homebrew in Terminal.

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install node with Homebrew.

```shell
brew install node
```

3. Install Gatsby CLI.

```shell
npm install -g gatsby-cli
```

## VSCode

1. Get the latest version from https://code.visualstudio.com/download.
2. Install plugins:
   - ES7 React/Redux/GraphQL/React-Native snippets
   - Prettier - Code formatter
   - vscode-styled-compomonents
3. In Settings:
   - Set Default Formatter to _esbenp.prettier-vscode_
   - Check _Format On Paste_ and _Format on Save_
   - Change Quote Style to _Double_.

## Create Project

1. Install official hello world starter.

```shell
gatsby new akaibu-gatsby https://github.com/gatsbyjs/gatsby-starter-hello-world
```

2. Open new project in VSCode.
3. Customize project specific config in .prettierrc as you wish.

```json
{
  "endOfLine": "lf",
  "semi": false,
  "singleQuote": false,
  "tabWidth": 2,
  "trailingComma": "es5"
}
```

3. Toggle open integrated terminal `` ctrl + ` ``.
4. Spin up development server at http://localhost:8000/.

```shell
gatsby develop
```
