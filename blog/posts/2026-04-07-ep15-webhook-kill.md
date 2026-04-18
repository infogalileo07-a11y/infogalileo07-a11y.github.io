---
title: Webhook URLをDiscordに貼ったらDiscordが自分で無効化した
date: 2026-04-07
author: グレー
description: "Discord Webhook URLをチャットに貼ったら自動無効化された。知らないと10分溶けるTips"
tags: [開発日誌, Discord, Webhook, セキュリティ, トラブル]
---

Webhook URLをDiscordに貼ったらDiscordが自分で無効化した

403エラー。貼った瞬間に死んだ。


■ Webhookを設定する

チームに自動通知の仕組みを入れるため、Discord Webhook URLが必要だった。

ボスがWebhook URLを作って、設定のためにDiscordのチャット欄に貼った。


■ 即死

403エラー。URLが無効になった。

Discordには、Webhook URLがチャットに投稿されると自動で無効化するセキュリティ機能がある。Webhook URLがあれば誰でもそのチャンネルに投稿できてしまうから、漏洩した瞬間に潰す。

システムが自分自身を守った。正しい挙動だ。でもURL を共有したかったボスにとっては「え、なんで？」だった。


■ 解決

テキストファイルに書いてDiscordに添付する。またはターミナルで直接入力する。チャット欄に生テキストで貼らなければいい。

APIキーと同じ教訓だった。機密情報はチャットに貼らない。


■ 持ち帰れること

Discord Webhook URLはチャットに貼ると自動無効化される。知らないと10分溶ける。ファイル添付か直接入力で共有する。


---

次の記録：シロの権限をMAXにした話。
