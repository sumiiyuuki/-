# コーディング規約

## ディレクトリ構造
```
root
　├ build
　├ node_modules
　├ src
　│　└ html
　│　　　└ common
　└ gulpfile.js
``` 

## フォーマット

### メタルール

#### -- ドキュメントタイプ
HTML5でのマークアップ
```HTML
<!DOCTYPE html>
```

#### -- 文字エンコード
UTF-8を使用
```HTML
<meta charset="utf-8">
```

#### -- 属性
html5に於いて省略できる属性は記述しない
```HTML
<!-- NG -->
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<link rel="stylesheet" type="text/css" href="style.css"/>

<!-- OK -->
<meta charset=utf-8">
<link rel="stylesheet" href="style.css">
```

### 基本的な書式
- インデント
  - 半角スペース2つ分でインデントする。
- コメントの書き方
  - HTMLでは、要素を子要素に持つ、一番外側のモジュールやセクションのあとにコメントを書く。
- カラーコード
  - HEX形式のカラーコードでRGB形式にできるものはRGB形式で記述する。

```HTML
<div class="media">
  <div class="media-thumb">
    <img src="" alt="">
  </div>
  <!-- /.media-thumb -->
  
  <div class="media-profile">
    <p>名前</p>
    <p>テキスト</p>
  </div>
  <!-- /.media-profile -->
</div>
<!-- /.media -->
```

```CSS
.media {
  //NG
  color: #eebbcc;
  
  //OK
  color: #ebc;
}
```

## 命名規則
基本的にはBEMを使用。
WAI-AREAを使用できる場面では、modifireの代わりにaria属性を使用する。
```HTML
<nav class="gnav">
  <ul class="gnav__inner">
    <li class="gnav__item">
      <a href="/" aria-cuurent="false">HOME</a>
     </li>
    <li class="gnav__item">
      <a href="/" aria-cuurent="true">ABOUT</a>
    </li>
    <li class="gnav__item">
      <a href="/" aria-cuurent="false">WORKS</a>
    </li>
  </ul>
</nav>
<!-- /.gnav -->
```

## HTMLルール


## CSSルール


## 対応ブラウザー


## 禁止事項
