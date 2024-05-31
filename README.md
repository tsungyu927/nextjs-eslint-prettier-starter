# Next.js + ESLint + Prettier + Typescript Project Starter

Feel free to use it at anywhere~

## 在這個範例中使用到的技術如下:

- [Typescript](https://www.typescriptlang.org/)
- [Next.js](https://nextjs.org/) (Version 14 with App Router)
- [TailwindCSS](https://tailwindcss.com/)
- [ESLint (Airbnb)](https://github.com/airbnb/javascript)
- [Prettier](https://prettier.io/)

## ESLint 相關套件

| 套件 | 說明 | 依賴(需要哪些額外套件) |
| -------- | -------- | -------- |
| eslint | ESLint 本身，用來識別並回報在 ECMAScript/JavaScript 中不符合規定的程式碼  |  |
| eslint-config-airbnb | 為 Javascript 和 React 程式碼提供一組由 Airbnb 定義的 rules 和 style 指南 | `eslint`, `eslint-plugin-import`, `eslint-plugin-react`, `eslint-plugin-react-hooks`, `eslint-plugin-jsx-a11y` |
| eslint-config-next | 包括一組專門針對 Next.js 量身定製的(推薦的) ESLint 規則      |  |
| eslint-config-prettier | 這個 extension 會關掉 ESLint 中所有跟 Prettier 衝突(或不必要)的 rules |  |
| eslint-plugin-import | 這個 Plugin 支援 linting ES2015+(ES6+) 的 import/export 語法，並防止出現錯誤的檔案路徑和錯誤的 import 名稱 |  |
| eslint-plugin-jsx-a11y | 這個 Plugin 提供一組 rules 來在 JSX 中執行 accessibility 的最佳實踐，他幫助我們識別並修正一些常見的 accessibility 的問題 | `eslint` |
| eslint-plugin-unused-imports | 這個 Plugin 會找到並且移除沒有使用的 ES6 module import | * Typescript: `@typescript-eslint/eslint-plugin`, `@typescript-eslint/parser` <br> * React: `eslint-plugin-react` (並且 enable `react/jsx-uses-react` 和 `react/jsx-uses-vars`) |
| eslint-import-resolver-typescript | 與 `eslint-plugin-import` 插件配合使用，幫助 ESLint 根據 TypeScript 的配置來理解並正確解析 module 的路徑 | `eslint`, `eslint-plugin-import` |
| @typescript-eslint/eslint-plugin | 一個 ESLint 的 Plugin，為 Typescript codebases 提供 lint rules | |
| @typescript-eslint/parser | 一個 ESLint 的 parser，他借助 [Typescript ESTree](https://github.com/typescript-eslint/typescript-eslint/tree/main/packages/typescript-estree) 來允許 ESLint lint Typescript 程式碼 | |

> `eslint-config-airbnb` 依賴套件中的`eslint-plugin-react`和`eslint-plugin-react-hooks` 已經由 `eslint-config-next` 內建提供，因此就不用額外新增這兩個 Plugin ([相關連結](https://nextjs.org/docs/app/building-your-application/configuring/eslint#eslint-config))

> `eslint-plugin-jsx-a11y` 雖然會被 `eslint-config-airbnb` 使用到，但**不需要**手動新增 plugin，因此在 .eslintrc.json 中**不需要**加上 `plugins: ["jsx-a11y"]`

## Prettier 相關套件

| 套件 | 說明 | 依賴(需要哪些額外套件) |
| -------- | -------- | -------- |
| prettier | Prettier 本身，用來格式化程式碼 | |
| prettier-plugin-tailwindcss | 是一個 Plugin，也是 TailwindCSS 官方推薦的 Plugin，用來自動排序程式碼中的 classes | `prettier` |
| @trivago/prettier-plugin-sort-imports | 是一個 Plugin，用來排序程式碼中 import 的順序，可以在 `.prettierrc` 中自訂義順序 | `prettier` |

> 其他 Convention:
> 1. JSX 屬性請使用 **double quotes (`"`)**；其他 JS 請使用 **single quotes (`'`)**
> 2. 其他 Airbnb 相關規範請參考我整理的這一份（[Link](https://hurricane-activity-c3d.notion.site/ESLint-Prettier-Rules-df67abf7c83d413b86d07a3b6bb3a9e1?pvs=4)）