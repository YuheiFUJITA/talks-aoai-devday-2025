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

<!--
今日は貴重なお時間をいただき、ありがとうございます。私はふじたと申します。
本日は「生成AIを活用したVS Codeによるこれからの開発体験」というテーマでお話しさせていただきます。

VS Codeは2015年の登場から現在まで、開発者ツールの概念を根本的に変革してきました。
特に2022年のGitHub Copilot統合以降、AIを活用した開発体験が劇的に向上しています。

今日は以下の点についてお話しします：
- VS Codeのこれまでの10年間の歩み
- GitHub Copilotの登場と進化
- これからの開発体験がどう変わっていくか
- この急速な進化についていく方法

それでは始めさせていただきます。
-->

---
layout: center
class: text-center
---

<div class="text-6xl font-bold text-gradient bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 bg-clip-text text-transparent">
  このスライドは<br>Vibe Writingで<br>作成しました
</div>

<!--
実は、このプレゼンテーションのスライドは、VS CodeのAI機能の一つである「Vibe Writing」を使って作成しました。

Vibe Writingは、GitHub Copilotの機能の一つで、自然言語の指示から構造化されたコンテンツを生成してくれます。
今回のスライドも、「AOAI Dev Day用のVS Code AI開発体験についてのプレゼンを作って」という指示から、
このようなMarkdown形式のスライドを自動生成してもらいました。

これは今日お話しする「AIを活用した開発体験」の実例でもあります。
単なるコード補完を超えて、ドキュメント作成やプレゼンテーション作成まで、
AIが開発者の様々な作業を支援してくれる時代になったということを象徴しています。
-->

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

<!--
まず簡単に自己紹介をさせていただきます。
ふじたと申します。VS Code Meetupという勉強会を運営しています。

VS Code Meetupは、VS Codeユーザーのためのコミュニティです。
現在4,727人のメンバーがいて、これまで58回のイベントを開催してきました。
月1回のペースで開催していて、最近はAI CodingやGitHub Copilotの話題が多いです。

TwitterやDiscord、YouTubeなど様々なチャンネルで活動しています。
特にDiscordではお悩み相談チャンネルがあって、VS Codeの使い方やトラブルシューティングなど、
メンバー同士で助け合っています。

私自身も長年VS Codeを使い続けていて、その進化を間近で見てきました。
特にGitHub Copilotの登場以降の変化は本当に劇的で、
今日はその体験も含めてお話しできればと思います。
-->

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

<!--
それでは本題に入らせていただきます。
まず、VS Codeのこれまでの歩みを振り返ってみましょう。

VS Codeは2015年の登場から現在まで、開発者ツールの概念を根本的に変革してきました。
この10年間で、単純なコードエディターから統合開発環境へ、
そして現在はAI時代の開発プラットフォームへと進化しています。

この進化は3つの大きな転換点によって特徴づけられます：
1. 拡張機能エコシステムの確立（2015-2018年）
2. リモート開発環境の革新（2018-2022年）  
3. AI統合による開発体験の変革（2022-2025年）

市場シェアで見ると、2016年の7%から2024年の73.6%まで、
10倍以上の成長を遂げています。

それぞれの時代を詳しく見ていきましょう。
-->

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

<!--
VS Codeの10年間の歩みを3つの時期に分けて見ていきます。

**基盤構築期（2015-2018）**
2015年4月のBuild 2015での発表から始まりました。
Electron、TypeScript、Monaco Editorという技術スタックの選択が成功の鍵でした。
2015年11月には拡張機能システムを導入し、6か月で1,000以上の拡張機能が生まれました。
市場シェアは7%から35%まで急上昇し、2018年には1位になりました。

**機能拡張期（2018-2022）**  
この時期は開発者の働き方を変える機能が次々と登場しました。
2018年のLive Share、2019年のRemote Development、2020年のSettings Syncなど、
コラボレーションとリモートワークを支える技術が確立されました。

**AI統合期（2022-2025）**
2022年のGitHub Copilot統合で開発体験が革命的に変わりました。
2023年のCopilot Chat、そして現在は自律的なコーディングエージェントまで登場しています。
市場シェアは73.6%に達し、事実上の業界標準となっています。

この進化の過程を詳しく見ていきましょう。
--></div>

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

<!--
基盤構築期は、VS Codeの成功の土台を築いた重要な時期です。

**技術的基盤の確立**
2015年4月29日のMicrosoft Buildでの発表は、開発者ツールの転換点となりました。
Electron、TypeScript、Monaco Editorという技術スタックの選択が成功の鍵でした。

Electronの採用により、Windows、macOS、Linuxでの統一された開発体験を実現しました。
当時はAtom Shellとして知られていた技術ですが、この選択がクロスプラットフォーム戦略を可能にしました。

**拡張機能エコシステムの革新**
2015年11月18日のConnect();での拡張機能システム導入が最も重要な戦略的決定でした。
VS Code自体と同じAPIを拡張機能開発者に提供することで、
6か月という短期間で1,000以上の拡張機能が生まれました。

同時にオープンソース化も行われ、MITライセンスで公開されました。
これにより、個人開発者から企業まで幅広い採用が可能になりました。

**市場での急成長**
この戦略により、Stack Overflow Developer Surveyでの採用率は劇的に向上しました。
2016年の7%（13位）から、わずか2年で2018年には35%（1位）まで成長しました。
-->

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

<!--
機能拡張期は、開発者の働き方を根本的に変える機能が次々と登場した時期です。

**Remote Development（2019年）**
2019年5月のRemote Development Extension Pack正式リリースは、開発者の働き方を変革しました。
Remote SSH、Remote Containers、Remote WSLの3つの機能により、場所に依存しない開発環境を実現しました。

特にCOVID-19パンデミック期間中、この機能は開発者コミュニティにとって不可欠なツールとなりました。
VS Code Serverがリモートマシンに自動インストールされ、ローカル品質の開発体験を提供します。

**Live Share（2018年）**
2018年5月の正式リリースにより、リアルタイムコード共有が可能になりました。
P2P接続による低遅延通信、セキュアなセッション管理、共有デバッグセッションにより、
ペアプログラミングとリモートチームのコラボレーションを革新しました。

**Settings Sync（2020年）**
2020年7月のSettings Sync正式リリースは、開発者の複数デバイス間での一貫した体験を実現しました。
設定、キーボードショートカット、拡張機能、スニペット、UI状態の同期により、
新しい環境での迅速なセットアップが可能になりました。

**Language Server Protocol**
LSPバージョン3.0の標準化により、エディタと言語サーバーの分離を実現しました。
これにより、複数エディタでの一貫したサポートが可能になりました。
-->

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

<!--
AI統合期は、開発体験を革命的に変えた時期です。

**GitHub Copilot統合（2022年）**
2022年のGitHub Copilot統合は、開発者の作業方法を根本的に変革しました。
リアルタイムコード補完から始まり、自然言語からのコード生成が可能になりました。
開発者の生産性は大幅に向上し、55%高速なタスク完了が報告されています。

**GitHub Copilot Chat（2023年）**
2023年のGitHub Copilot Chat機能により、対話型AI開発が現実になりました。
自然言語でのコード説明、デバッグ支援が可能になり、
2023年12月の一般提供開始で多くの開発者が利用できるようになりました。

**Web版の進化**
vscode.devの進化により、ブラウザでの完全な開発環境アクセスが実現しました。
GitHub Repositories統合により、直接的なリポジトリ編集が可能になり、
デスクトップ版に匹敵する機能をブラウザで提供できるようになりました。

**圧倒的な市場支配**
2024年現在、VS Codeは73.6%という圧倒的な市場シェアを獲得しています。
30,000以上の拡張機能を擁し、185カ国で利用される真にグローバルなツールです。
事実上の開発者ツールの標準となっています。
-->

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

<!--
このグラフは、VS Codeの驚異的な成長を視覚的に示しています。

Stack Overflow Developer Surveyの結果から見ると、
2016年にはわずか7%（13位）だった採用率が、
2024年には73.6%まで成長しています。

特に注目すべきは2018年に1位になった点です。
これは拡張機能エコシステムの成功とオープンソース戦略の成果です。

