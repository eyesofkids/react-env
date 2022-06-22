# Visual Studio Code 中的 CRA 專案 ESLint 與 Prettier 設定方式(TypeScript)

- 註: [CRA 3.0 已經內附 ESLint 與 TS linting 支援](https://github.com/facebook/create-react-app/issues/6475)
- 註: 以下 Create-React-App 簡稱為 CRA
- 註: 以下 Visual Studio Code 簡稱為 VS Code
- 註: [yarn](https://yarnpkg.com/) 需要額外安裝，Yarn 是 Facebook 提供的替代 npm 的工具，可以加速 node 模組的下載，推薦使用。

## CRA 專案部份

### 第 1 步: 建立專案

```sh
npx create-react-app my-app --template typescript
```

或

```sh
yarn create react-app my-app --template typescript
```

> 註: 全域的 create-react-app 工具程式已不支援，如有安裝請先移除

> 註: 也可以從現有的專案安裝 typescript 支援的相關模組，請參考 [CRA 官方網站 - Adding TypeScript](https://create-react-app.dev/docs/adding-typescript/)

### 第 2 步: 安裝 ESLint 與 Prettier 模組

```sh
yarn add prettier eslint-config-prettier eslint-plugin-prettier eslint-plugin-react-hooks
```

```sh
npm install --save-dev prettier eslint-config-prettier eslint-plugin-prettier eslint-plugin-react-hooks
```

## 第 3 步: 加入 eslint 與 prettier 設定檔案

下載 `.eslintrc` 與 `.prettierrc` 與 `.eslintignore` 的設定檔，拷貝到專案的根目錄。

---

## VS Code 開發工具部份

### 第 1 步: 安裝 VS Code 中的 ESLint 與 Prettier 擴充

安裝以下兩個 VS Code 擴充 (使用擴充套件搜尋名稱即可，安裝下載量最多的。):

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

## 第 2 步: 更新 VS Code 設定

請將以下的設定加到你的 VSCode 使用者設定之中(選單->喜好設定)：

```json
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": false
  },
  "prettier.disableLanguages": ["js"],
  "eslint.autoFixOnSave": true,
  "eslint.alwaysShowStatus": true,
  "files.autoSave": "afterDelay",
```

### 第 3 步: ESLint 於 VS Code 中的相關設定

VS Code 的`settings.json`檔案中加入以下的設定。

```json
"eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
],
```

> 註: 截至 2019.11 仍然需要這樣設定

## 參考資料

- [Adding TypeScript](https://create-react-app.dev/docs/adding-typescript/)
- [Autofix lightbulb not shown in TypeScript](https://github.com/Microsoft/vscode-eslint/issues/609)
