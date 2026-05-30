# parts-location-search — 開発者ガイド

[← README に戻る](./README.md)

## 構成

| ファイル | 役割 |
|---|---|
| `index.html` | メイン検索ページ |
| `parts-location-search.html` | 別エントリポイント（旧版互換） |
| `.nojekyll` | GitHub Pages で Jekyll を無効化 |

バックエンドは Google Apps Script（GAS）の Web アプリとして別途デプロイします。  
`index.html` 内の `GAS_URL` 定数にデプロイ済みの URL を設定してください。

## GitHub Pages 公開手順

このリポジトリには `.github/workflows/pages.yml` を同梱しており、`main` への push で自動公開されます。

1. GitHub の `Settings` > `Pages` を開く
2. `Build and deployment` の `Source` を `GitHub Actions` に設定
3. `main` ブランチに変更を push すると `Deploy to GitHub Pages` ワークフローが動く
4. 公開 URL の形式:

```
https://165cm.github.io/parts-location-search/
```

`Actions` タブのワークフロー結果に表示される `page_url` からも確認できます。

> 旧来の `Deploy from a branch`（`main` / `/ (root)`）でも `index.html` と `.nojekyll` のみで公開可能です。その場合はワークフローは不要です。

## GAS 連携確認

`index.html` 内の `GAS_URL` は設定済みです。

GitHub Pages で公開後、ページを開いて次を確認してください。

- 通報リストが読み込まれる
- 検索結果の「通報」ボタンでスプレッドシートへ追加される
- 「取消」でスプレッドシート上の通報が削除される

うまく動かない場合は、GAS 側の Web アプリ公開設定で「アクセスできるユーザー」が `全員` または用途に合う範囲になっているか確認してください。

## コミット規約

[中央マニュアル commits.md](https://github.com/165cm/portfolio/blob/main/docs/standards/commits.md) に従ってください。
