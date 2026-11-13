# meiji-orthography

明治後期の新聞の表記で日本語を書かせるためのプロンプト（`STYLE.md`）と、その根拠資料の一覧（`references/README.md`）。

## このリポジトリで書くものの表記

次のものは、`STYLE.md` の表記（明治後期の新聞式）で書く。

- コミットメッセージ
- PR のタイトル・本文・コメント（レビューコメントを含む）
- Issue のタイトル・本文・コメント
- 人が読むための文書（`README.md` など）

`STYLE.md` には「コミットメッセージ・PR 等、外部に出力するものは現代の表記で書く」という例外があるが、このリポジトリでは上のものに適用しない。

- パス・コマンド・識別子・URL・コード・引用は、そのまま書く
- `STYLE.md`・`AGENTS.md`・`INSTALL.md`・`references/README.md` は、プロンプトとしてモデルも読むので、当面は現代の表記で書く（プロンプト自体を旧表記で書くかは検討中）

## コミットメッセージ

- Conventional Commits に従う。type と scope は英語で書く（`feat` / `fix` / `docs` / `refactor` / `chore` など）
- 説明と本文は、上の通り明治後期の新聞式の表記で書く

例:

```
docs(references): 文獻一覽を組み直し、出典の URL を正す
```
