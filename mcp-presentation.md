---
marp: true
theme: default
paginate: true
---
# MCP勉強会資料
### 〜MCPとは何か、そしてなぜ今注目されるのか〜
---
## 🎯 勉強会の目的
- 社内でもプライベートでも、AI活用において**MCPは必須技術**に
- **社内LLMサーバー**の活用を広げる（MCPで操作できるように）
- 最新の生成AI技術を理解し、**世間との技術的乖離を防ぐ**
- **MicrosoftがOSレベルでMCPの採用を発表**（2024年5月）し、今後の業界標準になる可能性大！
---
## 👥 参加者の前提知識
| 項目             | レベル                     |
|------------------|----------------------------|
| Python           | 読める                     |
| ターミナル操作   | 基本的な操作は可能         |
| MCP / OpenAI API | 一部は聞いたことがある程度 |
---
## 🧠 MCPとは？
> 「生成AIに"何を""どこから"呼び出すかを決める、新しい連携プロトコルです」
---
## 🔌 MCPは"AI界のUSBポート"
| 観点         | USB                            | MCP                                              |
|--------------|----------------------------------|---------------------------------------------------|
| 接続         | プラグ統一で簡単に繋がる        | 呼び出し形式が統一されていてLLMが簡単に使える     |
| 仕様の変更   | OSはデバイスの仕様を意識しない  | LLMはToolの仕様変更を意識せずに使える             |
| 開発・追加   | USB機器なら誰でも作れる         | MCP Toolなら誰でも追加できる                     |
---
## 🚀 MCPとAPIの違い（ワークフロー）
### 🌐 従来のAPI方式：
1. API仕様を調べる
2. コードで実装する
3. 仕様が変わるたびに修正が必要
### 🔗 MCP方式：
1. MCP Toolに仕様を登録
2. LLMは常に同じ形式で呼び出す
3. **Tool側が変わってもLLM側はそのまま！**
---
## 🧪 MCPとAPIのコード比較（参考）
```python
# API方式：コード実装が必要
url = f"https://api.example.com/v1/weather/{city}"
response = requests.get(url)
# MCP方式：自然言語「東京の天気を教えて」でToolが実行される
```
---
## 🛠 活用例①：GitLab操作
- 「新しいリポジトリを作って」→ GitLabに即時反映！
```json
{
  "name": "create_repository",
  "parameters": {
    "project_name": "llm-demo",
    "visibility": "private"
  }
}
```
---
## 📚 活用例②：arXiv論文検索
- 「LLMの効率化に関する最新の論文を教えて」
```json
{
  "name": "search_arxiv",
  "parameters": {
    "query": "LLM efficiency 2024",
    "max_results": 5
  }
}
```
---
## 📊 活用例③：社内DBクエリ
- 「4月の売上が一番高かった支店は？」
```json
{
  "name": "query_sales",
  "parameters": {
    "query": "Which branch had the highest sales in April?"
  }
}
```
---
## 🧭 MCP全体構造図
![bg contain](A_diagram_in_the_digital_illustration_style_depict.png)
---
## 🧩 MCPとToolの関係性
- MCPは「統一インターフェース」
- Toolは自由な中身で拡張可能
- LLMは**Toolの仕様を知らずに自然言語で利用可能**！
---
## ⚙️ 補足：Python実行の意味
MCP設定で `"command": "python"` とあるのは、Pythonスクリプトで**MCP対応のサーバーアプリケーションを起動するため**です。
このサーバーは以下のような役割を果たします：
- LLMからのMCPリクエストを受け取る
- リクエストに含まれるTool名とパラメータに基づいて処理を実行
- 結果をレスポンスとしてLLMに返す
つまり、Python側では「Toolの実装」と「MCPプロトコルの解釈・応答」が行われています！
---
## 🎁 おまけ：今後の応用のヒント
- 社内業務をMCPでツール化してLLMで操作！
- Excel操作 / スケジューラ登録 / データ集計なども可能に
---
## 🙏 ご清聴ありがとうございました！
MCPでAI活用がより自由に、よりスマートになりますのよ〜っ💕