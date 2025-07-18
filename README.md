# 生成AIを活用したVS Codeによるこれからの開発体験

📅 **AOAI Dev Day 2025** | 2025年7月18日  
🎯 **イベント情報**: [aoai-devday.com](https://aoai-devday.com/)

## 概要

このプレゼンテーションでは、GitHub Copilotの登場からどのようにVS Codeが進化してきたのか、そしてこれからの開発体験がどのように変わっていくのかをお話します。

VS Codeは2015年の登場から現在まで、開発者ツールの概念を根本的に変革してきました。特に2022年のGitHub Copilot統合以降、AIを活用した開発体験が劇的に向上しています。

### 発表内容
- VS Codeのこれまでの10年間の歩み
- GitHub Copilotの登場と進化
- これからの開発体験がどう変わっていくか
- この急速な進化についていく方法

## スピーカー

**Yuhei FUJITA（ふじた）**  
🏃‍♂️ [VS Code Meetup](https://vscode.connpass.com/) 運営  
🐦 X: [@Yuhei_FUJITA](https://x.com/Yuhei_FUJITA)

## 開発環境のセットアップ

このプレゼンテーションは [Slidev](https://github.com/slidevjs/slidev) を使用して作成されています。

### 必要な環境
- Node.js 18+ 
- pnpm（推奨パッケージマネージャー）

### インストールと起動

```bash
# 依存関係のインストール
pnpm install

# 開発サーバーの起動
pnpm dev
```

開発サーバーが起動したら、ブラウザで <http://localhost:3030> にアクセスしてプレゼンテーションを確認できます。

### 利用可能なコマンド

```bash
# 開発サーバー起動（自動でブラウザが開きます）
pnpm dev

# 静的サイトとしてビルド
pnpm build

# PDF/PPTX形式でエクスポート
pnpm export
```

## プロジェクト構成

```
├── slides.md           # メインのプレゼンテーションファイル
├── package.json        # プロジェクト設定
├── vite.config.ts      # Vite設定（ポート3030で起動）
├── public/             # 静的ファイル
├── components/         # カスタムコンポーネント（予約済み）
├── pages/              # カスタムページ（予約済み）
└── snippets/           # コードスニペット（予約済み）
```

## スライドの編集

プレゼンテーションのすべての内容は `slides.md` ファイルに記載されています。このファイルを編集すると、開発サーバーが自動的に変更を反映します。

### 注意事項
- このプロジェクトではpnpmの使用が必須です（npm/yarnは使用しないでください）
- 開発サーバーは `localhost:3030` で起動します
- スライドはマークdown形式で記述され、Vue.jsコンポーネントも使用できます

## Slidevについて

Slidevの詳細な使用方法やカスタマイズ方法については、[公式ドキュメント](https://sli.dev/)をご参照ください。

### 使用テーマ
- **テーマ**: [@slidev/theme-seriph](https://github.com/slidevjs/slidev/tree/main/packages/theme-seriph)
- **カラースキーマ**: ダークモード
- **CSS フレームワーク**: UnoCSS

## ライセンス

このプレゼンテーションの内容は個人の発表用途で作成されています。
