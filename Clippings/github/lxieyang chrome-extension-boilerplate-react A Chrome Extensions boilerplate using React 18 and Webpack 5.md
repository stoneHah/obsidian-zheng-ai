---
title: "chrome-extension-boilerplate-react"
owner: "lxieyang"
source: "https://github.com/lxieyang/chrome-extension-boilerplate-react"
website: "/topics/react"
description: "A Chrome Extensions boilerplate using React 18 and Webpack 5."
stars: 3.8
tags:
  - "inbox"
  - "github"
  - "repo"
  - "react"
  - "javascript"
  - "chrome-extension"
  - "npm"
  - "boilerplate"
  - "typescript"
  - "webpack"
created: 2025-04-13
---
## README

[![](https://github.com/lxieyang/chrome-extension-boilerplate-react/raw/master/src/assets/img/icon-128.png)](https://github.com/lxieyang/chrome-extension-boilerplate-react/blob/master/src/assets/img/icon-128.png)

# Chrome Extension (MV3) Boilerplate with React 18 and Webpack 5[![npm](https://camo.githubusercontent.com/926ce4da727681f441e3a2cab3942786a24f1f95f1ac8617e50fce4de1b71523/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f762f6368726f6d652d657874656e73696f6e2d626f696c6572706c6174652d7265616374)](https://www.npmjs.com/package/chrome-extension-boilerplate-react) [![npm-download](https://camo.githubusercontent.com/122c936fd452935e9f412dcefff31b5e0ebaef8b5d584ebe2e06fc396a50d5ee/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f64772f6368726f6d652d657874656e73696f6e2d626f696c6572706c6174652d7265616374)](https://www.npmjs.com/package/chrome-extension-boilerplate-react) [![npm](https://camo.githubusercontent.com/18ef47aee3bf11ee83495b115b0c4fc887aecc3a9711db231de5c3c4299bac96/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f646d2f6368726f6d652d657874656e73696f6e2d626f696c6572706c6174652d7265616374)](https://www.npmjs.com/package/chrome-extension-boilerplate-react)

## Announcements- Recently updated from **[React](https://reactjs.org/)** ~~17~~ to **18**!
- ***This boilerplate adopts [Manifest V3](https://developer.chrome.com/docs/extensions/mv3/intro/mv3-overview/)!***
	- For V2 users, please check out the [manifest-v2](https://github.com/lxieyang/chrome-extension-boilerplate-react/tree/manifest-v2) branch, or use version [3.x](https://www.npmjs.com/package/chrome-extension-boilerplate-react/v/3.3.0).
	- Check out the [Manifest V3 Migration Guide](https://developer.chrome.com/docs/extensions/mv3/intro/mv3-migration/).
- Recently added [devtools](https://developer.chrome.com/docs/extensions/mv3/devtools/) Support! Thanks [GeekaholicLin](https://github.com/lxieyang/chrome-extension-boilerplate-react/issues/17)!
- Recently updated from **[Webpack Dev Server](https://webpack.js.org/configuration/dev-server/)** ~~3.x~~ to **4.x** and **[Webpack](https://webpack.js.org/)** ~~4~~ to **5**!
- Recently added [TypeScript](https://www.typescriptlang.org/) Support!

## FeaturesThis is a basic Chrome Extensions boilerplate to help you write modular and modern Javascript code, load CSS easily and [automatic reload the browser on code changes](https://webpack.github.io/docs/webpack-dev-server.html#automatic-refresh).

This boilerplate is updated with:

- [Chrome Extension Manifest V3](https://developer.chrome.com/docs/extensions/mv3/intro/mv3-overview/)
- [React 18](https://reactjs.org/)
- [Webpack 5](https://webpack.js.org/)
- [Webpack Dev Server 4](https://webpack.js.org/configuration/dev-server/)
- [React Refresh](https://www.npmjs.com/package/react-refresh)
- [react-refresh-webpack-plugin](https://github.com/pmmmwh/react-refresh-webpack-plugin)
- [eslint-config-react-app](https://www.npmjs.com/package/eslint-config-react-app)
- [Prettier](https://prettier.io/)
- [TypeScript](https://www.typescriptlang.org/)

This boilerplate is heavily inspired by and adapted from [https://github.com/samuelsimoes/chrome-extension-webpack-boilerplate](https://github.com/samuelsimoes/chrome-extension-webpack-boilerplate), with additional support for React 18 features, Webpack 5, and Webpack Dev Server 4.

Please open up an issue to nudge me to keep the npm packages up-to-date. FYI, it takes time to make different packages with different versions work together nicely.

## Installing and Running### Procedures:1. Check if your [Node.js](https://nodejs.org/) version is >= **18**.
2. Clone this repository.
3. Change the package's `name`, `description`, and `repository` fields in `package.json`.
4. Change the name of your extension on `src/manifest.json`.
5. Run `npm install` to install the dependencies.
6. Run `npm start`
7. Load your extension on Chrome following:
	1. Access `chrome://extensions/`
	2. Check `Developer mode`
	3. Click on `Load unpacked extension`
	4. Select the `build` folder.
8. Happy hacking.

## StructureAll your extension's code must be placed in the `src` folder.

The boilerplate is already prepared to have a popup, an options page, a background page, and a new tab page (which replaces the new tab page of your browser). But feel free to customize these.

## TypeScriptThis boilerplate now supports TypeScript! The `Options` Page is implemented using TypeScript. Please refer to `src/pages/Options/` for example usages.

## Webpack auto-reload and HRMTo make your workflow much more efficient this boilerplate uses the [webpack server](https://webpack.github.io/docs/webpack-dev-server.html) to development (started with `npm start`) with auto reload feature that reloads the browser automatically every time that you save some file in your editor.

You can run the dev mode on other port if you want. Just specify the env var `port` like this:

```
$ PORT=6002 npm run start
```

## Content ScriptsAlthough this boilerplate uses the webpack dev server, it's also prepared to write all your bundles files on the disk at every code change, so you can point, on your extension manifest, to your bundles that you want to use as [content scripts](https://developer.chrome.com/extensions/content_scripts), but you need to exclude these entry points from hot reloading [(why?)](https://github.com/samuelsimoes/chrome-extension-webpack-boilerplate/issues/4#issuecomment-261788690). To do so you need to expose which entry points are content scripts on the `webpack.config.js` using the `chromeExtensionBoilerplate -> notHotReload` config. Look the example below.

Let's say that you want use the `myContentScript` entry point as content script, so on your `webpack.config.js` you will configure the entry point and exclude it from hot reloading, like this:

{
  …
  entry: {
    myContentScript: "./src/js/myContentScript.js"
  },
  chromeExtensionBoilerplate: {
    notHotReload: \["myContentScript"\]
  }
  …
}

and on your `src/manifest.json`:

{
  "content\_scripts": \[
    {
      "matches": \["https://www.google.com/\*"\],
      "js": \["myContentScript.bundle.js"\]
    }
  \]
}

## Intelligent Code CompletionThanks to [@hudidit](https://github.com/lxieyang/chrome-extension-boilerplate-react/issues/4)'s kind suggestions, this boilerplate supports chrome-specific intelligent code completion using [@types/chrome](https://www.npmjs.com/package/@types/chrome).

## PackingAfter the development of your extension run the command

```
$ NODE_ENV=production npm run build
```

Now, the content of `build` folder will be the extension ready to be submitted to the Chrome Web Store. Just take a look at the [official guide](https://developer.chrome.com/webstore/publish) to more infos about publishing.

## SecretsIf you are developing an extension that talks with some API you probably are using different keys for testing and production. Is a good practice you not commit your secret keys and expose to anyone that have access to the repository.

To this task this boilerplate import the file `./secrets.<THE-NODE_ENV>.js` on your modules through the module named as `secrets`, so you can do things like this:

*./secrets.development.js*

export default { key: '123' };

*./src/popup.js*

import secrets from 'secrets';
ApiCall({ key: secrets.key });

👉 The files with name `secrets.*.js` already are ignored on the repository.

## Resources:- [Webpack documentation](https://webpack.js.org/concepts/)
- [Chrome Extension documentation](https://developer.chrome.com/extensions/getstarted)

---

Michael Xieyang Liu | [Website](https://lxieyang.github.io/)