2022年から2024年にかけての成長は、AI統合による効果が大きく影響しています。
GitHub Copilotの統合により、単なるエディタから開発プラットフォームへと進化しました。

この10年間で10倍以上の成長を遂げ、
現在では事実上の業界標準としての地位を確立しています。

65,000人以上の開発者が回答したこの調査は、
VS Codeがいかに開発者コミュニティに受け入れられているかを物語っています。
-->

---
layout: center
class: text-center
---

# GitHub Copilotの登場

<div class="text-4xl">🤖</div>

<div class="mt-8 text-xl text-gray-400">
2022年、AIがコーディングに革命をもたらした
</div>

<!--
ここから、VS Codeの進化における最も重要な転換点の一つ、
GitHub Copilotの登場についてお話しします。

2022年、GitHub Copilotの正式統合により、
AIがコーディングに革命をもたらしました。

これは単なる機能追加ではなく、
開発者の作業方法そのものを根本的に変える出来事でした。

GitHub Copilotは、OpenAIのCodexモデルを基盤として、
リアルタイムでコードを提案してくれる画期的なツールです。

自然言語のコメントから完全なコードを生成したり、
関数の始まりから残りの実装を予測したり、
これまで不可能だった開発体験を実現しました。

この登場により、VS Codeは単なるコードエディタから、
AI統合開発プラットフォームへと進化したのです。

その進化の過程を詳しく見ていきましょう。
-->

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

<!--
GitHub Copilotの進化を4つの段階に分けて見てみましょう。

**実験期（2021-2022）**
2021年6月の技術プレビュー開始から始まりました。
OpenAI Codexを基盤として、受諾率は27%でした。
この時期は招待制で限られた開発者のみが利用できました。

**ビジネス統合期（2022-2023）**
2022年6月に個人向けが月額10ドルで一般提供開始されました。
2023年2月にはビジネス向けも月額19ドルで提供開始され、
企業での本格的な導入が始まりました。

**チャット・企業機能期（2023-2024）**
2023年3月にGPT-4統合とCopilot Chatが発表されました。
Fill-In-the-Middle技術により受諾率が35%まで向上しました。
12月にはCopilot Chatが一般提供開始され、対話型AI開発が現実になりました。

**自律AI エージェント期（2024-2025）**
2024年以降、次世代AI開発が始まりました。
マルチモデル対応により、様々なAIモデルを選択できるようになりました。
現在では開発者がCopilotが生成した文字の88%を保持しており、
AIの提案がいかに有用かを示しています。

この進化により、単なるコード補完ツールから、
自律的な開発パートナーへと変貌を遂げています。
-->

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

<!--
GitHub Copilotの技術的進歩は本当に目覚ましいものがあります。

**AIモデルの進化**
最初はOpenAI Codexから始まり、GPT-4、そして現在のGPT-4oまで進化しました。
2021年の単純なプレフィックス補完から、
2023年には360度コンテキスト理解が可能になり、
2025年現在ではほぼ瞬時の提案生成が実現されています。

さらに素晴らしいのは、マルチモデル対応です。
Claude 3.5 Sonnet、Google Gemini 1.5 Pro、OpenAI o1シリーズなど、
様々なAIモデルから最適なものを選択できるようになりました。

**パフォーマンス向上**
コード品質も大幅に向上しています。
Javaでは61%の生成精度、Pythonでは43%の一発成功率を実現しています。
53.2%という高いテスト合格率は、AIが生成するコードの品質の高さを物語っています。

開発生産性の面では、55%高速なタスク完了、
95%の開発者が生産性向上を報告しています。
提案受諾率も平均30%と、実用性の高さを示しています。

これらの数字は、AIがもはや実験的なツールではなく、
実践的な開発パートナーとなったことを証明しています。
-->

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

<!--
GitHub Copilotの市場での成功は圧倒的です。

**驚異的な利用者数**
2025年現在、1.8百万人の有料サブスクライバーを抱えています。
77,000以上の組織が導入しており、Fortune 500企業の3分の1も導入しています。
Stack Overflow 2024の調査では、76%の開発者がAIを活用していると回答しています。

**業界標準としての確立**
30以上のプログラミング言語に対応し、主要なIDEすべてで利用可能です。
SOC 2 Type I認定も取得済みで、企業での安全な利用が保証されています。

77以上の拡張機能エコシステムを持ち、モバイル開発にも完全対応しています。
最近では自律的なコーディングエージェント機能も追加され、
単なるコード補完を超えた包括的な開発支援ツールとなっています。

これらの数字は、GitHub Copilotがもはや実験的なツールではなく、
開発者にとって必須のツールとして確立されたことを示しています。

AI活用は今や開発者にとって標準的なワークフローの一部となっています。
-->

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

<!--
VS CodeとGitHub Copilotの統合は本当に完璧です。

**開発体験の変革**
リアルタイム補完機能では、コードを書いている最中にインライン提案が表示され、
複数の候補から選択できます。コンテキストを理解した提案で、
まるで経験豊富な開発者がペアプログラミングしてくれているようです。

GitHub Copilot Chatは2023年12月の一般提供開始以降、多くの開発者が愛用しています。
自然言語でのコード説明やデバッグ支援により、
複雑な問題の解決が格段に楽になりました。

**次世代機能**
Copilot Workspaceは現在技術プレビュー提供中ですが、
タスク中心の開発環境を提供し、ブレインストーミングから実装まで
一貫したAI支援を受けることができます。

最も注目すべきは自律的なAIエージェント機能です。
GitHubイシューを直接AIエージェントに割り当てることができ、
自動でプルリクエストを作成し、反復的にコードを改善してくれます。

これはもはや単なるツールではなく、
AIパートナーとの共同開発という新しい開発体験を提供しています。
-->

---
layout: center
class: text-center
---

# GitHub Copilotによるこれからの開発体験

<div class="text-4xl">🚀</div>

<div class="mt-8 text-xl text-gray-400">
AIと共に進化する開発の未来
</div>

<!--
最後に、GitHub Copilotによるこれからの開発体験についてお話しします。

私たちは今、開発の歴史における重要な転換点にいます。
GitHub CopilotとVS Codeの統合により、AIが単なるツールから開発パートナーへと進化しました。

**自律的な開発エージェントの時代**
近い将来、AIエージェントが要件定義からテスト、デプロイまでの全工程を支援するようになります。
開発者の役割は、コードを書くことから、AIと協働して最適なソリューションを設計することへとシフトしていきます。

**創造性とイノベーションの解放**
繰り返し作業やボイラープレートコードの生成がAIに任されることで、
開発者はより創造的で戦略的な課題に集中できるようになります。

**学習と成長の新しい形**
AIペアプログラミングにより、ベテラン開発者の知見を瞬時に活用できるようになり、
学習サイクルが劇的に短縮されます。

この変化の波に乗り遅れないよう、ぜひ積極的にGitHub Copilotを活用してみてください。
未来の開発体験を、今すぐ体験することができます。

ご清聴ありがとうございました。
-->

---
layout: center
---

# GitHub Copilotによる3つのコーディング方法

<div class="grid grid-cols-3 gap-8 mt-12">

<div class="text-center space-y-6">
<div class="text-6xl">⚡</div>
<h2 class="text-2xl font-bold text-blue-400">Code Completion</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>リアルタイム補完</div>
<div>インライン提案</div>
<div>コンテキスト理解</div>
</div>
</div>

<div class="text-center space-y-6">
<div class="text-6xl">💬</div>
<h2 class="text-2xl font-bold text-purple-400">Agent Mode</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>対話型開発</div>
<div>自然言語指示</div>
<div>コード生成・解説</div>
</div>
</div>

<div class="text-center space-y-6">
<div class="text-6xl">🤖</div>
<h2 class="text-2xl font-bold text-green-400">coding agent</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>自律的コーディング</div>
<div>タスク実行</div>
<div>プルリクエスト作成</div>
</div>
</div>

</div>

<div class="mt-12 text-center text-lg text-gray-400">
それぞれの方法で、開発者の生産性とコード品質を向上
</div>

