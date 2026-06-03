---
title: 国産ヘッドレスCMS Niltoを試してみた
meta_title: 国産ヘッドレスCMS Niltoを試してみた
description: 国産ヘッドレスCMS Niltoを試してみたみました。contentfulやmicroCMSとの違いも紹介します。
date: 2026-05-30
image: /images/posts/04.jpg
categories:
  - development
authors:
  - icd-yokoo
tags:
  - astro
draft: false
---

今回は国産のヘッドレスCMS Niltoのご紹介。国産となると候補はかなり絞られますがNiltoは選択肢の1つとして名前が挙がることも多いかと思います。

### Sleipnirを作ったフェンリルが開発

Niltoはフェンリル株式会社が提供するSaaS型のヘッドレスCMS（コンテンツ管理システム）です。Webサイトやアプリの自由なデザインと快適なテキスト編集を実現し、最近ではAIエージェントと連携して入稿作業やコンテンツ運用を自動化する機能なども搭載されています。

H2O spaceのたにぐちまことさんも[こちらの記事](https://www.nilto.com/ja/interview/makoto-taniguchi-headless-cms)で紹介されていますが、以前、Astroの講座を視聴した際はmicroCMSを使っていたような記憶が・・・ いろいろと大人の事情がありそうです。

### Niltoを選んだわけ
なぜNiltoを選んだのかですが、Reactを使ったのテストサイトでmicroCMSを使ってしまっていた。というのが大きな理由です。（無料枠がもう空いていなかった）そこで、今回は、Niltoを使用してみました。

そのほかに、contentfulとDocker環境でwordpressをヘッドレス化して使用するテストも行いました。これらは別記事でも紹介しています。

### 実際に使ってみて
microCMSの使い勝手に慣れてしまうと、Niltoは少し面倒というか、クリック数や画面遷移が多いような感覚です。もちろん、優れている機能もあるのですが、編集のしやすさ、確認しやすさはmicroCMSの方が使い勝手は良かった。