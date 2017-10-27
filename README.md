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

### インデント
半角スペース2つ分でインデントする。
```HTML
<ul>
  <li>リスト1</li>
  <li>リスト2</li>
</ul>
```
```CSS
.item {
  color: red;
}
```

### コメントの書き方
HTMLでは、要素を子要素に持つ、
モジュールやセクションのあとにコメントを書く。
`<!-- /.class名 -->`
```HTML
<ul class="list">
  <li>リスト1</li>
  <li>リスト2</li>
  <li>リスト3</li>
</ul>
<!-- /.list -->
```
CSSも同じく
```SCSS
.list {
  color: red;
}
//.list
```

### カラーコード
HEX形式のカラーコードで省略できるものは省略する。
```css
//NG
p {
  color: #eebbcc;
}

//OK
p {
  color: #ebc;
}
```

## 命名規則


## HTMLルール


## CSSルール


## 対応ブラウザー


## 禁止事項
