# Markdown PDF Style Guide

## 概要

`markdown-pdf-style.css`は、VS CodeのMarkdown PDF拡張機能で使用するためのシンプルで洗練されたCSSスタイルシートです。日本語文書に最適化されており、プロフェッショナルな見た目のPDFを生成できます。

## 主な特徴

### ✨ デザイン
- **シンプル**: クリーンで読みやすいレイアウト
- **プロフェッショナル**: ビジネス文書に適した洗練されたデザイン
- **日本語対応**: 日本語フォントに最適化

### 🔧 問題解決
- **表の縦線表示**: Markdown PDFでよくある縦線が表示されない問題を解決
- **強調表示**: `**「ここ」**`のような日本語引用符との組み合わせに対応
- **改ページ制御**: 表やコードブロックが途中で切れないよう制御

### 📄 対応要素
- 見出し（H1-H6）
- 強調表示（bold、italic）
- 表（テーブル）
- コードブロック
- リスト
- 引用
- 画像
- 水平線

## 使用方法

### 1. VS Code設定

`settings.json`に以下を追加してください：

```json
{
    "markdown-pdf.styles": [
        "https://raw.githubusercontent.com/ShunsukeTamura06/mcp-study-materials/main/markdown-pdf-style.css"
    ],
    "markdown-pdf.includeDefaultStyles": false,
    "markdown-pdf.format": "A4",
    "markdown-pdf.orientation": "portrait",
    "markdown-pdf.border.top": "2cm",
    "markdown-pdf.border.bottom": "2cm",
    "markdown-pdf.border.right": "1.5cm",
    "markdown-pdf.border.left": "1.5cm"
}
```

### 2. ローカルファイルの使用

ローカルにCSSファイルをダウンロードして使用する場合：

```json
{
    "markdown-pdf.styles": [
        "C:/path/to/markdown-pdf-style.css"
    ],
    "markdown-pdf.includeDefaultStyles": false
}
```

### 3. PDF出力

1. Markdownファイルを開く
2. `Ctrl+Shift+P`でコマンドパレットを開く
3. `Markdown PDF: Export (pdf)`を実行
4. 美しいPDFが生成されます

## スタイルカスタマイズ

### カラーテーマ

メインカラーを変更したい場合は、以下の変数を修正してください：

```css
/* 見出しの下線色 */
h1 { border-bottom: 3px solid #3498db; }  /* ブルー */

/* 強調表示の背景色 */
strong { background-color: rgba(255, 235, 59, 0.2); }  /* イエロー */

/* 表のヘッダー色 */
th { background-color: #34495e; }  /* ダークグレー */
```

### フォント変更

```css
body {
    font-family: 'Your Preferred Font', 'Noto Sans JP', sans-serif;
    font-size: 12px;  /* サイズ調整 */
}
```

## ユーティリティクラス

特別な装飾が必要な場合に使用できるクラス：

```markdown
<div class="highlight">
重要な情報をハイライト
</div>

<div class="note">
📝 補足情報
</div>

<div class="warning">
⚠️ 注意事項
</div>

<div class="center">
中央揃えのテキスト
</div>

<div class="page-break"></div>
<!-- ここで改ページされます -->
```

## トラブルシューティング

### 表の縦線が表示されない
→ このCSSファイルで解決されています。`!important`を使用して強制的に境界線を表示します。

### 強調表示が効かない
→ 日本語引用符の問題に対応済みです。`** 「ここ」 **`のようにスペースを入れても動作します。

### フォントが適用されない
→ 日本語フォントが複数指定されているため、環境に応じて最適なフォントが選択されます。

## 更新履歴

- **2025-07-02**: 初回リリース
  - 基本スタイルの実装
  - 表の縦線問題解決
  - 日本語対応の強化

## ライセンス

このCSSファイルはMITライセンスのもとで公開されています。自由にご利用ください。
