# 1. Boostrap の基本

Bootstrap の基本では、Bootstrap でよく使う機能を抜粋して説明します。今回ご紹介する機能だけ知っていれば Bootstrap のマスターになれます。

## Bootstrap の仕組み

Bootstrap は HTML にクラス名を付けることでスタイルを決めていきます。  
中身が分からず使うのはモヤモヤするので簡単に Bootstrap の仕組みについて説明します。

今まで私たちは、一から CSS のクラスを作成し、コーディングを行ってきました。しかし、Bootstrap では、bootstrap.min.css という CSS ファイルを使い、あらかじめ独自のクラスが定義されているので、私たちはその定義されたクラスをただ使うだけでいいのです。

以下の例では、余白クラスの`.mb-5`を使って、p 要素に対し下側に広く余白を適用しています。HTML 要素に`.mb-5`を追加することで使えます。

```html
<p class="mb-5">下に余白を付けます</p>
```

```css
/* Bootstrap 組み込みクラス */
...
.mb-3 {
  margin-bottom: 1rem;
}
.mb-4 {
  margin-bottom: 1rem * 1.5;
}
.mb-5 {
  margin-bottom: 1rem * 3;
}
...
```

このように Bootstrap があらかじめ定義しているクラスを使うことでスタイルを適用します。

> 余白以外にも様々な機能があるので[公式ドキュメント](https://getbootstrap.jp/docs/5.3/getting-started/introduction/)をご覧ください。

## デザイン必要なし、便利なコンポーネント機能

Bootstrap には、[ボタン](https://getbootstrap.jp/docs/5.3/components/buttons)、[ナビゲーションバー](https://getbootstrap.jp/docs/5.3/components/navbar/)、[フォーム](https://getbootstrap.jp/docs/5.3/forms/form-control/)、[アラート](https://getbootstrap.jp/docs/5.3/components/alerts/)など、多くの事前にスタイルされたコンポーネントが用意されています。簡単な HTML を記述するだけですぐに実装可能です。  
コンポーネントの簡単な例を[index.html](./index.html)でご紹介していますのでご覧ください。

## ユーティリティ

ウェブ制作をする上で一般的に扱う CSS についても Bootstrap で実装されています。例えば、フォントサイズは以下のように指定可能です。

例　フォントサイズ

```html
<p class="fs-1">h1のフォントサイズを指定</p>
<p class="fs-2">h2のフォントサイズを指定</p>
```

例　太文字

```html
<p class="fw-bold">太くなります</p>
```

> 詳細は[公式ドキュメント]()

## グリッドシステム

グリッドシステムを使うと CSS の Grid を簡単に実装することが可能です。グリッドは、container と row を使用して作成し、col クラスを使ってページを行と列に分割します。

例　 1 行 3 列の行列を作るグリッド。 [index.html](./index.html)で確認できます。

```html
<div class="row">
  <div class="col">1</div>
  <div class="col">2</div>
  <div class="col">3</div>
</div>
```

グリッドのサイズも`col-*`に 1~12 のサイズを入れることで簡単に指定できます。最大サイズの`col-12`を指定すると横幅が 100%になります。

![](https://miro.medium.com/v2/resize:fit:4800/format:webp/0*z2Lkt066SfPxfWqM.png)
出典：[Medium, Replicate Bootstrap 3 Grid Using CSS Grid](https://medium.com/@mobomo/replicate-bootstrap-3-grid-using-css-grid-624c1088b0bc)

例　 3/12 のサイズを 2 つ、12/12 のサイズを 1 つ指定

```html
<div class="row">
  <div class="col-3">col-3</div>
  <div class="col-3">col-3</div>
  <div class="col-12">col-12</div>
</div>
```

> グリッドシステムの詳細については[公式ドキュメント](https://getbootstrap.jp/docs/5.3/layout/grid/)をご覧ください。
