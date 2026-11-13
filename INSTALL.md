# インストール手順（受け取った側の Claude Code 向け）

会話の表記を明治後期の新聞式にするプロンプトと、その根拠資料のパッケージ。
CLAUDE.md には import の 1 行だけを書き、中身はこのフォルダに置いたまま使う。

## 中身

- `STYLE.md`: 規則の本体（「## 会話の表記（明治後期の新聞式）」の節）
- `references/`: 根拠資料。中身は `references/README.md` を参照

## 手順

1. このフォルダを `~/.claude/meiji-orthography/` に置く
   （`STYLE.md` の中でこのパスを参照しているので、場所を変えるなら `STYLE.md` の中のパスも直す）
2. `~/.claude/CLAUDE.md` に次の 1 行を足す。既に「会話の表記」に当たる節があれば、その節を消してこの行に置き換える

   ```
   @~/.claude/meiji-orthography/STYLE.md
   ```

3. `STYLE.md` の中の次の 2 箇所は、元の環境の CLAUDE.md の別の節を前提にしている。受け取り側に合わせて直すか、消す
   - 「簡潔さ・1 段落 2 文の規則はこちらでも守る」（元の CLAUDE.md の回答スタイルの節を指す）
   - 末尾の「例外」の列挙（Notion・PR・Slack 等、元の環境で使っている出力先）

## 同期

両方の PC で使い続けるなら、このフォルダを dotfiles 等の Git リポジトリで管理し、`~/.claude/meiji-orthography/` に置く（またはシンボリックリンクを張る）。
