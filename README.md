# コーディング規約

## 共通ルール

HTML, CSS, JavaScriptに共通するルール。

### 対応ブラウザ

- PC : Internet Explorer 10〜、Firefox最新バージョン、Google Chrome最新バージョン
- SP : Android 4.0〜、iOS Safari最新バージョン

### コメントの書式

コメントには`//`は使用しない。

```SCSS
/* ====================
--- > ブロック
==================== */

/* --------------------
- > エレメント
-------------------- */

// 状態変化など
```

### 画像ファイル

画像ファイルは種類に応じて下記に記す文言を接頭辞として、以降の文字列をアンダースコアで接続して命名する。

| 種類| 表記 |
|:---|:---|
| 写真 | img |
| ボタン | btn |
| アイコン | ico |
| テキスト | txt |
| バナー | bnr |
| 背景 | bg |
| ロゴ | logo |

例）btn_icon.svg

### ディレクトリ

| 種類| 表記 |
|:---|:---|
| 開発ディレクトリ | src |
| HTMLディレクトリ | src/html |
| SCSSディレクトリ | src/scss |
| images/css/js 格納ディレクトリ | src/static |
| CSSディレクトリ | src/static/css |
| 画像ディレクトリ | src/static/images |
| jsディレクトリ | src/static/js |
| 出力ディレクトリ | build |

## HTMLルール

- HTML5でのセマンティックマークアップ
- インデントは半スペ2で統一
- 各ブロックのあとに閉じコメントを書く
  - 例）`<!-- /.block -->`
- 不要な属性は省略する
  - NG)`<link rel="stylesheet" type="text/css" href="style.css">`
  - OK)`<link rel="stylesheet" href="style.css">`
- 要素毎に改行する

### 命名規則

- BEM
- Modifireに関しては、アクセシビリティを考慮してWAI-ARIAを使用する。
- Jsのトリガー要素には`js-`の接頭辞を使用する。
- レイアウト要素には`l-`の接頭辞を使用する。

```HTML
<nav class="nav">
  <ul class="nav__inner">
    <li class="nav__item">
      <a href="" aria-current="false">項目1</a>
    </li>
    <li class="nav__item">
      <a href="" aria-current="true">項目2</a>
    </li>
    <li class="nav__item">
      <a href="" aria-current="false">項目2</a>
    </li>
  </ul>
</nav>
<!-- /.nav -->
```

## CSSルール

- SCSS記法で書くこと
  - コンパイル形式は`expanded`を使用
- セレクタのネストは3階層で留める
- インデントは半スペ2で統一
- カラーコードは小文字でHEX値を使用
  - 不透明度を表現したい場合はRGBA値も使用可能
- モジュール間の余白は各モジュールに含め、全てbottomを指定
  - 上記では補えない余白が必要な場合は、別途marginクラスを設ける
  - `.l-margin {margin-bottom: 10px;}`,`.l-margin2 {margin-bottom: 20px;}`

### リセットCSS

このプロジェクトでは 「Eric Meyer’s “Reset CSS” 2.0」 を使用。

### ディレクトリ構造

```
scss
　├ base
    ├ variables
      ├ _color.scss
      ├ _family.scss
      ├ _size..scss
    ├ _mixin.scss
    ├ _reset.scss
    └ _base.scss
　├ layout
    ├ _header.scss
    ├ _footer.scss
    └ _grid.scss
　├ module
    ├ _nav.scss
    └ _logo.scss
　└ theme
    └ _top.scss
```

ディレクトリ          | 用途
------------------- | ---------------------------------- |
base                | ベースとなるスタイルやリセットCSSを格納。
base/variable       | 変数を格納。
layout              | レイアウトスタイルを格納。
module              | モジュールスタイルを格納。
theme               | テーマによって切り替える際のスタイルを格納。

## 禁止事項

- クラス名に見た目を反映しない
- HTML内にスタイルは記述しない

## コミットメッセージ

【ページ名】作業した内容 - 理由