<!--
GitHub Copilotによる3つのコーディング方法についてご紹介します。

**Code Completion（コード補完）**
これは最も基本的で広く使われている機能です。
コードを書いている最中にリアルタイムでインライン提案を表示し、
コンテキストを理解した適切な補完を提供します。
タブキーを押すだけで提案を受け入れることができ、
開発速度を大幅に向上させます。

**Agent Mode（エージェントモード）**
GitHub Copilot Chatを使った対話型開発方法です。
自然言語で指示を出すことで、コードの生成や解説を行ってくれます。
「この関数をリファクタリングして」「このエラーを修正して」といった
具体的な指示により、より複雑な開発タスクを支援してくれます。

**coding agent（コーディングエージェント）**
最も高度な機能で、自律的にコーディングを行います。
GitHubイシューを直接エージェントに割り当てることで、
要件を理解し、コードを書き、テストを実行し、
プルリクエストまで自動で作成してくれます。

これら3つの方法を適切に使い分けることで、
開発者の生産性とコード品質を大幅に向上させることができます。
それぞれの特徴を理解し、場面に応じて最適な方法を選択することが重要です。
-->

---
layout: center
---

# Code Completion

<div class="flex justify-center mt-8">
  <video 
    src="https://code.visualstudio.com/assets/docs/copilot/inline-suggestions/nes-video.mp4" 
    controls 
    class="w-4/5 h-auto rounded-lg shadow-lg"
    autoplay
    loop
    muted
  >
    お使いのブラウザではビデオがサポートされていません。
  </video>
</div>

<div class="mt-8 text-center">
  <div class="text-sm text-gray-400">
    引用元: <a href="https://code.visualstudio.com/docs/copilot/ai-powered-suggestions#_next-edit-suggestions" class="text-blue-400 hover:underline">VS Code Documentation - AI-powered suggestions</a>
  </div>
</div>

<!--
このビデオでは、GitHub CopilotのCode Completion機能の実際の動作をご覧いただけます。

**リアルタイム補完の威力**
開発者がコードを書いている最中に、Copilotがリアルタイムでコードの続きを提案している様子が分かります。
グレーテキストで表示される提案は、コンテキストを完全に理解した適切なコードです。

**インライン提案の自然さ**
提案されるコードは、まるで経験豊富な開発者が隣でペアプログラミングしてくれているような自然さです。
変数名、関数名、ロジックの流れまで、すべてがコンテキストに適合しています。

**開発速度の向上**
タブキーを押すだけで提案を受け入れることができ、
従来の開発と比べて大幅な時間短縮を実現できます。

**学習効果**
AIの提案を見ることで、新しいアプローチや書き方を学ぶことができ、
開発者としてのスキル向上にも寄与します。

この機能により、繰り返し作業から解放され、
より創造的で戦略的な開発業務に集中できるようになります。
-->

---
layout: center
---

# Agent Mode

<div class="flex justify-center mt-8">
  <video 
    src="https://videos.ctfassets.net/8aevphvgewt8/5R57iyx96ENtWp4nOHBsAl/f935b264e79099bd8ed54e2d74db7ab5/hero-animation-lg.mp4" 
    controls 
    class="w-4/5 h-auto rounded-lg shadow-lg"
    autoplay
    loop
    muted
  >
    お使いのブラウザではビデオがサポートされていません。
  </video>
</div>

<div class="mt-8 text-center">
  <div class="text-sm text-gray-400">
    引用元: <a href="https://github.com/features/copilot" class="text-blue-400 hover:underline">GitHub Copilot Features</a>
  </div>
</div>

<!--
このビデオでは、GitHub CopilotのAgent Mode機能の実際の動作をご覧いただけます。

**対話型開発の革新**
チャットインターフェースを通じて自然言語で指示を出し、Copilotが理解してコードを生成している様子が分かります。
「このAPIを使ったファイルアップロード機能を作って」といった具体的なリクエストに対して、
適切なコード実装を提供してくれます。

**コンテキスト理解の深さ**
単純なコード生成だけでなく、プロジェクト全体の構造や既存のコードスタイルを理解して、
一貫性のある実装を提案してくれます。
エラーハンドリングやベストプラクティスも考慮した高品質なコードを生成します。

**反復的な改善プロセス**
最初の提案が完璧でなくても、「もう少しエラーハンドリングを詳しく」「TypeScriptで書き直して」といった
追加の指示により、段階的にコードを改善していくことができます。

**学習とメンタリング効果**
生成されたコードの説明も同時に提供されるため、
なぜそのような実装になったのかを理解でき、開発者のスキル向上にも寄与します。

Agent Modeにより、従来のStackOverflowやドキュメント検索に頼っていた調査時間を大幅に短縮し、
より効率的な開発フローを実現できます。
-->

---
layout: center
---

# coding agent

<div class="flex justify-center mt-8">
  <video 
    src="https://videos.ctfassets.net/8aevphvgewt8/oRsODfD5AIRds44zu51uQ/ad3028c1286fd523188cf482b542caba/features-breakout-coding-agent.mp4" 
    controls 
    class="w-4/5 h-auto rounded-lg shadow-lg"
    autoplay
    loop
    muted
  >
    お使いのブラウザではビデオがサポートされていません。
  </video>
</div>

<div class="mt-8 text-center">
  <div class="text-sm text-gray-400">
    引用元: <a href="https://github.com/features/copilot" class="text-blue-400 hover:underline">GitHub Copilot Features</a>
  </div>
</div>

<!--
このビデオでは、GitHub Copilotのcoding agent機能の実際の動作をご覧いただけます。

**自律的なコーディングの実現**
GitHubイシューを直接AIエージェントに割り当てることで、
要件を理解し、計画を立て、コードを実装し、テストまで自動で行っている様子が分かります。
従来の開発者が行っていた一連の作業をAIが代行してくれます。

**包括的なタスク実行**
単なるコード生成を超えて、ファイル作成、依存関係の管理、テストの実行、
さらにはプルリクエストの作成まで、開発ワークフロー全体を自動化します。
まさに「AIペア開発者」としての役割を果たしています。

**反復的な改善プロセス**
最初の実装でエラーが発生した場合、自動的にエラーを検出し、修正を試みます。
テストが失敗すれば、テストが通るまで何度でもコードを調整してくれます。
人間の開発者と同様の問題解決アプローチを取ります。

**レビューと承認フロー**
重要な変更については、人間の開発者による確認とレビューを経てからマージされます。
AIが提案する変更内容を適切に評価し、承認プロセスを経ることで品質を保証します。

coding agentにより、開発者はより戦略的で創造的な作業に集中でき、
繰り返し作業や定型的なタスクはAIに任せることができるようになります。
これは開発チームの生産性を飛躍的に向上させる革新的な機能です。
-->

---
---

# 神アプデ

<div class="flex gap-8 mt-8">
  <div class="w-3/5">
    <Tweet id="1943454185426686442" />
    <div class="mt-4 text-center">
      <div class="text-sm text-gray-400">
        GitHub Japan 公式アカウントより
      </div>
    </div>
  </div>
  
  <div class="w-2/5 space-y-4">
    <h2 class="text-xl font-bold mb-4">かつてあった恐怖体験</h2>
    <div class="space-y-2">
      <img src="/horror-video.gif" alt="Horror Video" class="w-full rounded-lg shadow-lg" />
      <img src="/horror-picture.png" alt="Horror Picture" class="w-full rounded-lg shadow-lg" />
    </div>
    <div class="text-left text-sm text-gray-400 mt-4">
      <div>GItHub Copilot Pro+を契約した僕の覚悟を</div>
      <div>返してください</div>
      <img src="/github.com_settings_billing.png" alt="GitHub Billing Settings" class="w-full mt-2 shadow-lg" />
    </div>
  </div>
</div>

<!--
GitHub Japanの公式アカウントから投稿された最新のアップデート情報をご紹介します。

このツイートでは、GitHub Copilotの最新機能や改善点について言及されており、
日本の開発者コミュニティに向けた重要な情報が含まれています。

**最新の機能強化**
継続的にアップデートされるGitHub Copilotの機能により、
開発者の生産性はさらに向上し続けています。

