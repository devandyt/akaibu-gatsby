---
id: 1-install
title: Install
sidebar_label: Install
---

## Official Docs

Visit https://www.gatsbyjs.com/docs/tutorial/part-zero/ to learn more.

## Steps for macOS

1. Install **Homebrew** in Terminal.

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install **node** with Homebrew.

```shell
brew install node
```

3. Install **Gatsby CLI**.

```shell
npm install -g gatsby-cli
```

## VSCode

1. Get the latest version from https://code.visualstudio.com/download.
2. Recommeded plugins:
   - ES7 React/Redux/GraphQL/React-Native snippets
   - Prettier - Code formatter
   - vscode-styled-components
3. Recommended Settings:
   - Set Default Formatter to **esbenp.prettier-vscode**.
   - Check **Format On Paste** and **Format on Save**.
   - Change **Quote Style** to Double.
   - Uncheck **Prettier: Semi** to remove semi colons at end of every line.

## Create Project

1. Install official **hello world starter**.

```shell
gatsby new akaibu-gatsby https://github.com/gatsbyjs/gatsby-starter-hello-world
```

2. Open new project in VSCode.
3. Customize project specific config in _.prettierrc_ as you wish.

_.prettierrc_

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
4. Spin up **development** server at http://localhost:8000/.

```shell
gatsby develop
```

## Get latest GIT version in macOS

1. Check version

```shell
git --version
```

2. Backup (or remove) Apple git (Optional)

```shell
sudo mv /usr/bin/git /usr/bin/git-apple
```

3. Install Homebrew if you didn’t have

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

4. Or update if you already have

```shell
brew update && brew upgrade
```

5. Install Git with Homebrew

```shell
brew install git
```

6. Symbolic link

```shell
brew link --force git
```

7. Quit terminal and open a new terminal, then check version.

```shell
git --version
```

8. You should see…

```shell
git version <latest version>
```

9. Nice! We’re safe now! And next time you can just…

```shell
brew update && brew upgrade
```
