# MCP Streamable HTTP Sample

このリポジトリは、Model Context Protocol (MCP) の Streamable HTTP 実装のサンプルコードを提供します。

## 概要

MCP (Model Context Protocol) は、クライアントとサーバー間の通信プロトコルで、複数の通信方式をサポートしています。このサンプルでは、Streamable HTTP 方式を使用した実装例を示しています。

Streamable HTTP は以下の特徴を持ちます：

- HTTP POST リクエストでメッセージを送信
- HTTP GET リクエストで Server-Sent Events (SSE) ストリームを確立
- セッション管理によるステートフルな通信

## 機能

このサンプルには以下の機能が含まれています：

- サーバー側：
  - Streamable HTTP トランスポートの実装
  - 複数クライアント接続のサポート
  - ツール機能の提供（echo、add）
  - セッション管理

- クライアント側：
  - サーバーへの接続
  - ツール一覧の取得
  - ツールの呼び出し

## 前提条件

- Node.js 18.x 以上
- npm または yarn

## インストール

```bash
# リポジトリをクローン（サブモジュールを含む）
git clone --recursive https://github.com/moritalous/mcp-streamablehttp-sample.git
cd mcp-streamablehttp-sample

# 依存関係をインストール
npm install

# TypeScript SDKをセットアップ
npm run setup
```

## ビルド

```bash
npm run build
```

## 実行方法

### サーバーの起動

```bash
npm run start:server
```

サーバーは、デフォルトでポート 3001 で起動します。環境変数 `PORT` を設定することで、ポート番号を変更できます。

### クライアントの実行

```bash
npm run start:client
```

クライアントは、デフォルトで `http://localhost:3001/mcp` に接続します。環境変数 `MCP_SERVER_URL` を設定することで、接続先を変更できます。

## 開発

開発モードでの実行：

```bash
# サーバー（開発モード）
npm run dev:server

# クライアント（開発モード）
npm run dev:client
```

## プロジェクト構成

```
mcp-streamablehttp-sample/
├── src/
│   ├── client.ts     # クライアント実装
│   └── server.ts     # サーバー実装
├── typescript-sdk/   # MCP TypeScript SDK (Gitサブモジュール)
├── dist/             # コンパイル済みコード
├── package.json      # プロジェクト設定
└── tsconfig.json     # TypeScript 設定
```

## ライセンス

MIT

## 参考資料

- [Model Context Protocol 仕様](https://spec.modelcontextprotocol.io/)
- [MCP SDK ドキュメント](https://github.com/modelcontextprotocol/typescript-sdk)
