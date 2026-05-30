# AI Coding Agent Guide

このリポジトリでの開発作法は、**中央マニュアル** に従ってください。

📘 中央マニュアル: https://github.com/165cm/portfolio/tree/main/docs/standards

- [tiers.md](https://github.com/165cm/portfolio/blob/main/docs/standards/tiers.md) — 作品ティア
- [commits.md](https://github.com/165cm/portfolio/blob/main/docs/standards/commits.md) — コミット規約
- [readme-template.md](https://github.com/165cm/portfolio/blob/main/docs/standards/readme-template.md) — README 規約
- [developer-template.md](https://github.com/165cm/portfolio/blob/main/docs/standards/developer-template.md) — DEVELOPER 規約
- [topics.md](https://github.com/165cm/portfolio/blob/main/docs/standards/topics.md) — Topics 規約
- [ops.md](https://github.com/165cm/portfolio/blob/main/docs/standards/ops.md) — その他運用ルール

## このリポジトリ固有の情報

- **Tier**: T1（趣味公開）
- **Category**: work
- **特有の制約**: バックエンドは Google Apps Script（GAS）Web アプリ。`GAS_URL` 定数の変更はスプレッドシート連携に直結するため慎重に扱うこと。フロントエンドは純粋な静的 HTML/JS のみ（ビルドツールなし）。

## このリポジトリでよく使うコマンド

```bash
# ビルドツールなし。ファイルを直接編集し、GitHub Pages で確認する。
# ローカルで確認したい場合は任意の静的サーバを使う:
npx serve .
# または
python3 -m http.server 8080
```
