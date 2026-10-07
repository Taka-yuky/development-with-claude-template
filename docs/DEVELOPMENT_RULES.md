# DEVELOPMENT_RULES.md

## タスク管理

> 【要記入】利用するタスク管理ツール（GitHub Issues / Backlog / Jira 等）に合わせて編集する。

- タスクは【要記入: ツール名】のissueで管理する
- 各issueに対して `f/<issue番号>` ブランチを切って作業する
- 作業開始前にissueのステータスを「処理中」に更新する
- PR作成時にissueをリンクする
- 作業後のステータス変更は人が行う

## チケット起票ルール

- **人間が明示的に依頼した場合のみ**起票する（AIが自律的に起票しない）
- 起票の方法: 【要記入】（例: MCP経由 / GitHub Web UI）
- テンプレート: `.github/ISSUE_TEMPLATE/`（GitHub以外のツールを使う場合は削除・置き換え）

| 種別 | 使用場面 |
|---|---|
| タスク | 機能実装・改善・ドキュメント更新など |
| バグ | 不具合修正 |

## 開発の進め方

1. **要件確認** — REQUIREMENTS.md・PRODUCT.md を確認する
2. **設計確認** — ARCHITECTURE.md などを参照する
3. **実装** — ブランチを切って実装する
4. **テスト** — テストを書いて通す
5. **PR作成** — レビューを依頼する
6. **マージ** — 承認後にmainへマージする

## AIへのタスク依頼

依頼前に以下のドキュメントをAIに参照させること:

- REQUIREMENTS.md（何を作るか）
- ARCHITECTURE.md（どう作るか）
- 【要記入】DATA_MODEL.md / API_CONTRACTS.md など、使っているもの

## ドキュメントの更新ルール

- 機能追加・変更時は関連するdocsも同時に更新する
- 要件の変更は `REQUIREMENTS.md` を更新し、背景を `docs/adr/` に残す
- 【要記入】API仕様・データモデルのドキュメントを使う場合は、その更新ルールも追記する

### 図の書き方

- 構成図・データフロー図・ER図などの図は [D2](https://d2lang.com/) で書く
- ソースと生成物はディレクトリを分ける。ファイル名（拡張子を除く）は両者で揃える

  ```
  docs/diagrams/
  ├── src/   # D2ソース（<図の名前>.d2）。編集するのはこちらのみ
  └── svg/   # 生成したSVG（<図の名前>.svg）。手で編集しない
  ```

- SVG は以下で生成し、ソースと一緒にGit管理する
  ```bash
  # 1つだけ生成
  d2 docs/diagrams/src/<図の名前>.d2 docs/diagrams/svg/<図の名前>.svg

  # すべて再生成
  for f in docs/diagrams/src/*.d2; do d2 "$f" "docs/diagrams/svg/$(basename "${f%.d2}").svg"; done
  ```
- ドキュメントからは SVG を埋め込み（例: `![構成図](diagrams/svg/<図の名前>.svg)`）、ソースの `.d2` へのパスも併記する
- 図を変更・削除するときは `src/` と `svg/` の両方を揃える（片方だけ残さない）

## やってはいけないこと

> 禁止事項の正本。`CLAUDE.md` からはここを参照する。
> AIによる commit / push は `.claude/settings.json` の `permissions.deny` でも禁止している。

- `main` ブランチへの直接push
- テストなしでのマージ
- 機密情報（パスワード、APIキー）のGitへのコミット
- 【要確認: マルチテナントの場合】他のアカウント/組織のデータを参照するコード（データ分離の原則）
- AIによる作業後のcommit（commitは人間が行う）
