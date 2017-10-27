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

## 命名規則
基本的にはBEMを使用。
WAI-AREAを使用できる場面では、modifireの代わりにaria属性を使用する。


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
  - 半角スペース2つ分でインデントする
- コメントの書き方
  - HTMLでは、要素を子要素に持つ、一番外側のモジュールやセクションのあとにコメントを書く
- カラーコード
  - HEX形式のカラーコードでRGB形式にできるものはRGB形式で記述する
- ショートハンドプロパティ
  - 可能な限りショートハンドプロパティで記述する
- 入れ子は3階層まで

```HTML
<div class="media">
  <div class="media__thumb">
    <img src="" alt="">
  </div>
  <!-- /.media__thumb -->
  
  <div class="media__profile">
    <p class="media__name">名前</p>
    <p class="media__txt">テキスト</p>
  </div>
  <!-- /.media__profile -->
</div>
<!-- /.media -->
```

```SCSS
/*----------
NG
----------*/
.media {
  background-image: url(path);
  background-repeat: no-repeat;
  background-position: top left;
  
  &__profile {
    width: 500px;
  }
  
  &__name {
    color: #eebbcc;
    font-size: 18px;
  }
}
```
```SCSS
/*----------
OK
----------*/
.media {
  background: url(path) no-repeat top left;
  
  &__profile {
    width: 500px;
  }
  
  &__name {
    color: #ebc;
    font-size: 18px;
  }
}
//.media
```

## HTMLルール


## CSSルール


## 対応ブラウザー


## 禁止事項
