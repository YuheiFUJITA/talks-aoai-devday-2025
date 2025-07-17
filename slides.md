---
# You can also start simply with 'default'
theme: seriph
# Force dark mode
colorSchema: 'dark'
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: 生成AIを活用したVS Codeによるこれからの開発体験
info: |
  このセッションでは、GitHub Copilotの登場からどのようにVS Codeが進化してきたのか、そしてこれからの開発体験がどのように変わっていくのかをお話します。
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# 生成AIを活用した<br>VS Codeによる<br>これからの開発体験

<div class="mt-8 space-y-2 text-lg">
  <div class="flex items-center justify-center space-x-2">
    <span>🎯</span>
    <span>AOAI Dev Day 2025</span>
    <a href="https://aoai-devday.com/" class="text-blue-500 hover:underline">aoai-devday.com</a>
  </div>
  <div class="flex items-center justify-center space-x-2">
    <span>📅</span>
    <span>2025-07-18</span>
  </div>
</div>

---
layout: center
class: text-center
---

<div class="text-6xl font-bold text-gradient bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 bg-clip-text text-transparent">
  このスライドは<br>Vibe Writingで<br>作成しました
</div>

---
layout: center
---

# 自己紹介

<div class="flex items-center justify-center space-x-8">
  <img src="http://github.com/YuheiFUJITA.png" alt="Yuhei FUJITA" class="w-32 h-32 rounded-full" />
  
  <div class="text-left space-y-4">
    <h2 class="text-2xl font-bold">Yuhei FUJITA（ふじた）</h2>
    <div class="space-y-2">
      <div class="flex items-center space-x-2">
        <span class="text-blue-500">🏃‍♂️</span>
        <span>運営: <a href="https://vscode.connpass.com/" class="text-blue-500 hover:underline">VS Code Meetup</a></span>
      </div>
      <div class="flex items-center space-x-2">
        <span class="text-blue-500">🐦</span>
        <span>X: <a href="https://x.com/Yuhei_FUJITA" class="text-blue-500 hover:underline">@Yuhei_FUJITA</a></span>
      </div>
    </div>
  </div>
</div>

---
layout: center
---

# VS Code Meetupとは

<div class="relative">

<div class="absolute top-0 right-0">
  <div class="flex flex-col items-center space-y-2">
    <img src="/connpass-vscode-meetup.png" alt="VS Code Meetup QR Code" class="w-32 h-32" />
    <div class="text-center text-sm text-gray-400">
      <div>VS Code Meetup</div>
      <div>Connpassページ</div>
    </div>
  </div>
</div>

<div class="grid grid-cols-2 gap-12 text-left pr-40">

<div class="space-y-6">

## 📋 概要
強力かつ軽量なオープンソースのコードエディター「Visual Studio Code」のミートアップです。

## 👥 コミュニティ規模
- メンバー数: **4,727人**
- 開催イベント: **58回**  
- 開催頻度: 月1回ペース

</div>

<div class="space-y-6">

