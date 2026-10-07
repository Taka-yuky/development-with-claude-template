# Documentation Index

AIと人間が共通で使うドキュメントの入口です。
まずここを読み、目的に応じて各ドキュメントへ移動してください。

> **テンプレート利用者へ**: 各ドキュメントの `【要記入】` を埋め、`【要確認】` の前提がプロジェクトに当てはまるか確認してください（当てはまらない記述は削除）。
> `docs/options/` 配下は必要なものだけ `docs/` 直下へ移動して使うオプションのドキュメントです（詳細は `docs/options/README.md`）。
> 使わないドキュメントはこのINDEXからも削除してください。
>
> **注意**: このファイルは `CLAUDE.md` から `@` で常時読み込まれます。ここで `@` を使うとリンク先も毎回読み込まれてしまうため、パスは通常の表記で書いてください。

## 0. Start Here

- `CLAUDE.md` — AI/開発者の入口（概要・ルール・クイックコマンド）
- `docs/PRODUCT.md` — プロダクト概要（誰の・何を・なぜ）
- `docs/REQUIREMENTS.md` — 要件と受け入れ基準の正本

## 1. Development Rules（開発の進め方）

- `docs/DEVELOPMENT_RULES.md` — タスクの管理・進め方・完了の定義・禁止事項（常時読み込み）

## 2. Architecture（どう作るか）

- `docs/ARCHITECTURE.md` — システム境界・依存ルール・設計パターン
- `docs/TECHNICAL_STACK.md` — 採用技術・バージョン
- `docs/adr/` — 設計判断の記録（ADR）
- `docs/diagrams/` — 図（ソースは `src/*.d2`、生成物は `svg/*.svg`）

オプション（`docs/options/` から必要に応じて移動して利用）:

- `docs/options/DATA_MODEL.md` — エンティティ・スキーマ・マイグレーション方針
- `docs/options/API_CONTRACTS.md` — APIエンドポイント・エラー形式・バージョニング
- `docs/options/FRONTEND_STRUCTURE.md` — フロントエンドのディレクトリ構成・ファイル役割
- `docs/options/FRONTEND_CODE_GUIDE.md` — フロントエンドのコード構成・パターン・データフロー

## 3. Engineering Standards（品質・運用）

- `docs/DEV_WORKFLOW.md` — ブランチ・コミット・PR・CI・リリース
- `docs/QUALITY.md` — コード品質基準・レビュー・ロギング
- `docs/TEST_STRATEGY.md` — テスト範囲・モック方針
- `docs/SECURITY.md` — 脅威モデル・認証認可・入力検証・シークレット管理

## 4. Human Docs（人間向け）

- `docs/human/` — 人間が読むためのドキュメント置き場（例: オンボーディング、運用手順）。AIが常に参照する対象ではない

---

## Reading Guide（目的別）

### 機能を実装したい

1) `docs/REQUIREMENTS.md`
2) `docs/ARCHITECTURE.md`
3) `DATA_MODEL.md` / `API_CONTRACTS.md`（使っている場合）
4) `docs/TEST_STRATEGY.md`
5) `docs/SECURITY.md`（認証・データを扱う場合）

### 要件を変更したい

1) `docs/REQUIREMENTS.md`
2) `docs/adr/` に判断を追記
3) テストと実装を更新

### 本番障害を調査したい

1) `docs/SECURITY.md`（認証・データ関連の場合）
2) `docs/ARCHITECTURE.md`
3) 【要記入】RUNBOOK.md を作成したらここに追加

### PRをレビューしたい

- `docs/QUALITY.md`
- `docs/DEV_WORKFLOW.md`