**日本語サポートの充実**
日本語でのコメントや変数名にも対応し、
日本の開発者にとってより使いやすいツールとなっています。

**コミュニティとの連携**
GitHub Japanチームは、日本の開発者コミュニティの声を積極的に収集し、
プロダクトの改善に反映させています。

このような継続的な改善により、GitHub CopilotとVS Codeの組み合わせは、
これからも開発体験を革新し続けることでしょう。
-->

---
layout: center
class: text-center
---

# GitHub Copilot Chat<br>オープンソース化の衝撃

<div class="text-4xl">📖</div>

<div class="mt-8 text-xl text-gray-400">
2025年5月19日、業界に激震が走った
</div>

<!--
2025年5月19日、MicrosoftがGitHub Copilot ChatをMITライセンスでオープンソース化すると発表しました。
これは、AI開発ツール市場における透明性向上と競争力強化を目的とした戦略的な転換点となりました。

1,500万人のユーザーを抱えるCopilotサービスの中核機能をオープンソース化することで、
VS Codeの市場支配的地位を維持しながら、開発者コミュニティとの信頼関係を強化する狙いがあります。

この動きは、単なる技術的な決定ではなく、CursorやWindsurfなどの競合AI搭載エディタの急成長に対する
直接的な対抗策として位置付けられています。

LLMの性能向上により「秘密のプロンプト戦略」の価値が低下した今、
Microsoftは透明性を武器に、VS Codeを中心とした開発者エコシステムの支配的地位を
確固たるものにしようとしています。
-->

---
layout: two-cols
---

# オープンソース化の経緯

<div class="space-y-6">

## 📅 発表から公開までの流れ

**Microsoft Build 2025**
- 段階的なオープンソース化計画を発表
- 「今後数週間以内に」との約束

**2025年6月30日**
- **GitHub Copilot Chat拡張機能**正式公開
- **MITライセンス**で提供開始

</div>

::right::

<div class="space-y-6">

## 🎯 発表の背景

**競合他社の急成長**
- **Cursor**: 90億ドルの評価
- **Windsurf**: OpenAI買収検討（30億ドル）

**開発者コミュニティからの要求**
- 透明性向上への圧力
- Proposed APIs制限への不満

</div>

<!--
GitHub Copilot Chatのオープンソース化は、戦略的な判断に基づく重要な決定でした。

**発表から公開までの流れ**
Microsoft Build 2025において、VS Codeチームは段階的なオープンソース化計画を発表しました。
「今後数週間以内に」という約束通り、6月30日にGitHub Copilot Chat拡張機能が
MITライセンスで正式に公開されました。

この迅速な対応は、Microsoftの本気度を示すものでした。

**発表の背景には強力な圧力**
VS Codeのフォークとして成功したCursorが90億ドルの評価を受け、
WindsurfがOpenAIによる30億ドルでの買収検討を受けるなど、
競合他社の急成長がありました。

また、拡張機能開発者からの「Proposed APIs」へのアクセス制限に対する不満も高まっていました。
開発者コミュニティは、より透明性の高い開発環境を求めていたのです。

主要なテック系メディアは概ね好意的な反応を示し、
RedditやHacker Newsでは透明性向上への評価が相次ぎました。
-->

---
layout: center
---

# 戦略的意図とビジネス目標

<div class="grid grid-cols-3 gap-8 mt-8">

<div class="text-center space-y-4">
<div class="text-5xl">🏆</div>
<h3 class="text-xl font-bold text-blue-400">市場支配力の維持</h3>
<div class="text-sm text-gray-300">
<div>VS Code市場シェア: 73.6%</div>
<div>「AI-native editor」への進化</div>
<div>競合他社との差別化</div>
</div>
</div>

<div class="text-center space-y-4">
<div class="text-5xl">💰</div>
<h3 class="text-xl font-bold text-purple-400">収益事業の拡大</h3>
<div class="text-sm text-gray-300">
<div>年間20億ドルの収益創出</div>
<div>GitHub収益成長の40%以上</div>
<div>企業導入の促進</div>
</div>
</div>

<div class="text-center space-y-4">
<div class="text-5xl">🤝</div>
<h3 class="text-xl font-bold text-green-400">パートナーシップ多様化</h3>
<div class="text-sm text-gray-300">
<div>OpenAI依存度の軽減</div>
<div>Anthropic、Google連携</div>
<div>戦略的多様化の推進</div>
</div>
</div>

</div>

<div class="mt-8 text-center text-lg text-gray-400">
**三つの戦略的目標を同時に達成する巧妙な戦略**
</div>

<!--
Microsoftのオープンソース化決定は、三つの戦略的目標を同時に達成する巧妙な戦略です。

**市場支配力の維持・強化**
既に開発者の73.6%が使用するVS Codeを「AI-native editor」へと進化させることで、
競合他社との差別化を図っています。
オープンソース化により、開発者コミュニティの信頼を獲得し、
さらなる市場シェア拡大を狙っています。

**収益事業の更なる拡大**
年間20億ドルの収益を創出するGitHub Copilot事業は、
GitHubの収益成長の40%以上を占める重要事業です。
透明性向上を通じた信頼性構築により、企業での導入促進を狙っています。

**パートナーシップの戦略的多様化**
13億ドルの投資先であるOpenAIに対する依存度を軽減し、
Anthropic、Google、Azureなど複数のAIプロバイダーとの連携を強化する
戦略的多様化を進めています。

競合他社への圧力も重要な要素です。
オープンソース化により、競合他社が独自機能開発に投資していたリソースを、
オープンソース標準への対応に振り向けることを強制し、
VS Code生態系に開発者を引き戻す効果を狙っています。
-->

---
layout: two-cols
---

# 技術的詳細と公開範囲

<div class="space-y-6">

## ✅ オープンソース化された機能

**中核機能の公開**
- **Agent Mode**: 自動化マルチステップタスク
- **Edit Mode**: 対話的コード編集
- **Chat Integration**: エディター内AI会話
- **システムプロンプト**: 透明性の確保
- **テレメトリ収集**: データ収集の可視化

</div>

::right::

<div class="space-y-6">

## ❌ 制限事項と依存関係

**非公開部分**
- **AIモデル本体**: OpenAI Codex/GPT等
- **バックエンドサービス**: クラウドインフラ
- **プロプライエタリAPI**: 独自APIエンドポイント

**利用条件**
- **有効なCopilotサブスクリプション**が必要
- **Microsoft/OpenAIクラウド**への依存継続

</div>

<!--
GitHub Copilot Chatのオープンソース化では、中核機能が公開される一方で、
重要な制限事項も存在します。

**オープンソース化された機能**
Agent Mode、Edit Mode、Chat Integration、システムプロンプト、テレメトリ収集など、
GitHub Copilot Chatの中核機能が公開されました。

Agent Modeでは自動化されたマルチステップコーディングタスクの実行が可能で、
Edit Modeでは対話的なコード編集、Chat Integrationではエディター内でのAI会話機能を提供します。

特に重要なのは、システムプロンプトとテレメトリ収集の透明化です。
これにより、AIがどのような指示で動作し、どのようなデータが収集されているかが明確になりました。

**制限事項と依存関係**
ただし、完全な自立運用は不可能です。
OpenAI CodexやGPT等のAIモデル本体、バックエンドサービス、プロプライエタリAPIは
依然として非公開です。

利用には有効なCopilotサブスクリプションが必要で、
Microsoft/OpenAIのクラウドサービスへの依存は継続します。

MIT Licenseの採用により、商用利用、修正・配布、プライベート利用が許可される一方、
著作権表示とライセンス条項の保持が義務付けられています。
-->

---
layout: center
---

# 実用的な活用方法

<div class="grid grid-cols-3 gap-8 mt-8">

<div class="space-y-4">
<div class="text-4xl text-center">🔍</div>
<h3 class="text-lg font-bold text-blue-400">コード監査・学習</h3>
<div class="text-sm text-gray-300 space-y-2">
<div>• システムプロンプトの研究</div>
<div>• AI動作メカニズムの理解</div>
<div>• セキュリティ監査の実施</div>
<div>• ベストプラクティスの学習</div>
</div>
</div>

