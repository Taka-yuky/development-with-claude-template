# development-with-claude-template

## このリポジトリの役割

Claude Codeをcoding agentとして利用する場合のテンプレートリポジトリです。
このリポジトリをテンプレートとして、各プロジェクトの開発を始めましょう！

## 使い方

1. このテンプレートからリポジトリを作成する
2. `CLAUDE.md` と `docs/` 配下の `【要記入】` を埋める（`grep -rn "【要記入】" CLAUDE.md docs` で残りを確認できる）
3. `docs/options/` から必要なドキュメントだけ `docs/` へ移動し、`docs/INDEX.md` に反映する（使わないものは削除）
4. 設計判断は `docs/adr/000-template.md` をコピーして `docs/adr/001-xxx.md` のように記録する
