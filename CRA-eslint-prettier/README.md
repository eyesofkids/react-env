# CRA eslint prettier

## 步驟一：建立新的專案

```sh
create-react-app myapp
```

或

```sh
npx create-react-app my-app
```

## 步驟二：安裝 VS Code 擴充

安裝以下兩個 VS Code 擴充:

- ESLint
- Prettier

## 步驟三：加入 eslint 與 prettier 設定檔案

下載兩個 `.eslintrc` 與 `.prettierrc` 的設定檔，拷貝到專案的根目錄

## 步驟四：更新 VS Code 設定

請將以下的設定加到你的 VSCode 使用者設定之中(選單->喜好設定)：

```json
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": false
  },
  "prettier.disableLanguages": ["js"],
  "eslint.autoFixOnSave": true,
  "eslint.alwaysShowStatus": true,
  "files.autoSave": "onFocusChange",
```

## 步驟五：安裝模組

在終端機裡，對應專案的根目錄，輸入以下的指令:

yarn 使用:

```sh
yarn add eslint-plugin-prettier prettier eslint-config-react-app eslint-plugin-import eslint-plugin-react eslint-plugin-flowtype eslint-plugin-jsx-a11y eslint-plugin-react-hooks
```

npm 使用:

```sh
npm install --save-dev eslint-plugin-prettier prettier eslint-config-react-app eslint-plugin-import eslint-plugin-react eslint-plugin-flowtype eslint-plugin-jsx-a11y eslint-plugin-react-hooks
```

> 註: [yarn](https://yarnpkg.com/) 需要額外安裝，Yarn 是 Facebook 提供的替代 npm 的工具，可以加速 node 模組的下載。
