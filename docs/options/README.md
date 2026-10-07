# docs/options

プロジェクトによって必要性が変わるドキュメントの雛形です。
使うものだけ `docs/` 直下へ移動（または `git mv`）し、`docs/INDEX.md` に追記してください。
使わないものは削除して構いません。

| ファイル | 使う場面 |
|---|---|
| `DATA_MODEL.md` | DBを持つプロジェクト。エンティティ・制約の背景を残す |
| `API_CONTRACTS.md` | APIを提供するプロジェクト。エンドポイント仕様を残す |
| `FRONTEND_STRUCTURE.md` | フロントエンドを持つプロジェクト。ディレクトリ構成を残す |
| `FRONTEND_CODE_GUIDE.md` | フロントエンドの設計パターン・データフローを説明したい場合 |

移動後は `CLAUDE.md` や `DEVELOPMENT_RULES.md` の参照先（`DATA_MODEL.md` / `API_CONTRACTS.md` 等）も確認してください。
