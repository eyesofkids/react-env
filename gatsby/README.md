# Visual Studio Code 中的 Gatsby 專案 ESLint 與 Prettier 設定方式

ref: [https://www.gatsbyjs.org/docs/eslint/](https://www.gatsbyjs.org/docs/eslint/)

## 專案部份

### 第 1 步: 建立新的專案

```sh
npm install -g gatsby-cli
gatsby new gatsby-site
```

### 第 2 步: 安裝 ESLint 與 Prettier 模組

在終端機裡，對應專案的根目錄，輸入以下的指令:

yarn 使用:

```sh
yarn add eslint-plugin-prettier prettier eslint-config-react-app eslint-plugin-import eslint-plugin-react eslint-plugin-jsx-a11y eslint-plugin-react-hooks
```

npm 使用:

```sh
npm install --save-dev eslint-plugin-prettier prettier eslint-config-react-app eslint-plugin-import eslint-plugin-react eslint-plugin-jsx-a11y eslint-plugin-react-hooks
```

### 第 3 步: 加入 eslint 與 prettier 設定檔案

下載 `.eslintrc.js` 與 `.prettierrc` 與 `.eslintignore` 的設定檔，拷貝到專案的根目錄。

註: `.prettierrc` 目前gatsby有內建檔案，蓋掉原本的。

---

## VS Code 開發工具部份

### 第 1 步: 安裝 VS Code 中的 ESLint 與 Prettier 擴充

安裝以下兩個 VS Code 擴充 (使用擴充套件搜尋名稱即可，安裝下載量最多的。):

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

### 第 2 步: 更新 VS Code 設定

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
