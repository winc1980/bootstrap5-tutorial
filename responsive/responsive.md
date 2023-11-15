# レスポンシブ

HTML だけでレスポンシブを実装します。

## ブレイクポイント

Bootstrap には便利なブレイクポイントの機能があります。今までメディアクエリを使ってブレイクポイントを設定していましたが、Bootstrap ではすでにその機能を実装しているため、クラスを指定するだけでよいです。これを使うことで HTML だけでレスポンシブなページを構築することが可能です。
6 種類のブレイクポイントがあり、padding や margin などの Spacing や、グリッドシステムの col など様々なクラスに使えます。
これさえマスターすればコーディングを効率化できるはずです。

|   xs   |   sm   |   md   |   lg   |   xl    |   xxl   |
| :----: | :----: | :----: | :----: | :-----: | :-----: |
| <576px | ≥576px | ≥768px | ≥992px | ≥1200px | ≥1400px |

> 実際使うのは、sm, md, lg くらいなのでそれ以外はとりあえず覚えなくてよいです。

## グリッドシステムのレスポンシブ

ブレイクポイントを使えば、グリッドの行と列を自由に変化させることが可能です。

例　 3 列の要素を、スマホサイズで 1 列にする

1. まず 3 列のグリッドを作成します

```html
<div class="row">
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
</div>
```

2. 次に、col に md のブレイクポイントを設定して、768px まで col を適用させるようにします

```html
<div class="row">
  <div class="col-md">col-md</div>
  <div class="col-md">col-md</div>
  <div class="col-md">col-md</div>
</div>
```

実際の動作は[index.html](./index.html)で確認できます。

### ブレイクポイントを使った FAQ ページをご紹介

[faq-page-demo.html](./faq-page-demo.html)にアクセスしてください。

## 様々な画面サイズで適切に余白を作るコンテナ

親要素はとりあえず Container を設置しておけ！ というくらいコンテナとても重要な Bootstrap の機能です。コンテナはデバイスの様々な画面サイズに対してレスポンシブに左右に余白を与え、要素を中心へ配置します。

以下の例ではコンテナの実装を示しています。[index.html](./index.html)で使用例を載せています。

例

```html
<div class="container">
  <div>ここがコンテナーの中身</div>
</div>
```

実際の動作を確認するには、[index.html](./index.html)を確認してください。

> コンテナの詳細については[公式ドキュメント](https://getbootstrap.jp/docs/5.3/layout/containers/)をご覧ください。