<div class="space-y-4">
<div class="text-4xl text-center">⚙️</div>
<h3 class="text-lg font-bold text-purple-400">カスタマイズ・拡張</h3>
<div class="text-sm text-gray-300 space-y-2">
<div>• 企業固有要件への対応</div>
<div>• プライベートデプロイメント</div>
<div>• **Ollama**等ローカルAI統合</div>
<div>• 独自機能の追加開発</div>
</div>
</div>

<div class="space-y-4">
<div class="text-4xl text-center">🚀</div>
<h3 class="text-lg font-bold text-green-400">開発・コントリビューション</h3>
<div class="text-sm text-gray-300 space-y-2">
<div>• バグ修正への貢献</div>
<div>• 新機能の提案・実装</div>
<div>• 国際化・ローカライゼーション</div>
<div>• パフォーマンス最適化</div>
</div>
</div>

</div>

<div class="mt-8 text-center">
<div class="bg-gray-800 p-4 rounded-lg">
<div class="text-sm text-gray-400">
GitHubリポジトリ: <a href="https://github.com/microsoft/vscode-copilot-chat" class="text-blue-400 hover:underline">microsoft/vscode-copilot-chat</a><br>
詳細なドキュメント、アーキテクチャガイド、コントリビューションガイドを提供
</div>
</div>
</div>

<!--
GitHub Copilot Chatのオープンソース化により、開発者は三つの形で実用的な活用が可能になりました。

**コード監査・学習**
システムプロンプトの研究により、AIがどのような指示で動作しているかを理解できます。
AI動作メカニズムの透明化により、セキュリティ監査の実施や、
ベストプラクティスの学習が可能になりました。

これは特に企業での導入検討において重要で、
AIがどのようにコードを生成し、どのようなデータを扱っているかを
詳細に検証できるようになりました。

**カスタマイズ・拡張**
企業固有の要件に合わせた修正や、プライベートデプロイメントの実現が可能です。
特に注目すべきは、Ollama等のローカルAIモデルとの統合です。

これにより、クラウドサービスに依存しない、
完全にオンプレミスでのAI開発環境を構築することができるようになります。

**開発・コントリビューション**
バグ修正への貢献、新機能の提案・実装、国際化・ローカライゼーション、
パフォーマンス最適化など、様々な形でプロジェクトに貢献できます。

GitHubリポジトリ「microsoft/vscode-copilot-chat」では、
詳細なドキュメント、アーキテクチャガイド、コントリビューションガイドが提供されており、
開発者が容易に参加できる環境が整備されています。
-->

---
layout: two-cols
---

# 業界への広範囲な影響

<div class="space-y-6">

## 📈 開発者生産性の劇的向上

**実証された効果**
- **55%** のタスク完了時間短縮
- **85%** がコード品質向上を体験
- Pull Request作成: **9.6日→2.4日**
- **67%** が週5日以上使用

## 🏢 企業導入の加速

**導入実績**
- **20,000+** 組織が導入済み
- **100万+** アクティブユーザー
- Fortune 500企業の**1/3**が採用

</div>

::right::

<div class="space-y-6">

## ⚔️ 競合への深刻な影響

**既存プレイヤー**
- **Amazon CodeWhisperer**
- **Tabnine**
- 差別化戦略の見直しが急務

**新興プレイヤー**
- **Cursor**（月額20ドル）
- **Windsurf**（月額15ドル）
- vs **Copilot**（月額10ドル）

## 💰 価格競争の激化

現在のプレミアム料金体系の見直しが必要

</div>

<!--
GitHub Copilot Chatのオープンソース化は、業界全体に広範囲な影響を与えています。

**開発者生産性の劇的向上**
実証されたデータが示すように、開発者の生産性は劇的に向上しています。
55%のタスク完了時間短縮、85%がコード品質向上を体験しており、
Pull Request作成時間は9.6日から2.4日に短縮されました。

67%の開発者が週5日以上Copilotを使用しているという事実は、
もはやAIが開発者の日常業務に不可欠なツールとなったことを示しています。

**企業導入の加速**
20,000以上の組織が既にGitHub Copilotを採用し、
100万人以上の開発者がアクティブユーザーとなっています。
Fortune 500企業の3分の1が採用済みという事実は、
企業レベルでのAI導入が本格化していることを物語っています。

**競合他社への深刻な影響**
Amazon CodeWhispererやTabnineなどの既存プレイヤーは、
差別化戦略の見直しを迫られています。

新興のCursorやWindsurfは独自性の強化が必要となっており、
価格競争も激化しています。
現在のプレミアム料金体系（Cursor月額20ドル、Windsurf月額15ドル vs Copilot月額10ドル）の
変化も予想されます。

オープンソース化により、競合他社は更なる競争圧力にさらされることになります。
-->

---
layout: center
---

# 長期的展望と未来戦略

<div class="space-y-8">

<div class="grid grid-cols-2 gap-12">

<div class="space-y-6">

## 🔄 技術ロードマップ

**数ヶ月以内**
- **インライン補完機能**の統合
- VS Codeコア本体への統合

**2025年第3四半期**
- **10M+トークンコンテキスト**
- 全コードベース単一プロンプト解析

</div>

<div class="space-y-6">

## 📊 市場規模の拡大予測

**急成長する市場**
- **2024年**: 67億ドル
- **2030年**: 257億ドル
- 年率**25.2%**の成長率

**経済的インパクト**
- **1.5兆ドル**のGDP押し上げ効果

</div>

</div>

<div class="mt-8 bg-gray-800 p-6 rounded-lg">

## 🚀 技術進化の方向性

<div class="grid grid-cols-3 gap-6 text-center">

<div>
<div class="text-2xl mb-2">🔗</div>
<div class="text-sm">**Model Context Protocol**</div>
<div class="text-xs text-gray-400">標準化の推進</div>
</div>

<div>
<div class="text-2xl mb-2">🤖</div>
<div class="text-sm">**マルチエージェント**</div>
<div class="text-xs text-gray-400">システム協調</div>
</div>

<div>
<div class="text-2xl mb-2">🎤</div>
<div class="text-sm">**リアルタイム音声**</div>
<div class="text-xs text-gray-400">対応強化</div>
</div>

</div>

</div>

</div>

<!--
GitHub Copilot Chatのオープンソース化は、長期的な技術発展の礎となります。

**技術ロードマップ**
数ヶ月以内にインライン補完機能も統合され、
続いてVS Codeコア本体への統合が予定されています。
これにより、VS Codeは真のオープンソースAIエディターとして進化する計画です。

2025年第3四半期までには、10M+トークンコンテキストにより、
全コードベースを単一プロンプトで解析可能になる予定です。
これは開発者の理解力を飛躍的に向上させる画期的な進歩です。

**市場規模の拡大**
AI開発ツール市場は急速に拡大しており、
2024年の67億ドルから2030年には257億ドルに成長する予測です。
年率25.2%の成長率を維持し、経済的インパクトは1.5兆ドルのGDP押し上げ効果が期待されます。

**技術進化の方向性**
Model Context Protocol（MCP）による標準化、マルチエージェントシステム、
リアルタイム音声対応などが重要な発展方向です。

これらの技術により、2030年頃には70%のルーチンコード自動化が実現し、
開発者はより創造的な作業に集中できるようになると予想されます。

AI開発ツールが標準的な開発環境として完全に定着し、
ソフトウェア開発業界全体のパラダイムシフトが完了することが予想されます。
-->

---
layout: center
---

# 結論：透明性革命の始まり

<div class="space-y-8 mt-8">

<div class="text-center">
<div class="text-4xl mb-4">🌟</div>
<h2 class="text-2xl font-bold text-gradient bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 bg-clip-text text-transparent">
GitHub Copilot Chatのオープンソース化は<br>AI開発ツール市場における透明性革命の始まり
</h2>
</div>

<div class="grid grid-cols-2 gap-12">

<div class="space-y-4">

## ✅ 短期的成果

- **開発者コミュニティの信頼獲得**
- **競合他社への圧力**
- **技術的透明性の向上**
- **70%のルーチンコード自動化**

</div>

