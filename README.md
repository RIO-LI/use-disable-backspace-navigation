# @sinouiincubator/use-disable-backspace-navigation

[![npm version](https://img.shields.io/npm/v/@sinouiincubator/use-disable-backspace-navigation)](https://www.npmjs.com/package/@sinouiincubator/use-disable-backspace-navigation)
[![downloads](https://img.shields.io/npm/dm/@sinouiincubator/use-disable-backspace-navigation)](https://www.npmjs.com/package/@sinouiincubator/use-disable-backspace-navigation)

阻止 IE、Firefox 等浏览器中按下 **回格键（ Backspace ）** 时页面发生回退的默认行为。

## 安装

```shell
yarn add @sinouiincubator/use-disable-backspace-navigation
```

或者

```shell
npm add @sinouiincubator/use-disable-backspace-navigation --save
```

## 使用

建议在 React 项目的根组件中添加，如 `App` 组件：

```tsx
import useDisableBackspaceNavigation from '@sinouiincubator/use-disable-backspace-navigation';

function App() {
  useDisableBackspaceNavigation();

  return <div className="app" />;
}
```

## 说明

`use-disable-backspace-navigation` 不会影响正常的输入框（ `input` ）、多行文本框（ `textarea` ）、可编辑元素（ `contentEditable` ）的输入行为，即按回退键删除内容。更多细节见 [stackoverflow 上的讨论](https://stackoverflow.com/questions/1495219/how-can-i-prevent-the-backspace-key-from-navigating-back)。

## 本地开发

项目中有以下有用的命令。

### `yarn start`

在开发和监听模式下启动项目。当代码发生变化时就会重新编译代码。它同时会实时地向你汇报项目中的代码错误。

### `yarn build`

打包，并将打包文件放在`dist`文件夹中。使用 rollup 对代码做优化并打包成多种格式（`Common JS`，`UMD`和`ES Module`）。

### `yarn lint`

`yarn lint`会检查整个项目是否有代码错误、风格错误。

开启 vscode 的 eslint、prettier 插件，在使用 vscode 编码时，就会自动修正风格错误、提示语法错误。

### `yarn format`

`yarn format`可以自动调整整个项目的代码风格问题。

### `yarn test`

`yarn test`以监听模式启动 jest，运行单元测试。

开启 vscode 的 jest 插件，会在文件变化时自动运行单元测试。
