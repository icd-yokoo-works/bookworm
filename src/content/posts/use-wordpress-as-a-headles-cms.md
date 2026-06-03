---
title: wordpressをヘッドレスCMSとして使ってみる
meta_title: wordpressをヘッドレスCMSとして使ってみる
description: 今回はローカル環境でDockerを使いwordpressをヘッドレスCMSとしてBlogを制作してみました
date: 2026-06-01
image: /images/posts/05.jpg
categories:
  - development
authors:
  - icd-yokoo
tags:
  - astro
draft: false
---

今回はローカル環境でDockerを使いwordpressをヘッドレスCMSとしてBlogを制作してみました。個人的にはwordpressがあまり好きではないのですが、所属会社の担当が、やたらとwordpress推しで、サイトリニューアルはすべてwordpressで提案しているので、どうせなら、ヘッドレス化してNextとかで構築できたら面白いのではないかと思い、まずはローカルでテストしてみることにしました。



参考にさせていただいたのは[こちらの記事](https://owlcamp.jp/ceo-built-website-with-ai/)です。ローカルでも環境を作ってしまえば、簡単なのかもしれません。


### AIにお願いする

wordpressが嫌いな理由はPHP。ほとんど触れないので、コーディングの大半はAIにお願いします。Figmaで画面のイメージを作り、Figma MCPからcoursorに投げます。

20分ぐらいすると、テーマや管理画面の入力欄まで整えてくれます。
ただし、無料枠のクレジットを半分以上消費してしまいました。
