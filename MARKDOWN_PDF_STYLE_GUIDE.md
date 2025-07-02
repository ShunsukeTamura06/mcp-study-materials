# Markdown PDF Style Guide

## 概要

`markdown-pdf-style.css`は、VS CodeのMarkdown PDF拡張機能で使用するためのシンプルなCSSスタイルシートです。主に表の縦線表示問題を解決します。

## 主な特徴

- **表の縦線表示**: Markdown PDFでよくある縦線が表示されない問題を解決
- **シンプル**: 必要最小限のスタイル設定
- **日本語対応**: 日本語フォントに最適化

## 使用方法

VS Codeの `settings.json` に以下を追加：

```json
{
    "markdown-pdf.styles": [
        "https://raw.githubusercontent.com/ShunsukeTamura06/mcp-study-materials/main/markdown-pdf-style.css"
    ],
    "markdown-pdf.includeDefaultStyles": false
}
```

## 強調表示の問題について

⚠️ **重要**: `**「ここ」**` のような日本語引用符との組み合わせはMarkdownパーサーの制限により、CSSでは解決できません。

### 解決方法

1. **HTMLタグを使用（推奨）**:
   ```markdown
   <strong>「ここ」</strong>
   ```

2. **引用符を分離**:
   ```markdown
   **「ここ**」
   ```

3. **アンダースコア記法**:
   ```markdown
   __「ここ」__
   ```

## トラブルシューティング

### 表の縦線が表示されない
→ このCSSで解決されます

### 強調表示が効かない
→ 上記の解決方法を使用してください

## ライセンス

MIT License