## 🌐 活動チャンネル
- [Twitter (#vscodejp)](https://twitter.com/hashtag/vscodejp)
- [Discord](https://discord.gg/MG6wy7mjRk) - お悩み相談チャンネル
- [Facebook Group](https://www.facebook.com/groups/vscodemeetup) - 告知メイン
- [YouTube Channel](https://www.youtube.com/channel/UCFqnW6XfzhJXDZIl8soW-Gw) - 配信・アーカイブ

## 🎯 最近のトピック
- AI Coding（GitHub Copilot）
- VS Code Monthly Update

</div>

</div>

</div>

---
layout: center
class: text-center
---

# VS Codeのこれまでの歩み

<div class="text-4xl">⏳</div>

<div class="mt-8 text-xl text-gray-400">
コードエディターから統合開発環境へ、<br>
そしてAI時代の開発プラットフォームへ
</div>

---
layout: center
---

# VS Code 10年間の歩み

<div class="timeline-container mt-8">

<div class="grid grid-cols-3 gap-8 text-center">

<div class="space-y-4">
<div class="text-2xl font-bold text-blue-400">2015-2018</div>
<div class="text-lg font-semibold">基盤構築期</div>
<div class="space-y-2 text-sm">
<div>🎯 2015年4月: Build 2015で発表</div>
<div>🔧 2015年11月: 拡張機能システム</div>
<div>📈 市場シェア: 7% → 35%</div>
</div>
</div>

<div class="space-y-4">
<div class="text-2xl font-bold text-purple-400">2018-2022</div>
<div class="text-lg font-semibold">機能拡張期</div>
<div class="space-y-2 text-sm">
<div>🤝 2018年: Live Share</div>
<div>🌐 2019年: Remote Development</div>
<div>⚙️ 2020年: Settings Sync</div>
</div>
</div>

<div class="space-y-4">
<div class="text-2xl font-bold text-green-400">2022-2025</div>
<div class="text-lg font-semibold">AI統合期</div>
<div class="space-y-2 text-sm">
<div>🤖 2022年: GitHub Copilot</div>
<div>💬 2023年: Copilot Chat</div>
<div>📊 2024年: 市場シェア73.6%</div>
</div>
</div>

</div>

</div>

---
layout: two-cols
---

# 基盤構築期（2015-2018）

<div class="space-y-6">

## 🚀 技術的基盤の確立

**2015年4月29日 Microsoft Build**
- Electron + TypeScript + Monaco Editor
- クロスプラットフォーム対応
- 軽量でありながら高機能

## 🔧 拡張機能エコシステム

**2015年11月18日 Connect();**
- VS Code APIを拡張機能に開放
- 6か月で1,000以上の拡張機能
- オープンソース化（MITライセンス）

</div>

::right::

<div class="space-y-6">

## 📈 市場での急成長

<div class="bg-gray-800 p-4 rounded-lg">

**Stack Overflow Developer Survey**
- 2016年: **7%**（13位）
- 2017年: **22%**（5位）  
- 2018年: **35%**（🥇1位）

</div>

## 🎯 成功要因

- **オープンソース戦略**
- **拡張機能エコシステム**
- **継続的な機能改善**
- **コミュニティ重視**

</div>

---
layout: two-cols
---

# 機能拡張期（2018-2022）

<div class="space-y-4">

## 🌐 Remote Development（2019年）

**働き方を変えた技術革新**
- Remote SSH
- Remote Containers
- Remote WSL
- COVID-19時代の必須ツール

## 🤝 Live Share（2018年）

**リアルタイムコラボレーション**
- P2P接続による低遅延
- 共有デバッグセッション

</div>

::right::

<div class="space-y-4">

## ⚙️ Settings Sync（2020年）

**デバイス間の統一体験**
- 設定・拡張機能の同期
- スニペット・UI状態の同期
- 迅速な環境セットアップ

## 🔤 Language Server Protocol

**開発体験の標準化**
- エディターと言語サーバーの分離
- 複数エディターでの一貫サポート

</div>

---
layout: two-cols
---

# AI統合期（2022-2025）

<div class="space-y-6">

## 🤖 GitHub Copilot統合

**2022年: 開発体験の革命**
- リアルタイムコード補完
- 自然言語からコード生成
- 開発者の生産性向上

## 💬 GitHub Copilot Chat

**2023年: 対話型AI開発**
- 自然言語でのコード説明
- デバッグ支援
- 2023年12月一般提供開始

</div>

::right::

<div class="space-y-6">

## 🌐 Web版の進化

**vscode.dev**
- ブラウザで完全な開発環境
- GitHub Repositories統合
- デスクトップ版に匹敵する機能

## 📊 圧倒的な市場支配

**2024年現在**
- 市場シェア: **73.6%**
- 30,000以上の拡張機能
- 185カ国で利用

</div>

---
layout: center
---

# 市場シェアの変遷

<div class="flex justify-center mt-8">

<div class="space-y-8 text-center">

<div class="grid grid-cols-5 gap-8 items-end h-64">

<div class="flex flex-col items-center">
<div class="bg-blue-500 w-16 rounded-t" style="height: 20px;"></div>
<div class="mt-2 text-sm">2016</div>
<div class="text-xs text-gray-400">7%</div>
</div>

<div class="flex flex-col items-center">
<div class="bg-blue-500 w-16 rounded-t" style="height: 60px;"></div>
<div class="mt-2 text-sm">2017</div>
<div class="text-xs text-gray-400">22%</div>
</div>

<div class="flex flex-col items-center">
<div class="bg-blue-500 w-16 rounded-t" style="height: 100px;"></div>
<div class="mt-2 text-sm">2018</div>
<div class="text-xs text-gray-400">35%</div>
<div class="text-xs text-yellow-400">🥇1位</div>
</div>

<div class="flex flex-col items-center">
<div class="bg-blue-500 w-16 rounded-t" style="height: 160px;"></div>
<div class="mt-2 text-sm">2022</div>
<div class="text-xs text-gray-400">71%</div>
</div>

<div class="flex flex-col items-center">
<div class="bg-blue-500 w-16 rounded-t" style="height: 200px;"></div>
<div class="mt-2 text-sm">2024</div>
<div class="text-xs text-gray-400">73.6%</div>
</div>

</div>

<div class="text-lg text-gray-300">
Stack Overflow Developer Survey 結果
</div>

<div class="text-sm text-gray-400">
単純なエディタから開発プラットフォームへ：<br>
**10年間で10倍以上の成長**を遂げ、事実上の業界標準に
</div>

</div>

</div>

---
layout: center
class: text-center
---

# GitHub Copilotの登場

<div class="text-4xl">🤖</div>

<div class="mt-8 text-xl text-gray-400">
2022年、AIがコーディングに革命をもたらした
</div>

---
layout: two-cols
---

# GitHub Copilotの4段階進化

<div class="space-y-4">

## 🧪 実験期（2021-2022）
**2021年6月 技術プレビュー開始**
- OpenAI Codex基盤
- 受諾率: **27%**

## 💼 ビジネス統合期（2022-2023）
**2022年6月 個人向け一般提供開始**
- 個人向け: $10/月
**2023年2月 ビジネス向け一般提供開始**
- ビジネス向け: $19/月

</div>

::right::

<div class="space-y-4">

## 💬 チャット・企業機能期（2023-2024）
**2023年3月 GPT-4統合・Chat発表**
- Fill-In-the-Middle: 受諾率**35%**
- GitHub Copilot Chat発表（12月一般提供）

## 🤖 自律AI エージェント期（2024-2025）
**2024年〜 次世代AI開発**
- マルチモデル対応
- 開発者はCopilotが生成した文字の**88%**を保持

</div>

---
layout: center
---

# 技術的進歩の軌跡

<div class="grid grid-cols-2 gap-12 mt-8">

<div class="space-y-6">

## 🧠 AIモデルの進化

<div class="space-y-4">

**OpenAI Codex → GPT-4 → GPT-4o**
- **2021年**: 単純なプレフィックス補完
- **2023年**: 360度コンテキスト理解
- **2025年**: ほぼ瞬時の提案生成

**マルチモデル対応**
- Claude 3.5 Sonnet
- Google Gemini 1.5 Pro
- OpenAI o1シリーズ

</div>

</div>

<div class="space-y-6">

## 📊 パフォーマンス向上

<div class="bg-gray-800 p-4 rounded-lg space-y-3">

**コード品質**
- Java: **61%** 生成精度
- Python: **43%** 一発成功率
- **53.2%** 高いテスト合格率

**開発生産性**
- **55%** 高速なタスク完了
- **95%** 生産性向上報告
- **30%** 提案受諾率（平均）

</div>

</div>

</div>

---
layout: center
---

# 市場での圧倒的成功

<div class="grid grid-cols-3 gap-8 mt-8">

<div class="text-center space-y-4">
<div class="text-5xl font-bold text-blue-400">1.8M</div>
<div class="text-lg">有料サブスクライバー</div>
<div class="text-sm text-gray-400">2025年現在</div>
</div>

<div class="text-center space-y-4">
<div class="text-5xl font-bold text-purple-400">77K+</div>
<div class="text-lg">導入組織数</div>
<div class="text-sm text-gray-400">Fortune 500企業の1/3も導入</div>
</div>

<div class="text-center space-y-4">
<div class="text-5xl font-bold text-green-400">76%</div>
<div class="text-lg">開発者がAI活用</div>
<div class="text-sm text-gray-400">Stack Overflow 2024</div>
</div>

</div>

<div class="mt-12 space-y-4">

## 🏆 業界標準として確立

<div class="grid grid-cols-2 gap-8 text-left">

<div class="space-y-2">
<div>✅ **30+プログラミング言語**対応</div>
<div>✅ **主要IDE**すべてで利用可能</div>
<div>✅ **SOC 2 Type I**認定済み</div>
</div>

<div class="space-y-2">
<div>✅ **77+拡張機能**エコシステム</div>
<div>✅ **モバイル開発**完全対応</div>
<div>✅ **自律的なコーディングエージェント**</div>
</div>

</div>

</div>

---
layout: two-cols
---

# VS Codeとの完璧な統合

<div class="space-y-4">

## 🔧 開発体験の変革

**リアルタイム補完**
- インライン提案
- 複数候補表示
- コンテキスト理解

**GitHub Copilot Chat**
- 自然言語でのコード説明
- デバッグ支援
- 2023年12月一般提供開始

</div>

::right::

<div class="space-y-4">

## 🚀 次世代機能

**Copilot Workspace**
- タスク中心の開発環境
- ブレインストーミングから実装まで
- 技術プレビュー提供中

**自律的なAIエージェント**
- GitHubイシューの直接割り当て
- 自動プルリクエスト作成
- 反復的コード改善

</div>

---
layout: center
class: text-center
---

# VS Codeの進化にしがみつく方法

<div class="text-4xl">🚀</div>

<div class="mt-8 text-xl text-gray-400">
急速に進化するツールと技術についていくために
</div>
