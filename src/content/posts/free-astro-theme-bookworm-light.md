---
title: Astroのblogテンプレート設定方法
meta_title: Astroのblogテンプレート設定方法
description: Astroの無料テーマ「bookworm」を使用してblogを作成します。
date: 2026-05-23
image: /images/posts/thumb-bookworm-light.png
categories:
  - development
authors:
  - icd-yokoo
tags:
  - astro
  - github
draft: false
---
こちらの記事では、Astroの無料テーマを使ってblogを構築する手順を説明します。


## テーマのダウンロード
[こちら](https://astro.build/themes/)のサイトから、お好きなテーマを選んでダウンロードします。

今回は、[bookworm-light-astro](https://github.com/themefisher/bookworm-light-astro.git)というテーマを使用します。

画面内の`Get Started` ボタンをクリックし、[Github](https://github.com/hasinhayder/storyteller-astro)のへ移動。

ファイルをcloneするか、ダウンロードします。\
※今回はzipファイルをダウンロードして進めていきます。

クローンする場合は
```
git clone https://github.com/themefisher/bookworm-light-astro.git
```

## ファイルを所定の位置へ移動（コピー）

ダウンロードしたファイルを、
Astroのフォルダにコピーします。

```
C:\Users\**USERE_NAME**\Desktop\Astro_test\astro
```

## テーマの初期設定
手順に沿って初期設定を行います。

bookwormのフォルダへ移動し、以下のコマンドを入力

```
npm install
```

続いて、

```
npm run dev
```
をたたくと、ローカルサーバーが立ち上がり、\
blogのトップページを確認することができます。

ひとまずこちらで、動作確認は終了。

あとは、適宜、ファイルを微調整していきます。