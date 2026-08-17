# AI-Diary-privacy-policy

アプリ「AI Diary」のプライバシーポリシー及び利用規約の設置リポジトリです。
GitHub Pages で静的サイトとして公開しています。

| ファイル | 内容 |
|---|---|
| `index.html` | 2文書への入口 |
| `privacy-policy.html` | プライバシーポリシー（日本語・English） |
| `terms.html` | 利用規約（日本語・English） |
| `source/*.md` | 生成元の Markdown（差分レビュー用のコピー） |
| `.nojekyll` | Jekyll を無効化（`source/*.md` が HTML へ変換されて衝突するのを防ぐ） |

## ⚠️ このリポジトリの HTML を直接編集しないこと

**法務文書の正本はアプリ本体のリポジトリ `ai-diary-demo` の `doc/legal/*.md` です。**
かつて正本が Notion とリポジトリで二重管理になり内容がずれた経緯があるため、正本は1箇所に固定しています。

本文を修正するときは:

1. `ai-diary-demo` 側で `doc/legal/privacy-policy.md` / `doc/legal/terms.md` を編集する
2. 生成し直す

   ```bash
   # ai-diary-demo のルートで
   node scripts/build-legal-site.mjs --out /path/to/AI-Diary-privacy-policy
   ```

3. このリポジトリの差分をコミットして push する（Pages が自動で再デプロイされます）

`source/*.md` も手で編集しないでください（手順2で上書きされます）。

## リンクの扱い

生成時に、利用規約から参照しているプライバシーポリシーへのリンクだけを、
Notion の公開ミラーからこのサイト内の `./privacy-policy.html` へ差し替えています
（差し替え表は `scripts/build-legal-site.mjs` の `PUBLISH_LINK_REWRITES`）。
全社プライバシーポリシーは AI Diary のポリシーとは別文書なので、Notion のまま維持しています。

## お問い合わせ

株式会社Enginee — legal@enginee.co.jp / https://www.enginee.co.jp/form
