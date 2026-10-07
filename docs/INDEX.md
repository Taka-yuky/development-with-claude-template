# Documentation Index

AIと人間が共通で使うドキュメントの入口です。
まずここを読み、目的に応じて各ドキュメントへ移動してください。

> **テンプレート利用者へ**: 各ドキュメントの `【要記入】` を埋めてください。
> `docs/options/` 配下は必要なものだけ `docs/` 直下へ移動して使うオプションのドキュメントです（詳細は `docs/options/README.md`）。
> 使わないドキュメントはこのINDEXからも削除してください。

## 0. Start Here

- @../CLAUDE.md — AI/開発者の入口（概要・ルール・クイックコマンド）
- @./PRODUCT.md — プロダクト概要（誰の・何を・なぜ）
- @./REQUIREMENTS.md — 要件と受け入れ基準の正本

## 1. Development Rules（開発の進め方）

- @./DEVELOPMENT_RULES.md — タスクの管理・進め方・完了の定義

## 2. Architecture（どう作るか）

- @./ARCHITECTURE.md — システム境界・依存ルール・設計パターン
- @./TECHNICAL_STACK.md — 採用技術・バージョン
- @./adr/ — 設計判断の記録（ADR）

オプション（`docs/options/` から必要に応じて移動して利用）:

- `options/DATA_MODEL.md` — エンティティ・スキーマ・マイグレーション方針
- `options/API_CONTRACTS.md` — APIエンドポイント・エラー形式・バージョニング
- `options/FRONTEND_STRUCTURE.md` — フロントエンドのディレクトリ構成・ファイル役割
- `options/FRONTEND_CODE_GUIDE.md` — フロントエンドのコード構成・パターン・データフロー

## 3. Engineering Standards（品質・運用）

- @./DEV_WORKFLOW.md — ブランチ・コミット・PR・CI・リリース
- @./QUALITY.md — コード品質基準・レビュー・ロギング
- @./TEST_STRATEGY.md — テスト範囲・モック方針
- @./SECURITY.md — 脅威モデル・認証認可・入力検証・シークレット管理

## 4. Human Docs（人間向け）

- `human/` — 人間が読むためのドキュメント置き場（例: オンボーディング、運用手順）。AIが常に参照する対象ではない

---

## Reading Guide（目的別）

### 機能を実装したい

1) REQUIREMENTS.md
2) ARCHITECTURE.md
3) DATA_MODEL.md / API_CONTRACTS.md（使っている場合）
4) TEST_STRATEGY.md

### 要件を変更したい

1) REQUIREMENTS.md
2) `adr/` に判断を追記
3) テストと実装を更新

### 本番障害を調査したい

1) SECURITY.md（認証・データ関連の場合）
2) ARCHITECTURE.md
3) 【要記入】RUNBOOK.md を作成したらここに追加

### PRをレビューしたい

- QUALITY.md
