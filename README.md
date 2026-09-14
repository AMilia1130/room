# よるぱぱ｜紹介したもの

楽天ROOM（[@yorupapa_night](https://room.rakuten.co.jp/yorupapa_night/items)）で
紹介した商品を、日付ごとにまとめた静的サイトです。

Instagram のプロフィールに貼るリンク先として使います。
Instagram はフィード本文のリンクが踏めないため、
「さっき見た商品」に最短で辿り着ける場所として置いています。

同時に、Instagram Graph API の Content Publishing に渡す
**画像の公開URL** もここから配信します（API は画像のバイト列ではなく公開URLを要求するため）。

## 更新のしかた

このフォルダは手で編集しません。本体側で生成し直します。

```powershell
cd ..            # room-auto のプロジェクト
room-auto site   # site/ を作り直す
cd site
git add -A && git commit -m "更新" && git push
```

## 中身

```
index.html        トップ（Instagramのプロフィールに貼るURL）
<日付>/index.html その日に紹介した商品
<日付>/img/       商品カード画像
.nojekyll         GitHub Pages に Jekyll 処理をさせない
```

本ページはアフィリエイトリンクを含みます（PR）。