<div class="space-y-4">

## ⚠️ 新たな課題

- **技術的負債リスク**
- **セキュリティ懸念**
- **人材育成方針の見直し**
- **基礎スキルの重要性変化**

</div>

</div>

<div class="mt-8 text-center bg-gray-800 p-6 rounded-lg">
<div class="text-lg text-gray-300">
2030年頃には、AI開発ツールが標準的な開発環境として完全に定着し、<br>
ソフトウェア開発業界全体の<strong class="text-blue-400">パラダイムシフトが完了</strong>する見込み
</div>
</div>

</div>

<!--
GitHub Copilot Chatのオープンソース化は、AI開発ツール市場における透明性革命の始まりです。

**戦略的成功の要因**
Microsoftは短期的な競争優位を犠牲にしながらも、
長期的には業界標準を自ら設定し、VS Codeを中心とした開発者エコシステムの
支配的地位を強化する戦略を展開しています。

この決定は、開発者コミュニティの信頼獲得、競合他社への圧力、
技術的透明性の向上という三つの目標を同時に達成する巧妙な戦略です。

**実現される変革**
今後の展開により、70%のルーチンコード自動化が実現し、
開発者はより創造的な作業に集中できるようになります。

**新たな課題への対応**
一方で、技術的負債リスクやセキュリティ懸念、人材育成方針の見直しなど、
新たな課題も浮上しています。
オープンソース化は万能薬ではなく、品質管理と長期保守性の確保、
基礎的なコーディングスキルの重要性変化への対応が求められます。

**業界全体のパラダイムシフト**
2030年頃には、AI開発ツールが標準的な開発環境として完全に定着し、
ソフトウェア開発業界全体のパラダイムシフトが完了することが予想されます。

GitHub Copilot Chatのオープンソース化は、その変革プロセスの重要な里程標として、
今後長期間にわたって業界の発展を牽引していくでしょう。
-->

---
layout: center
class: text-center
---

# 詳細なDebug Logが確認できるように

<div class="flex justify-center mt-8">
  <img src="/developer-show-chat-debug-view.png" alt="GitHub Copilot Chat Debug Log - panel/editAgent詳細ログ" class="w-4/5 max-w-4xl rounded-lg shadow-lg" />
</div>

<div class="mt-6 text-center text-xs text-gray-400 opacity-70">
  （しれっとNESのログも見れたりします）
</div>

<!--
このスクリーンショットは、GitHub Copilot Chatのオープンソース化により実現された
透明性の具体例を示しています。

**表示されている詳細情報**
- panel/editAgent（84f74080）の内部処理
- ChatCompletions APIの詳細なメタデータ
- Claude Sonnet 3.5モデルの使用状況
- リクエスト/レスポンスの完全なJSON構造
- ファイルパスやワークスペース情報
- プロンプトトークンの詳細情報

**オープンソース化前との違い**
これまでブラックボックスだった内部処理が、このように詳細に可視化されるようになりました。
開発者は以下のことが可能になります：

- **トラブルシューティング**: エラーの原因を詳細に特定
- **パフォーマンス分析**: トークン使用量や処理時間の最適化
- **セキュリティ監査**: 送信されるデータの完全な把握
- **カスタマイズ開発**: 内部構造を理解した拡張機能開発

**開発者コミュニティへの影響**
この透明性は、AI開発ツール業界の新しいスタンダードを示しており、
競合他社も同様の透明性を提供せざるを得なくなっています。

Microsoftの戦略的判断により、VS Codeエコシステムの信頼性と
開発者エクスペリエンスが大幅に向上しました。
-->

---
layout: center
class: text-center
---

# VS CodeやGitHub Copilotの進化を追い続けるために

<div class="text-4xl">📚</div>

<div class="mt-8 text-xl text-gray-400">
継続的学習と情報収集のための実践的アプローチ
</div>

<!--
ここからは、VS CodeやGitHub Copilotの進化を追い続けるための
具体的な方法についてお話しします。

技術の進歩が急速な現在、新機能や更新に常にキャッチアップしていくことは
開発者にとって重要でありながらも挑戦的な課題です。

特にAI統合により変化のスピードが加速している今、
効率的で持続可能な学習方法を確立することが必要です。

このセクションでは、以下の観点から実践的なアプローチをご紹介します：
1. 公式情報源の活用方法
2. コミュニティとの連携
3. 継続的な実践と実験
4. 学習リソースの選択と活用

これらの方法を組み合わせることで、
技術の変化に遅れることなく、常に最新の開発体験を活用できるようになります。
-->

---
layout: two-cols
---

# VS Code Insidersを使う

<img src="/no-stable-yes-insiders.png" alt="VS Code StableはNO、VS Code InsidersはYES" class="w-full max-w-sm mx-auto rounded-lg shadow-lg" />

::right::

## Insidersを使うメリット

🚀 **最新機能の先行体験**  
安定版より3-4週間早く新機能を試せる

🤖 **GitHub Copilotの最新AI機能**  
新しいAI機能をいち早く体験

🔧 **フィードバックでコミュニティ貢献**  
バグ報告や改善提案で開発に参加

⚡ **安定版との並行利用**  
設定やデータが完全に分離され安全

<!--
VS Code Insidersは、最新機能をいち早く体験できる開発者向けの貴重な情報源です。

**VS Code Insiders の特徴**
VS Code Insidersは毎日自動ビルドされ、リリースされる開発版です。
安定版より3-4週間早く新機能を体験できるため、
今後リリースされる機能を事前に把握し、準備することが可能です。

GitHub Copilotの最新機能も、多くの場合Insiders版で先行利用できます。
これにより、AI機能の進化をいち早く体験し、
実際のワークフローに組み込む準備ができます。

**並行利用の利点**
Stable版とInsiders版は完全に独立しており、
設定やデータが分離されているため、両方を安全に利用できます。
本格的な開発にはStable版、新機能の実験にはInsiders版という
使い分けが可能です。

**導入と活用**
code.visualstudio.com/insidersから簡単にダウンロードでき、
Windows、macOS、Linuxすべてに対応しています。
既存のStable版との共存も問題ありません。

新機能の事前検証、拡張機能の互換性確認、
さらにはフィードバックによるコミュニティ貢献も可能です。

ただし、バグが含まれる可能性があるため、
本番環境での使用は避け、定期的なバックアップを心がけることが重要です。
-->

---
layout: center
---

# VS CodeのGitHub Repositoryをチェックする

<div class="grid grid-cols-3 gap-8 mt-12">

<div class="text-center space-y-4">
<div class="text-6xl">🔍</div>
<h2 class="text-xl font-bold text-blue-400">重要なポイント</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>• Issues & Discussions</div>
<div>• 新機能の提案</div>
<div>• バグレポート</div>
<div>• コミュニティの要望</div>
</div>
</div>

<div class="text-center space-y-4">
<div class="text-6xl">⚙️</div>
<h2 class="text-xl font-bold text-purple-400">効率的な使い方</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>• `label:endgame-plan`をチェック</div>
<div>• `next`ブランチをチェック</div>
</div>
</div>

<div class="text-center space-y-4">
<div class="text-6xl">🚀</div>
<h2 class="text-xl font-bold text-green-400">実践・活用</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>• リポジトリをWatch</div>
<div>• IssueをSubscribe</div>
<div>• Pull Requestsの確認</div>
<div>• Releaseページの監視</div>
</div>
</div>

</div>

<div class="mt-12 bg-gray-800 p-4 rounded-lg">
<div class="text-center text-sm text-gray-400">
GitHubリポジトリ: <a href="https://github.com/microsoft/vscode" class="text-blue-400 hover:underline">microsoft/vscode</a><br>
詳細なドキュメント、開発状況、コミュニティディスカッションを提供
</div>
</div>

<!--
VS CodeのGitHub Repositoryは、開発の最前線を知るための最も重要な情報源です。

**何をチェックするか**
IssuesとDiscussionsでは、新機能の提案や議論、バグレポートの動向、
コミュニティからの要望を把握できます。
これにより、VS Codeの将来的な方向性を理解することができます。

