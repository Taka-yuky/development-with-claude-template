# development-with-claude-template

## このリポジトリの役割

Claude Codeをcoding agentとして利用する場合のテンプレートリポジトリです。
このリポジトリをテンプレートとして、各プロジェクトの開発を始めましょう！

## 使い方

1. このテンプレートからリポジトリを作成する
2. `CLAUDE.md` と `docs/` 配下の `【要記入】` を埋める
3. `【要確認】` の付いた前提（マルチテナント・パスワード認証など）がプロジェクトに当てはまるか確認し、当てはまらない記述は削除する
   - 残りは `grep -rn -e "【要記入】" -e "【要確認】" CLAUDE.md docs` で確認できる
4. `docs/options/` から必要なドキュメントだけ `docs/` へ移動し、`docs/INDEX.md` に反映する（使わないものは削除）
5. 設計判断は `docs/adr/000-template.md` をコピーして `docs/adr/001-xxx.md` のように記録する
6. `.claude/settings.json` の `permissions.deny` を確認し、AIに禁止したい操作を調整する
   - `.env.example` を読めるようにするため、`.env.*` はワイルドカードを使わずファイル名を列挙している。別名の `.env` ファイルを使う場合は追記する
7. `.github/` のIssue/PRテンプレートと `LICENSE` をプロジェクトに合わせて編集する

## 構成

| パス | 役割 |
|---|---|
| `CLAUDE.md` | AIの入口。`@` で常時読み込むのは `docs/INDEX.md` と `docs/DEVELOPMENT_RULES.md` のみ |
| `docs/` | AIと人間が共通で使うドキュメント（入口は `docs/INDEX.md`） |
| `docs/options/` | 必要に応じて使うドキュメントの雛形 |
| `docs/human/` | 人間向けドキュメント |
| `.claude/settings.json` | Claude Code の共有設定（commit / push・秘密情報ファイルの読み取りを禁止） |
| `.github/` | Issue / PR テンプレート |

## 注意

- `CLAUDE.md` やそこから `@` で読み込むファイルは毎回コンテキストに展開されます。`@` は常時必要なものだけに付けてください。
