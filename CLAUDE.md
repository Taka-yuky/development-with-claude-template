# CLAUDE.md

> このファイルはAI/開発者の入口です。`【要記入】` の箇所をプロジェクトに合わせて埋めてください。
> 詳細な情報は `docs/` に置き、ここには「常に読ませたい要点」だけを書きます。
> `@` で読み込んだファイルは毎回コンテキストに展開されるため、`@` は本当に常時必要なものだけに付けてください。

## Project Memory

Product Goal: 【要記入】このプロダクトが達成したいことを1文で（詳細は `docs/PRODUCT.md`）

常に読み込むドキュメント:
@docs/INDEX.md
@docs/DEVELOPMENT_RULES.md

その他のドキュメントは `docs/INDEX.md` の Reading Guide に従い、作業内容に応じて読むこと。

## AIへの注意事項

### 禁止事項

- `docs/DEVELOPMENT_RULES.md` の「やってはいけないこと」を正本とする
- git の commit / push は `.claude/settings.json` の `permissions.deny` でも禁止している

### 実装前の確認事項

- `docs/REQUIREMENTS.md` と `docs/ARCHITECTURE.md` を確認してから実装する
- 認証・データを扱う実装では `docs/SECURITY.md` を確認する
- 【要記入】例: 要件が曖昧な場合は実装前に質問する

### テスト要件

- 【要記入】例: 新規ロジックには必ずテストを書く（詳細は `docs/TEST_STRATEGY.md`）

### 実装完了後の必須作業

- 【要記入】例: テスト・Lintの実行、関連docsの更新（`docs/DEVELOPMENT_RULES.md` のドキュメント更新ルール参照）

## クイックコマンド

> 【要記入】利用する言語・ツールに合わせて書き換える。以下は記入例。

```bash
# 開発サーバ起動
<command>

# テスト実行
<command>

# Lint / フォーマット
<command>

# ビルド
<command>
```