Pull Requestsでは、現在実装中の機能やコードレビューの内容、
リリース予定を把握できます。
特に、マージ間近のPRは次のリリースに含まれる可能性が高い機能です。

**効果的な活用法**
定期的な確認習慣として、週1回のIssues/PRチェック、
Releaseページの確認、Milestoneの進捗把握をお勧めします。

フィルタリング機能を活用することで、効率的に情報収集できます。
`label:feature-request`で新機能提案、`milestone:next`で次期リリース予定、
`is:open is:pr`で現在オープンなPull Requestを確認できます。

通知設定では、リポジトリのWatch設定や、
興味のあるIssueをSubscribeすることで、
重要な更新を見逃さないようにできます。

GitHub Repositoryを活用することで、
VS Codeの開発動向を詳細に把握し、新機能への準備を整えることができます。
-->

---
layout: center
---

# VS CodeのMonthly Updateをチェックする

<div class="grid grid-cols-3 gap-8 mt-12">

<div class="text-center space-y-4">
<div class="text-6xl">📅</div>
<h2 class="text-xl font-bold text-blue-400">毎月の情報源</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>• Release Notes</div>
<div>• VS Code Blog</div>
<div>• Update動画</div>
<div>• Change Log</div>
</div>
</div>

<div class="text-center space-y-4">
<div class="text-6xl">🔍</div>
<h2 class="text-xl font-bold text-purple-400">注目ポイント</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>• 新機能の詳細</div>
<div>• 破壊的変更</div>
<div>• パフォーマンス改善</div>
<div>• 拡張機能API変更</div>
</div>
</div>

<div class="text-center space-y-4">
<div class="text-6xl">⚡</div>
<h2 class="text-xl font-bold text-green-400">活用方法</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>• リリース日に即チェック</div>
<div>• 設定変更の確認</div>
<div>• 新機能の実験</div>
<div>• チームでの情報共有</div>
</div>
</div>

</div>

<div class="mt-12 bg-gray-800 p-4 rounded-lg">
<div class="text-center text-sm text-gray-400">
公式ページ: <a href="https://code.visualstudio.com/updates" class="text-blue-400 hover:underline">code.visualstudio.com/updates</a><br>
毎月第1木曜日にリリース、詳細な変更内容と使用例を提供
</div>
</div>

<!--
VS CodeのMonthly Updateは、毎月リリースされる最も重要な情報源です。

**毎月の情報源**
Release Notesは最も詳細で公式な情報源です。
VS Code Blogでは新機能の背景や使用例が詳しく解説されます。
Update動画では視覚的に新機能を確認でき、Change Logでは技術的な変更を把握できます。

**注目すべきポイント**
新機能の詳細は今後の開発に直接影響します。
破壊的変更は既存のワークフローに影響する可能性があります。
パフォーマンス改善は開発効率に直結し、
拡張機能API変更は使用している拡張機能に影響する可能性があります。

**効果的な活用方法**
毎月第1木曜日のリリース日に即座にチェックすることをお勧めします。
設定変更が必要かどうかを確認し、新機能を実際に試してみることが重要です。
チームでの情報共有により、組織全体での活用を促進できます。

VS CodeのMonthly Updateを定期的にチェックすることで、
常に最新の機能を活用し、開発効率を最大化することができます。
-->

---
layout: center
class: text-center
---

# 自分で情報を追うのが大変、そんな人へ

<div class="text-4xl">😓</div>

<div class="mt-8 text-xl text-gray-400">
情報収集を効率化するためのリソースとコミュニティ
</div>

<!--
ここまでVS CodeやGitHub Copilotの進化を追うための様々な方法をご紹介してきましたが、
「これだけの情報を自分で追うのは大変」と感じる方も多いと思います。

実際に、新機能のリリース頻度は非常に高く、
毎日のようにInsidersには新しい機能が追加され、
毎月のアップデートでは大量の新機能や変更がリリースされます。

個人で全ての情報を追跡し、理解し、活用するのは現実的ではありません。
そこで重要になるのが、情報収集を効率化するリソースの活用と、
コミュニティとの連携です。

このスライドでは、自分で全てを追わなくても
効率的に最新情報をキャッチアップできる方法をご紹介します。

時間を節約しながらも、重要な情報を見逃さないための
実践的なアプローチを学んでいきましょう。
-->

---
layout: image-left
image: /vscode-meetup-monthly-update-playlist.png
---

# Monthly Update配信

**効率的な情報収集の解決策**

- 毎月リリースノートをみんなでチェック
- すべての内容をデモを通して解説
- これを見るだけで最新情報を追える

<div class="mt-6">
  <img src="/time-version-chart.png" alt="時間とバージョンの関係グラフ" class="w-full max-w-xs rounded-lg shadow-lg" />
  <div class="mt-2 text-xs text-gray-500 text-center">
    アプデが多すぎてついに3時間超えに
  </div>
</div>

<!--
VS Code Monthly Updateのまとめ動画プレイリストをご紹介します。

この動画シリーズは、毎月リリースされるVS Codeのアップデート内容を
分かりやすく解説したものです。

**動画の特徴**
- 新機能の実演デモ
- 実際の使用例の紹介
- 設定方法の詳細説明
- 開発効率向上のTips

**活用メリット**
長い公式ドキュメントを読む時間がない場合でも、
動画を見ることで効率的に新機能を把握できます。
視覚的な説明により、機能の理解が深まります。

通勤時間や休憩時間などの隙間時間を活用して
最新情報をキャッチアップすることが可能です。

このようなコミュニティ発信の情報を活用することで、
個人での情報収集負荷を大幅に軽減できます。
-->

---
layout: center
class: text-center
---

# まとめ

<div class="text-5xl">🚀</div>

<div class="mt-8 text-xl text-gray-400">
AI時代の開発体験で得られた知見
</div>

<!--
最後に、今日お話しした内容をまとめて振り返りたいと思います。

「生成AIを活用したVS Codeによるこれからの開発体験」というテーマで、
VS Codeの10年間の進化と、GitHub Copilotによって実現された革新的な開発体験について
詳しくお話ししてきました。

このセッションを通じて、皆さんに以下のことをお伝えできたのではないかと思います：

1. VS Codeがいかに開発者ツールの概念を変革してきたか
2. GitHub CopilotがどのようにAI時代の開発体験を実現したか
3. オープンソース化によってもたらされる透明性と可能性
4. これからの開発体験で私たちに求められるスキルと心構え

この急速な技術進歩の中で、重要なのは変化を恐れるのではなく、
新しい技術を積極的に学び、活用していくことです。

最後に、今日のセッションの重要なポイントをまとめて締めくくりたいと思います。
-->

---
layout: center
---

# プレゼンテーションの重要なポイント

<div class="grid grid-cols-2 gap-12 mt-8">

<div class="space-y-6">

## 🏆 VS Codeの10年間の成功

<div class="space-y-3 text-sm">
<div class="flex items-start space-x-2">
<span class="text-blue-400">📈</span>
<span>市場シェア **7% → 73.6%** の劇的成長</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-blue-400">🔧</span>
<span>拡張機能エコシステムによる成功</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-blue-400">🌐</span>
<span>リモート開発環境の革新</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-blue-400">🤖</span>
<span>AI統合による開発体験の変革</span>
</div>
</div>

## 💫 GitHub Copilotの革命

<div class="space-y-3 text-sm">
<div class="flex items-start space-x-2">
<span class="text-purple-400">⚡</span>
<span>**55%** 高速なタスク完了を実現</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-purple-400">👥</span>
<span>**1.8M** 有料サブスクライバー</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-purple-400">🏢</span>
<span>Fortune 500企業の **1/3** が導入</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-purple-400">📊</span>
<span>**88%** のコードが開発者に保持される高品質</span>
</div>
</div>

</div>

<div class="space-y-6">

## 🔓 オープンソース化の意義

<div class="space-y-3 text-sm">
<div class="flex items-start space-x-2">
<span class="text-green-400">🔍</span>
<span>透明性向上による信頼性構築</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-green-400">⚙️</span>
<span>企業固有要件への柔軟な対応</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-green-400">🤝</span>
<span>開発者コミュニティとの協働促進</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-green-400">🏁</span>
<span>競合他社への戦略的優位性確保</span>
</div>
</div>

