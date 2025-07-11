# Claude Code プロジェクト

## 概要
このプロジェクトは Claude Code の開発環境をセットアップするためのものです。

## 開発環境

### システム要件
- Docker
- Docker Compose
- Node.js v20.19.3

### セットアップ
1. 環境変数の設定
   ```bash
   cp .env.example .env
   # .env ファイルを編集して適切な値を設定
   ```

2. Docker コンテナの起動
   ```bash
   docker-compose up -d
   ```

### 環境変数
- `GIT_USER_NAME`: Git ユーザー名
- `GIT_USER_EMAIL`: Git メールアドレス

## ファイル構成
```
/workspace/
├── .devcontainer/          # DevContainer 設定
│   ├── Dockerfile         # Docker イメージ定義
│   ├── devcontainer.json  # DevContainer 設定
│   └── init-firewall.sh   # ファイアウォール初期化スクリプト
├── .env                   # 環境変数 (gitignore対象)
├── .gitignore             # Git無視ファイル
├── docker-compose.yml     # Docker Compose 設定
└── CLAUDE.md             # このファイル
```

## Git設定
- デフォルトブランチ: `main`
- `.env` ファイルはgitignore対象のため、Git管理から除外されています

## 使用方法
DevContainer を使用して開発環境を構築し、Claude Code での開発を行います。

## 開発時の注意点
- `.env` ファイルは機密情報を含むため、Git管理から除外されています
- 新しい環境では `.env` ファイルを手動で作成してください
- Node.js用の標準的な.gitignore設定が適用されています