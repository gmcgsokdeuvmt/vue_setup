# 環境構築(WSL)

```
sudo apt install nodejs npm
sudo npm install -g @vue/cli
```

- nodejs v10.19.0
- npm 6.14.4
- @vue/cli 4.5.6

```
vue create all-project
```

# 全部選ぶとどうなるか？

```
? Please pick a preset: Manually select features
? Check the features needed for your project: 
 ◉ Choose Vue version
 ◉ Babel
 ◉ TypeScript
 ◉ Progressive Web App (PWA) Support
 ◉ Router
 ◉ Vuex
 ◉ CSS Pre-processors
 ◉ Linter / Formatter
 ◉ Unit Testing
❯◉ E2E Testing
```

## Vue のバージョンを選ぶ

```
? Choose a version of Vue.js that you want to start the project with (Use arrow keys)
❯ 2.x 
  3.x (Preview) 
```

## クラススタイル？

- Vue + TypeScript で必要な選択肢(https://qiita.com/jesus_isao/items/0b305c7d90c45ad66c1b)
- class-style component syntax では 'vue-class-component' をimport して型をつける
- 使わない場合は・・・？
- TypeScript を今回は使わないので気にしない

```
? Use class-style component syntax? (Y/n) 
```

## Babel alongside TypeScript?

- Vue + TypeScript で必要な選択肢
- TypeScript でも 自動 polyfill などをしてくれる？
- TypeScript を今回は使わないので気にしない

```
? Use Babel alongside TypeScript (required for modern mode, auto-detected polyfills, tra
nspiling JSX)? (Y/n) 
```

## history mode for router?

- vue router を使うと default でハッシュ'#' がついてしまう
- ハッシュなしでも URL 直接入力できるようになるのが history mode
- シングルページアプリケーションなのでルーティングを適切に設定する必要がある

```
? Use history mode for router? (Requires proper server setup for index fallback in produ
ction) (Y/n) 
```

## Sass SCSS? Less? Stylus?

- AltCSS. コンパイルする必要がある

```
? Pick a CSS pre-processor (PostCSS, Autoprefixer and CSS Modules are supported by defau
lt): (Use arrow keys)
❯ Sass/SCSS (with dart-sass) 
  Sass/SCSS (with node-sass) 
  Less 
  Stylus 
```

## Airbnb? Standard? Prettier?

- コーディングスタイル(https://qiita.com/takeharu/items/dee0972e5f39bfd4d7c8)
  - Google JavaScript Style Guide(https://google.github.io/styleguide/javascriptguide.xml)
  - jQuery JavaScript Style Guide(https://contribute.jquery.org/style-guide/js/)
  - Airbnb JavaScript Style Guide(https://github.com/airbnb/javascript)
  - Node.js Style Guide
- フォーマッタ Prettier(https://prettier.io/)
  - コードを自動フォーマットできる（？）


```
? Pick a linter / formatter config: (Use arrow keys)
❯ ESLint with error prevention only 
  ESLint + Airbnb config 
  ESLint + Standard config 
  ESLint + Prettier 
  TSLint (deprecated) 
```

## Lint するタイミングの設定

```
? Pick additional lint features: (Press <space> to select, <a> to toggle all, <i> to inv
ert selection)
❯◉ Lint on save
 ◯ Lint and fix on commit
```

## Unit test をするツール

- Mocha: js のユニットテストツール
- Chai: アサーションツール
- Jest: シンプルさを重視した、快適な JavaScript テスティングフレームワーク

使わないと違いがわからない… Jest は YKKAP のプロジェクトで少し使ったことがある

```
? Pick a unit testing solution: (Use arrow keys)
❯ Mocha + Chai 
  Jest 
```

## E2E テストをするツール

- 3つの選択肢がある。使ってみないと違いがわからない…？

```
? Pick an E2E testing solution: (Use arrow keys)
❯ Cypress (Chrome only) 
  Nightwatch (WebDriver-based) 
  WebdriverIO (WebDriver/DevTools based) 
```

## E2Eテストをする際のカバー対象

```
? Pick browsers to run end-to-end test on (Press <space> to select, <a> to toggle all, <
i> to invert selection)
❯◉ Chrome
 ◯ Firefox
```

## config file をどうするか

```
? Where do you prefer placing config for Babel, ESLint, etc.? (Use arrow keys)
❯ In dedicated config files 
  In package.json 
```

## 結果

```
Vue CLI v4.5.6
? Please pick a preset: Manually select features
? Check the features needed for your project: Choose Vue version, Babel, TS, PWA, Router
, Vuex, CSS Pre-processors, Linter, Unit, E2E
? Choose a version of Vue.js that you want to start the project with 2.x
? Use class-style component syntax? Yes
? Use Babel alongside TypeScript (required for modern mode, auto-detected polyfills, tra
nspiling JSX)? Yes
? Use history mode for router? (Requires proper server setup for index fallback in produ
ction) Yes
? Pick a CSS pre-processor (PostCSS, Autoprefixer and CSS Modules are supported by defau
lt): Sass/SCSS (with dart-sass)
? Pick a linter / formatter config: Basic
? Pick additional lint features: Lint on save
? Pick a unit testing solution: Jest
? Pick an E2E testing solution: Nightwatch
? Pick browsers to run end-to-end test on Chrome, Firefox
? Where do you prefer placing config for Babel, ESLint, etc.? In package.json
? Save this as a preset for future projects? No
```

# どれを設定すべきなんだろうか…

