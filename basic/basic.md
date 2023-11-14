# 1. Boostrapの基本

Bootstrapの基本では、Bootstrapでよく使う機能を抜粋して説明します。今回ご紹介する機能だけ知っていればBootstrapのマスターになれます。

## Bootstrapの仕組み

BootstrapはHTMLにクラス名を付けることでスタイルを決めていきます。  
中身が分からず使うのはモヤモヤするので簡単にBootstrapの仕組みについて説明します。

今まで私たちは、一からCSSのクラスを作成し、コーディングを行ってきました。しかし、Bootstrapでは、bootstrap.min.cssというCSSファイルを使い、あらかじめ独自のクラスが定義されているので、私たちはその定義されたクラスをただ使うだけでいいのです。

以下の例では、余白クラスの`.mb-5`を使って、p要素に対し下側に広く余白を適用しています。HTML要素に`.mb-5`を追加することで使えます。

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

このようにBootstrapがあらかじめ定義しているクラスを使うことでスタイルを適用します。  
> 余白以外にも様々な機能があるので[公式ドキュメント](https://getbootstrap.jp/docs/5.3/getting-started/introduction/)をご覧ください。

## デザイン必要なし、便利なコンポーネント機能

Bootstrapには、[ボタン](https://getbootstrap.jp/docs/5.3/components/buttons)、[ナビゲーションバー](https://getbootstrap.jp/docs/5.3/components/navbar/)、[フォーム](https://getbootstrap.jp/docs/5.3/forms/form-control/)、[アラート](https://getbootstrap.jp/docs/5.3/components/alerts/)など、多くの事前にスタイルされたコンポーネントが用意されています。簡単なHTMLを記述するだけですぐに実装可能です。  
コンポーネントの簡単な例を[index.html](./index.html)でご紹介していますのでご覧ください。

## グリッドシステム

グリッドシステムを使うとCSSのGridを簡単に実装することが可能です。グリッドは、containerとrowを使用して作成し、colクラスを使ってページを行と列に分割します。

1行3列の行列を作るグリッドの例。 [index.html](./index.html)で確認できます。

```html
<div class=row>
  <div class="col">1</div>
  <div class="col">2</div>
  <div class="col">3</div>
</div>
```

グリッドのサイズも`col-*`に1~12のサイズを入れることで簡単に指定できます。最大サイズの`col-12`を指定すると横幅が100%になります。

3/12のサイズを2つ、12/12のサイズを1つ指定した例。

```html
<div class="row">
  <div class="col-3">col-3</div>
  <div class="col-3">col-3</div>
  <div class="col-12">col-12</div>
</div>
```

> グリッドシステムの詳細については[公式ドキュメント](https://getbootstrap.jp/docs/5.3/layout/grid/)をご覧ください。
