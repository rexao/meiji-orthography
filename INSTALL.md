# インストール手順（受け取った側の Claude Code 向け）

日本語のメッセージへの回答を、明治後期の新聞の表記で書かせるプロンプト。
`~/.claude/CLAUDE.md` には import の 1 行だけを書き、中身はこのリポジトリに置いたまま使う。

## 中身

- `STYLE.md`: 規則の本体（「## 会話の表記（明治後期の新聞式）」の節）。使うのはこのファイルだけ
- `references/README.md`: 規則の根拠資料の一覧と、規則との対応表
- `AGENTS.md`・`CLAUDE.md`: このリポジトリを編集するときの規約。使うだけなら不要

## 手順

1. clone する場所（親ディレクトリ）をユーザーに尋ねる。以下の `~/path/to/` は、そのパスに置き換える
2. このリポジトリを clone する。`~/path/to/meiji-orthography/` ができる

   ```sh
   cd ~/path/to/
   git clone https://github.com/rexao/meiji-orthography.git
   ```

3. `~/.claude/CLAUDE.md` に次の 1 行を足す。既に「会話の表記」に当たる節があれば、その節を消してこの行に置き換える

   ```
   @~/path/to/meiji-orthography/STYLE.md
   ```

4. `STYLE.md` 末尾の「例外」の列挙（Notion・Gmail・Claude Docs 等）は、元の環境で使っている出力先。受け取り側の環境に合わせて直す。直した上で更新も受け取り続けるなら、fork して管理する

## 更新

clone した場所で `git pull` する。`STYLE.md` は import しているだけなので、次の会話から新しい規則が効く。

## 根拠資料（任意）

規則の出典を確かめたいときだけ要る。資料のファイルは著作権と容量のためリポジトリに含めていない。`references/README.md` の各文献の節にある URL から入手し、そこに書かれた「ファイル名」で `references/` に置く。
