# Documentation-and-good-practices

> Este repositorio es para adjuntar herramientas, documentación importante para crear un servicio de streeming.

[![github release version](https://img.shields.io/github/v/release/nhn/tui.editor.svg?include_prereleases)](https://github.com/nhn/tui.editor/releases/latest)  [![license](https://img.shields.io/github/license/nhn/tui.editor.svg)](https://github.com/nhn/tui.editor/blob/master/LICENSE) [![PRs welcome](https://img.shields.io/badge/PRs-welcome-ff69b4.svg)](https://github.com/nhn/tui.editor/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22) ![code with hearth by NHN Cloud](https://img.shields.io/badge/%3C%2F%3E%20with%20%E2%99%A5%20by-NHN_Cloud-ff1414.svg)


## 🚩 Table of Contents

- [URL](#-url)
- [Learned lessons?](#-learned-lessons)
- [Features](#-features)
- [Examples](#-examples)
- [Browser Support](#-browser-support)
- [Pull Request Steps](#-pull-request-steps)
- [Contributing](#-contributing)
- [TOAST UI Family](#-toast-ui-family)
- [Used By](#-used-by)
- [License](#-license)


## 📦 URL

### Back

| Name | Description |
| --- | --- |
| [`@devdocs.io`](https://devdocs.io/) | Documentacion variada |
| [`@jestjs.io`](https://jestjs.io/docs/jest-object#jestmockedtitem-t-deep--false) | Moked |
| [`@guias.makeitreal.camp`](https://guias.makeitreal.camp/react/testing) | guias.makeitreal.camp |

### Front

| Name | Description |
| --- | --- |
| [`@toast-ui/react-editor`](https://github.com/nhn/tui.editor/tree/master/apps/react-editor) | [React](https://reactjs.org/) wrapper component |
| [`@toast-ui/vue-editor`](https://github.com/nhn/tui.editor/tree/master/apps/vue-editor) | [Vue](https://vuejs.org/) wrapper component |

### Others

| Name | Description |
| --- | --- |
| [`@toast-ui/editor-plugin-chart`](https://github.com/nhn/tui.editor/tree/master/plugins/chart) | Plugin to render chart |
| [`@toast-ui/editor-plugin-code-syntax-highlight`](https://github.com/nhn/tui.editor/tree/master/plugins/code-syntax-highlight) | Plugin to highlight code syntax |
| [`@toast-ui/editor-plugin-color-syntax`](https://github.com/nhn/tui.editor/tree/master/plugins/color-syntax) | Plugin to color editing text |
| [`@toast-ui/editor-plugin-table-merged-cell`](https://github.com/nhn/tui.editor/tree/master/plugins/table-merged-cell) | Plugin to merge table columns |
| [`@toast-ui/editor-plugin-uml`](https://github.com/nhn/tui.editor/tree/master/plugins/uml) | Plugin to render UML |


## 🤖 Learned lessons?

El asistente de prueba simulado proporciona escrituras en sus módulos simulados e incluso sus métodos profundos, en función de la escritura de su fuente. Hace uso de la última característica de TypeScript, por lo que incluso tiene tipos de argumentos completos en el IDE (a diferencia de jest.MockInstance).

 *Nota: si bien debe ser una función para que se cambie el tipo de entrada, el asistente en sí no hace nada más que devolver el valor de entrada dado.. *

### Productive Markdown Mode



**CommonMark + GFM Specifications**

Today *CommonMark* is the de-facto *Markdown* standard. *GFM (GitHub Flavored Markdown)* is another popular specification based on *CommonMark* - maintained by *GitHub*, which is the *Markdown* mostly used. TOAST UI Editor follows both [*CommonMark*](http://commonmark.org/) and [*GFM*](https://github.github.com/gfm/) specifications. Write documents with ease using productive tools provided by TOAST UI Editor and you can easily open the produced document wherever the specifications are supported.

* **Live Preview** : Edit Markdown while keeping an eye on the rendered HTML. Your edits will be applied immediately.
* **Scroll Sync** : Synchronous scrolling between Markdown and Preview. You don't need to scroll through each one separately.
* **Syntax Highlight** : You can check broken Markdown syntax immediately.

### Easy WYSIWYG Mode



* **Table** : Through the context menu of the table, you can add or delete columns or rows of the table, and you can also arrange text in cells.
* **Custom Block Editor** : The custom block area can be edited through the internal editor.
* **Copy and Paste** : Paste anything from browser, screenshot, excel, powerpoint, etc.




### Use of Various Extended Functions - Plugins


CommonMark and GFM are great, but we often need more abstraction. The TOAST UI Editor comes with powerful **Plugins** in compliance with the Markdown syntax.

**Five basic plugins** are provided as follows, and can be downloaded and used with npm.

* [**`chart`**](https://github.com/nhn/tui.editor/tree/master/plugins/chart) : A code block marked as a 'chart' will render [TOAST UI Chart](https://github.com/nhn/tui.chart).
* [**`code-syntax-highlight`**](https://github.com/nhn/tui.editor/tree/master/plugins/code-syntax-highlight) : Highlight the code block area corresponding to the language provided by [Prism.js](https://prismjs.com/).
* [**`color-syntax`**](https://github.com/nhn/tui.editor/tree/master/plugins/color-syntax) : 
Using [TOAST UI ColorPicker](https://github.com/nhn/tui.color-picker), you can change the color of the editing text with the GUI.
* [**`table-merged-cell`**](https://github.com/nhn/tui.editor/tree/master/plugins/table-merged-cell) : 
You can merge columns of the table header and body area.
* [**`uml`**](https://github.com/nhn/tui.editor/tree/master/plugins/uml) : A code block marked as an 'uml' will render [UML diagrams](http://plantuml.com/screenshot).

## 🎨 Features

* [Viewer](https://github.com/nhn/tui.editor/tree/master/docs/en/viewer.md) : Supports a mode to display only markdown data without an editing area.
* [Internationalization (i18n)](https://github.com/nhn/tui.editor/tree/master/docs/en/i18n.md) : Supports English, Dutch, Korean, Japanese, Chinese, Spanish, German, Russian, French, Ukrainian, Turkish, Finnish, Czech, Arabic, Polish, Galician, Swedish, Italian, Norwegian, Croatian + language and you can extend.
* [Widget](https://github.com/nhn/tui.editor/tree/master/docs/en/widget.md) : This feature allows you to configure the rules that replaces the string matching to a specific `RegExp` with the widget node.
* [Custom Block](https://github.com/nhn/tui.editor/tree/master/docs/en/custom-block.md) : Nodes not supported by Markdown can be defined through custom block. You can display the node what you want through writing the parsing logic with custom block.

## 🐾 Examples

* [Basic](https://nhn.github.io/tui.editor/latest/tutorial-example01-editor-basic)
* [Viewer](https://nhn.github.io/tui.editor/latest/tutorial-example04-viewer)
* [Using All Plugins](https://nhn.github.io/tui.editor/latest/tutorial-example12-editor-with-all-plugins)
* [Creating the User's Plugin](https://nhn.github.io/tui.editor/latest/tutorial-example13-creating-plugin)
* [Customizing the Toobar Buttons](https://nhn.github.io/tui.editor/latest/tutorial-example15-customizing-toolbar-buttons)
* [Internationalization (i18n)](https://nhn.github.io/tui.editor/latest/tutorial-example16-i18n)

Here are more [examples](https://nhn.github.io/tui.editor/latest/tutorial-example01-editor-basic) and play with TOAST UI Editor!


## 🌏 Browser Support

| <img src="https://user-images.githubusercontent.com/1215767/34348387-a2e64588-ea4d-11e7-8267-a43365103afe.png" alt="Chrome" width="16px" height="16px" /> Chrome | <img src="https://user-images.githubusercontent.com/1215767/34348590-250b3ca2-ea4f-11e7-9efb-da953359321f.png" alt="IE" width="16px" height="16px" /> Internet Explorer | <img src="https://user-images.githubusercontent.com/1215767/34348380-93e77ae8-ea4d-11e7-8696-9a989ddbbbf5.png" alt="Edge" width="16px" height="16px" /> Edge | <img src="https://user-images.githubusercontent.com/1215767/34348394-a981f892-ea4d-11e7-9156-d128d58386b9.png" alt="Safari" width="16px" height="16px" /> Safari | <img src="https://user-images.githubusercontent.com/1215767/34348383-9e7ed492-ea4d-11e7-910c-03b39d52f496.png" alt="Firefox" width="16px" height="16px" /> Firefox |
| :---------: | :---------: | :---------: | :---------: | :---------: |
| Yes | 11+ | Yes | Yes | Yes |


## 🔧 Pull Request Steps

TOAST UI products are open source, so you can create a pull request(PR) after you fix issues. Run npm scripts and develop yourself with the following process.

### Setup

Fork `main` branch into your personal repository. Clone it to local computer. Install node modules. Before starting development, you should check if there are any errors.

```sh
$ git clone https://github.com/{your-personal-repo}/tui.editor.git
$ npm install
$ npm run build toastmark
$ npm run test editor
```

> TOAST UI Editor uses [npm workspace](https://docs.npmjs.com/cli/v7/using-npm/workspaces/), so you need to set the environment based on [npm7](https://github.blog/2021-02-02-npm-7-is-now-generally-available/). If subversion is used, dependencies must be installed by moving direct paths per package.

### Develop

You can see your code reflected as soon as you save the code by running a server. Don't miss adding test cases and then make green rights.

#### Run snowpack-dev-server
[snowpack](https://www.snowpack.dev/) allows you to run a development server without bundling.

``` sh
$ npm run serve editor
```

#### Run webpack-dev-server
If testing of legacy browsers is required, the development server can still be run using a [webpack](https://webpack.js.org/).

``` sh
$ npm run serve:ie editor
```

#### Run test

``` sh
$ npm test editor
```

### Pull Request

Before uploading your PR, run test one last time to check if there are any errors. If it has no errors, commit and then push it!

For more information on PR's steps, please see links in the Contributing section.

## 💬 Contributing

* [Code of Conduct](https://github.com/nhn/tui.editor/blob/master/CODE_OF_CONDUCT.md)
* [Contributing Guideline](https://github.com/nhn/tui.editor/blob/master/CONTRIBUTING.md)
* [Commit Convention](https://github.com/nhn/tui.editor/blob/master/docs/COMMIT_MESSAGE_CONVENTION.md)
* [Issue Guidelines](https://github.com/nhn/tui.editor/tree/master/.github/ISSUE_TEMPLATE)


## 🍞 TOAST UI Family

- [TOAST UI Calendar](https://github.com/nhn/tui.calendar)
- [TOAST UI Chart](https://github.com/nhn/tui.chart)
- [TOAST UI Grid](https://github.com/nhn/tui.grid)
- [TOAST UI Image Editor](https://github.com/nhn/tui.image-editor)
- [TOAST UI Components](https://github.com/nhn)


## 🚀 Used By

* [NHN Dooray! - Collaboration Service (Project, Messenger, Mail, Calendar, Drive, Wiki, Contacts)](https://dooray.com)
* [UNOTES - Visual Studio Code Extension](https://marketplace.visualstudio.com/items?itemName=ryanmcalister.Unotes)


## 📜 License

This software is licensed under the [MIT](https://github.com/nhn/tui.editor/blob/master/LICENSE) © [NHN Cloud](https://github.com/nhn).
