---
title: Astroのセットアップ
meta_title: Astroでサイト構築するための環境構築手順をまとめました。
description: Astroでサイト構築するための環境構築手順をまとめました。
date: 2025-04-01
image: /images/posts/thumb-astronomy.png
categories:
  - development
authors:
  - icd-yokoo
tags:
  - astro
  - github
  - node
  - js
draft: false
---
こちらの記事では、static site generator **Astro**の開発手順をまとめます。


## Astroとは
AstroはJavaScriptベースの多機能で効率的な静的サイトジェネレーターのひとつです。

以下のサイトでは現在starの数も第6位となっており、開発者コミュニティから高い評価を受けています。

https://jamstack.org/generators/


### 公式サイト
https://astro.build/


## Astroの設定方法
※vs codeで作業をお行いますので、必ずインストールしておいてください。\
また、vs codeにAstroのエクステンションも入れておくとよいでしょう。


### 1. Node.jsのインストール
こちらからダウンロード

https://nodejs.org/ja



### 2. npm npxの確認

```
npm --version
npx --version
```

でバージョンを確認する。

以下のエラーが出る場合は実行ポリシーを変更する必要あり。

```
npm : このシステムではスクリプトの実行が無効になっているため、ファイル C:\Program Files\nodejs\npm.ps1 を読み込むことができません。詳細については、「about_Execution_
Policies」(https://go.microsoft.com/fwlink/?LinkID=135170) を参照してください。
```

### 参考サイト
https://ydk.vc/vscode-nodejs-scripts-about-execution-policies/
https://learn.microsoft.com/ja-jp/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.5
https://learn.microsoft.com/ja-jp/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.4

### 実行ポリシーを変更する

```
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```


## 3. Astroのセットアップ
作業ディレクトリを決め、ターミナルを起動
私の場合は

```
C:\Users\**USERE_NAME**\Desktop\Astro_test\astro
```
のディレクトリにしました。
`USER_NAME`や`Astro_test`、`astro`などは適宜変更してください。

ディレクトリを移動したら、
ターミナルに、以下のコマンドを入力

```
npm create astro@latest
```

これで初期設定完了です。
