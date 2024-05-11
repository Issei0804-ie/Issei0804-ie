---
title: "Syskan"
date: 2022-10-11T11:19:51+09:00
draft: false
---

うちの学科にはシステム管理チーム~~謎の組織~~があって、そこで学科サービスのメンテナンス、機能向上を行っていました。
僕が4年次のときのシステムは物理サーバーが9台あって、主にcephとkvm, podman を使ってサービス提供していた感じです。


それで、podmanが色々厳しいところがあって、k8sに移行する作業を行っている途中です。
例えば

- コンテナにIPアドレスを割り振る際、pingを飛ばして対象がいないことを確認して割り振っている
  + しかも結構めんどくさい
- 各物理サーバーで1台ずつほしいサービスを立ち上げる際、同じ作業を9回行う必要がある
- どこの物理サーバーで何のサービスを提供しているかわかりにくい
- podmanでコンテナを立ち上げるために物理サーバー上で作業することがメイン
  + 物理サーバー上の作業をやめたい
- 一部のサーバーに負荷が偏る
- デプロイ作業を絶妙にCI化できない

みたいな感じです。