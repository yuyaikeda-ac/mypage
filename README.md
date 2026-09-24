# mypage

リンク集ページ（GitHub Pages で公開）。スマートフォン閲覧を前提に作ってある。

## ファイル

| ファイル | 役割 |
|---|---|
| `index.html` | 公開ページ本体。単体で完結（外部依存なし） |
| `profilepig.jpeg` | プロフィール写真 |

## 編集する場所

`index.html` 下部の `<script>` 内、**「▼▼▼ 編集はこのブロックだけ ▼▼▼」から「▲▲▲」までの間**だけを触る。

### PROFILE — 名前・所属

```js
const PROFILE = {
  name:   "池田 悠耶",
  romaji: "Yuya Ikeda",
  meta: [ "…", "…" ],   // 名前の下に並ぶ行
};
```

### LINKS — リンクボタン

配列の順番がそのまま上からの並び順になる。

```js
{
  title: "researchmap",
  sub:   "研究業績",          // 小さい説明（省略可）
  url:   "https://researchmap.jp/yuyaikeda",
  icon:  "researchmap",      // researchmap / link
  color: "#0F6E62",
},
```

## 見た目の方針

白地・罫線・文字だけで構成する。影・グラデーション・アニメーションは使わない。
色はリンク色（`--accent`）と各リンクのアイコン色だけに限定する。
