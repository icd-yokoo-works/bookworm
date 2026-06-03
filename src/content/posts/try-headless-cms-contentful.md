---
title: ヘッドレスCMS contentful を試してみた
meta_title: Astroとcontentfulを使ったサイトを公開する方法
description: Astroとcontentfulで作成したページを公開する手順を説明します。
date: 2026-05-30
image: /images/posts/01.jpg
categories:
  - development
authors:
  - icd-yokoo
tags:
  - astro
  - github
  - microCMS
draft: false
---
こちらの記事では、AstroにヘッドレスCMSの一つ、Contentfulを組み込んだページの制作から公開までの手順を説明します。

## contentfulとは
[contentful](https://www.contentful.com) とは、ヘッドレスCMSのひとつ。2013年にドイツ、ベルリンで設立された会社のサービス。

今回はこちらのサービスとAstroをっ組み合わせてページを制作していきます。


## 1. 作業ファイルの設定

まずは保存先のフォルダに移動します。
こちらの[ページ](https://www.contentful.com/astro-starter/)を参考にし、Astroの作業ファイルの設定を行います。

vs codeのターミナルに
以下のコマンドを入力
```
npm create astro@latest -- --template contentful/starter-astro-bookshelf
```

今回はデスクトップのAstroフォルダ内に新しく`astro_contentful`フォルダを作りました。

```
~/Desktop/Astro/astro_contentfu
```


## 2. contentfulアカウントの作成
contentfulのアカウントを作成します。
githubのアカウントがあればそちらと連携してアカウント作成が可能です。


## 3API Keyの作成
アカウント作成が終わったら、API Keyを作成します。
画面右上の設定アイコン（歯車アイコン）からAPI Keysへ移動し作成

## 3. contentful のセットアップ
ターミナルに以下のコマンドを入力
```
npm run setup
``` 

メッセージに沿って、
```
? Enter you Contentful Space ID 
? Enter you Content Delivery API Key
? Enter you Content Management Token
```
- Space ID
- Content Delivery API - access token
を入力
3つ目にはCMA access tokenを入力するようにと指示が出るので、
画面右上の設定アイコン（歯車アイコン）からCMS Tokensへ移動し作成しコピペします。

一通り処理が終わったら、
```
npm run dev
```
と入力し、
ローカルサーサーバーを立ち上げて表示確認します。

Astrobrary
のページが表示されれば設定は完了です。

## 使ってみて
仕組みは分かったものの、最初にインストールしたbookshelfがあまりイケてないので、改めてインストールをやり直します。

contentfulとは関係ないが、obsidianをいれて、原稿（.mdファイル）を管理すれば快適になりそう。