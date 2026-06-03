---
title: Astroで作成したページをgithub pagesで公開する方法
meta_title: Astroで作成したページをgithub pagesで公開する方法
description: Astroで作成したページをgithub pagesで公開する手順を説明します。
date: 2026-06-02
image: /images/posts/thumb-github.png
categories:
  - development
authors:
  - icd-yokoo
tags:
  - astro
  - js
  - github
draft: false
---

こちらの記事では、Astroで制作したページ（blog）をGitHub pagesに公開する手順を説明します。

## GitHub pagesとは
> You can use GitHub Pages to host a website about yourself, \
> your organization, or your project directly from a repository on GitHub.


> GitHub Pagesはあなた自身やあなたの属する組織、プロジェクトのサイトを\
> GitHubのリポジトリから直接公開できるホスティングサービス。


[GitHub Pages](https://docs.github.com/ja/pages/getting-started-with-github-pages/what-is-github-pages) とは、GitHubリポジトリから直接静的サイトをホストすることができるサービスで、\
リポジトリを使ってサイトのコードやファイルを保存しておけば、GitHubが自動で公開してくれます。

GitHub Pagesを活用すれば、サイトを即座に立ち上げることができるため、\
ポートフォリオやオープンソースプロジェクト、その他の静的コンテンツを簡単に公開することができます。

今回はこちらのサービスを利用してAstroで作ったページを公開していきます。


## 1. リポジトリの作成

自身のGitHubアカウントにログインし、リポジトリを作成します。\
今回は`astro`という名前でリポジトリを作成しています。

このリポジトリに作成したファイルを上げていきます。


## 2. GitHub Actionsの作成
AstroサイトをGitHub Pagesに公開するには
[GitHub Actions](https://docs.astro.build/ja/guides/deploy/github/)の作成が必要になります。\
上記のリンク先を確認しながら、deploy.ymlファイルを作成します。


```
import { defineConfig } from 'astro/config'

export default defineConfig({
  site: 'https://450k.github.io',
  base: '/astro',
})
```
となります。


## 3. パスの調整
baseの設定を記述している場合、\
このまま公開を行うと、画像のパスなどがすべて切れてしまうため、\
画像のパス、リンクのパスをすべて変更する必要があります。

vs codeの一括置換などで、

```
<a href="/about">About</a>
↓↓↓ 
<a href="/450k/about">About</a>
``` 


```
<img src="/image/logo.svg">
↓↓↓
<a src="/450k/image/logo.svg">
```


```
<img src={/image/****}>
↓↓↓
<a src={/450k/image/****}>
```

などに変更してください。

```
npm run dev
```
でローカルサーバーを起動し、表示確認を行います。

## 4. GitHubのリポジトリへコミット

パスの変更が終わり、表確認もできたらmainブランチへコミットします。\
あとは自動的にGitHubが処理してくれますので、\
GitHub PagesのURLにアクセスして確認してください。