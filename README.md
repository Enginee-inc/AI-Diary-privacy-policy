# AI-Diary-privacy-policy

アプリ「AI Diary」のプライバシーポリシー及び利用規約の設置リポジトリです。
GitHub Pages で公開しています。

**2文書はそれぞれ独立した単独ページ**です。まとめの入口ページ（index）はあえて置いていません。
App Store 審査でリンクを開いたときに、1クリックも挟まず本文が表示される状態にするためです。

| ファイル | 公開URL |
|---|---|
| `privacy-policy.html` | https://enginee-inc.github.io/AI-Diary-privacy-policy/privacy-policy.html |
| `terms.html` | https://enginee-inc.github.io/AI-Diary-privacy-policy/terms.html |
| `source/*.md` | 生成元の Markdown（差分レビュー用のコピー。公開表示には使わない） |
| `.nojekyll` | Jekyll を無効化（`source/*.md` が HTML へ変換されて衝突するのを防ぐ） |

各ページは日本語と英語を併記し、冒頭の言語切替と目次から辿れます。

## ⚠️ 公開には可視性の切り替えが必要

このリポジトリが **internal のままだと、上記URLは GitHub のログイン画面へリダイレクトされ、
審査担当にもユーザーにも本文が見えません**（private Pages のため）。
`Settings > General > Change repository visibility` から **Public** にしてください。

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
