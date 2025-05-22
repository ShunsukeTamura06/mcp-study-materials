# MCP勉強会資料 📚

このリポジトリは、**Model Context Protocol (MCP)** に関する勉強会資料をまとめたものです。MCPは、AIと外部ツールを接続するための革新的なプロトコルで、2024年11月にAnthropicによりオープンソースとして発表されました。

## 🎯 目的

このリポジトリの目的は以下の通りです：

- MCPの基本概念と仕組みを理解する
- 実際の業務での活用例を学ぶ  
- MCPサーバーの作成・運用方法を習得する
- 社内でのMCP導入における課題と対策を共有する

## 📋 内容概要

### 📊 プレゼンテーション資料

| ファイル | 形式 | 説明 |
|---------|------|------|
| `mcp-introduction.md` | Marp (Markdown) | MCPの概要と活用例についてのプレゼンテーション（編集可能） |
| `mcp-introduction.pdf` | PDF | プレゼンテーション資料のPDF版（配布用） |
| `mcp-introduction.pptx` | PowerPoint | プレゼンテーション資料のPowerPoint版（編集用） |
| `mcp-presentation.md` | Marp (Markdown) | 旧版のプレゼンテーション資料 |

### 🖼️ 図表・画像

| ファイル | 説明 |
|---------|------|
| `image.png` | MCPホストとMCPサーバーの立ち上げ図 |
| `image-1.png` | LLMのシステムプロンプトにメタデータが組み込まれた状態 |
| `image-2.png` | MCPホストでのMCPサーバー実行例 |
| `image-3.png` | 公式MCPサーバーの一覧 |

## 🚀 主要トピック

### 1. MCPとは何か？
- AIが「答える」から「行動する」へ進化するためのプロトコル
- LLMとツール間の統一された通信規約
- 従来のAPI連携との違いとメリット

### 2. MCPの仕組み
- MCPホスト、MCPクライアント、MCPサーバーの役割
- メタデータの自動反映による動的なツール連携
- 認証とセキュリティ

### 3. 実用的な活用例
- ファイル操作の自動化
- Git操作の自然言語化
- メール・チャット連携
- データベース検索
- 論文検索の効率化

### 4. 実装方法
- FastMCPを使った簡単なMCPサーバー作成
- 設定ファイルの編集方法
- 公式MCPサーバーの活用

### 5. 社内導入の課題と対策
- MCPホストの制限への対応
- オープンソースMCPサーバーの運用
- セキュリティ制限下での実装方法

## 🛠️ 使用方法

### プレゼンテーション資料の閲覧・編集

#### Marp（推奨）
1. VS Codeに[Marp拡張機能](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)をインストール
2. `mcp-introduction.md`をVS Codeで開く
3. Marpプレビューで表示またはPDF/HTML/PPTXにエクスポート

#### その他の形式
- **PDF版**: `mcp-introduction.pdf`を直接開く（配布・印刷用）
- **PowerPoint版**: `mcp-introduction.pptx`をMicrosoft PowerPointで開く

### 資料の活用シーン

- **勉強会・研修**: MCPの基礎から実践まで段階的に学習
- **チーム共有**: AI活用促進のための知識共有
- **技術検討**: 新技術導入の判断材料として
- **実装ガイド**: MCPサーバー開発の参考資料として

## 🔧 技術仕様

### 対象者
- AI・機械学習に興味のある開発者
- 業務効率化を検討している非エンジニア
- 新しい技術トレンドを把握したい技術者

### 前提知識
- プログラミングの基礎知識（Python推奨）
- APIの基本概念
- LLM/ChatGPTの基本的な使用経験

### 実行環境
- Python 3.8以上（MCPサーバー開発用）
- Node.js（公式MCPサーバー使用時）
- VS Code + Marp拡張機能（資料編集用）

## 📈 更新履歴

- **2025-05-21**: 詳細なREADME追加、プレゼンテーション資料の充実
- **2025-05-20**: 初回リポジトリ作成、基本的なMCP概要資料追加

## 🤝 貢献・フィードバック

このリポジトリに対する改善提案や質問がございましたら、Issueやプルリクエストをお気軽にお送りください。MCPの理解促進と実用化に向けて、皆様のご協力をお待ちしています。

## 📚 参考リンク

- [Anthropic MCP公式ドキュメント](https://docs.anthropic.com/claude/docs/mcp)
- [MCP GitHub リポジトリ](https://github.com/modelcontextprotocol)
- [FastMCP ライブラリ](https://github.com/jlowin/fastmcp)
- [公式MCPサーバー一覧](https://github.com/modelcontextprotocol/servers)

---

**Note**: このリポジトリの資料は学習・研究目的で作成されており、実際の業務での導入前には十分な検証を行ってください。