## 🚀 これからの開発体験

<div class="space-y-3 text-sm">
<div class="flex items-start space-x-2">
<span class="text-yellow-400">⚡</span>
<span>**Code Completion**: リアルタイム補完</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-yellow-400">💬</span>
<span>**Agent Mode**: 対話型開発支援</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-yellow-400">🤖</span>
<span>**Coding Agent**: 自律的コーディング</span>
</div>
<div class="flex items-start space-x-2">
<span class="text-yellow-400">📚</span>
<span>継続的学習と情報収集の重要性</span>
</div>
</div>

</div>

</div>

<!--
今日のプレゼンテーションの重要なポイントをまとめました。

**VS Codeの10年間の成功**
VS Codeは2015年の登場から2024年まで、市場シェアを7%から73.6%まで成長させました。
拡張機能エコシステムの確立、リモート開発環境の革新、
そしてAI統合による開発体験の変革という3つの大きな進化を遂げました。

**GitHub Copilotの革命**
2022年の統合以降、開発者の生産性を55%向上させ、
1.8百万人の有料サブスクライバーを獲得しました。
Fortune 500企業の3分の1が導入し、
開発者が生成されたコードの88%を保持するという高い品質を実現しています。

**オープンソース化の意義**
2025年のGitHub Copilot Chatオープンソース化は、
透明性向上、企業要件への対応、コミュニティ協働、競合優位性確保という
多面的な戦略的意義を持っています。

**これからの開発体験**
Code Completion、Agent Mode、Coding Agentという
3つのコーディング方法により、開発者の役割は大きく変化しています。
継続的な学習と情報収集が、この変化についていくために重要です。
-->

---
layout: center
---

# 私たちに求められるもの

<div class="space-y-8 mt-8">

<div class="grid grid-cols-3 gap-8">

<div class="text-center space-y-4">
<div class="text-5xl">🧠</div>
<h2 class="text-xl font-bold text-blue-400">新しい思考</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>AIと協働する発想</div>
<div>創造性を重視する姿勢</div>
<div>効率化への柔軟性</div>
</div>
</div>

<div class="text-center space-y-4">
<div class="text-5xl">📚</div>
<h2 class="text-xl font-bold text-purple-400">継続的学習</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>新機能の積極的な試行</div>
<div>コミュニティとの情報共有</div>
<div>基礎スキルの維持・向上</div>
</div>
</div>

<div class="text-center space-y-4">
<div class="text-5xl">🔮</div>
<h2 class="text-xl font-bold text-green-400">未来への準備</h2>
<div class="text-sm text-gray-300 space-y-2">
<div>変化を恐れない心構え</div>
<div>技術進歩への適応力</div>
<div>価値創造への集中</div>
</div>
</div>

</div>

<div class="mt-12 bg-gray-800 p-6 rounded-lg">
<h3 class="text-lg font-bold text-center mb-4 text-gradient bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 bg-clip-text text-transparent">
開発者の役割は「コードを書く人」から「AIと協働してソリューションを創造する人」へ
</h3>
<div class="text-center text-sm text-gray-400">
単純作業の自動化により、より創造的で戦略的な課題に集中できる時代が到来
</div>
</div>

</div>

<!--
AI時代の開発体験において、私たち開発者に求められるものは大きく変化しています。

**新しい思考の必要性**
AIと協働する発想が重要になります。AIを単なるツールとして使うのではなく、
開発パートナーとして活用する思考が必要です。
創造性を重視する姿勢と、効率化への柔軟性が求められます。

**継続的学習の重要性**
技術の進歩が急速な今、新機能を積極的に試し、
コミュニティとの情報共有を通じて学び続けることが重要です。
同時に、AIに依存するだけでなく、基礎的なスキルの維持・向上も欠かせません。

**未来への準備**
変化を恐れない心構えと技術進歩への適応力が必要です。
重要なのは、技術の変化に振り回されるのではなく、
価値創造に集中することです。

**開発者の役割の変化**
これらの要素により、開発者の役割は根本的に変化しています。
「コードを書く人」から「AIと協働してソリューションを創造する人」へ。

単純作業の自動化により、私たちはより創造的で戦略的な課題に集中できる
素晴らしい時代を迎えています。

この変化を積極的に受け入れ、新しい開発体験を楽しんでいきましょう。
-->

---
layout: center
class: text-center
---

# 最後に

<div class="space-y-8 mt-8">

<div class="text-center">
<div class="text-5xl mb-4">🙏</div>
<h2 class="text-3xl font-bold text-gradient bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 bg-clip-text text-transparent">
ご盛聴ありがとうございました
</h2>
</div>

<div class="grid grid-cols-2 gap-12 mt-12">

<div class="space-y-4">
<h3 class="text-xl font-bold text-blue-400">📞 お気軽にお声がけください</h3>
<div class="space-y-2 text-sm">
<div class="flex items-center justify-center space-x-2">
<span class="text-blue-500">🐦</span>
<span>X: <a href="https://x.com/Yuhei_FUJITA" class="text-blue-500 hover:underline">@Yuhei_FUJITA</a></span>
</div>
<div class="flex items-center justify-center space-x-2">
<span class="text-purple-500">💬</span>
<span>Discord: <a href="https://discord.gg/MG6wy7mjRk" class="text-purple-500 hover:underline">VS Code Meetup</a></span>
</div>
<div class="flex items-center justify-center space-x-2">
<span class="text-green-500">📧</span>
<span>何でもお聞きください！</span>
</div>
</div>
</div>

<div class="space-y-4">
<h3 class="text-xl font-bold text-purple-400">🎯 VS Code Meetup</h3>
<div class="space-y-2 text-sm">
<div class="flex items-center justify-center space-x-2">
<span class="text-blue-500">🌐</span>
<span><a href="https://vscode.connpass.com/" class="text-blue-500 hover:underline">vscode.connpass.com</a></span>
</div>
<div class="flex items-center justify-center space-x-2">
<span class="text-purple-500">👥</span>
<span>4,727人のコミュニティ</span>
</div>
<div class="flex items-center justify-center space-x-2">
<span class="text-green-500">📅</span>
<span>月1回のペースで開催中</span>
</div>
</div>
</div>

</div>

<div class="mt-12 bg-gray-800 p-6 rounded-lg">
<div class="text-lg text-center text-gray-300">
AIと共に歩む開発の未来を、一緒に楽しんでいきましょう！🚀
</div>
</div>

</div>

<!--
最後になりますが、本日は貴重なお時間をいただき、本当にありがとうございました。

「生成AIを活用したVS Codeによるこれからの開発体験」というテーマで、
VS Codeの進化、GitHub Copilotの革命、そしてこれからの開発者に求められることについて
お話しさせていただきました。

**今日お伝えしたかったこと**
技術の進歩は急速ですが、変化を恐れる必要はありません。
むしろ、AI統合による開発体験の向上は、私たち開発者にとって大きなチャンスです。
単純作業から解放され、より創造的で価値のある仕事に集中できる時代が到来しています。

**皆さんへのお願い**
ぜひ今日学んだことを実際に試してみてください。
GitHub Copilotを使ってみる、VS Code Insidersを試してみる、
コミュニティに参加してみる、小さなことから始めることが重要です。

**つながりを大切に**
VS Codeに関する質問、AI開発についての相談、新機能の共有など、
いつでもお気軽にお声がけください。
VS Code Meetupコミュニティでは、皆さんとの交流をお待ちしています。

AIと共に歩む開発の未来を、一緒に楽しんでいきましょう！

本日は本当にありがとうございました。
-->

---
layout: center
class: text-center
---

# Thank you!

<div class="text-6xl">🎉</div>

<div class="mt-8 text-2xl text-gray-400">
Happy Coding with AI! 🤖✨
</div>

<!--
Thank you very much for your attention!

今日は本当にありがとうございました。
AIと一緒に、楽しいコーディングライフをお過ごしください！

ぜひこれからも新しい技術に挑戦し続け、
素晴らしい開発体験を追求していってください。

Happy Coding with AI!
-->

