# mypage

リンク集ページ（GitHub Pages で公開）。

## ファイル

| ファイル | 役割 |
|---|---|
| `index.html` | 公開ページ本体。単体で完結（外部依存なし） |
| `pin-tool.html` | PIN 暗号文の生成ツール。**公開しない**（`.gitignore` で除外） |

## リンクの編集

`index.html` の下部にある `const LINKS = [ ... ]` だけを編集する。
ブロックをコピーして貼り付ければ、いくつでもリンクを増やせる。

```js
{
  title: "表示名",
  url:   "https://example.com",
  icon:  "linkedin",   // linkedin / line / mail / x / github / note / link
  color: "#3182F6",
},
```

## PIN で保護されたリンク

`url` の代わりに `enc`（AES-256-GCM の暗号文）と `pin`（桁数）を持たせると、
PIN を入力しないと開けないリンクになる。URL はソースに平文で残らない。

PIN や URL を変更する手順:

1. `pin-tool.html` をブラウザで開く
2. URL と PIN を入力して「暗号文を作る」
3. 出力された文字列を `index.html` の `enc: "..."` に貼り替える
