# parts-location-search

部品在庫の棚位置検索ページです。GitHub Pages ではリポジトリ直下の `index.html` を公開します。

## GitHub Pages 公開手順

このリポジトリには `.github/workflows/pages.yml` を同梱しており、`main` への push で自動公開されます。

1. GitHub の `Settings` > `Pages` を開きます。
2. `Build and deployment` の `Source` を `GitHub Actions` にします。
3. `main` ブランチに変更を push すると、`Deploy to GitHub Pages` ワークフローが走り、公開されます。
4. 公開URLは次の形式です。

```text
https://<GitHubユーザー名>.github.io/parts-location-search/
```

`Actions` タブのワークフロー結果に表示される `page_url` からも確認できます。

> 旧来の `Deploy from a branch`（`main` / `/ (root)`）でも `index.html` と `.nojekyll` のみで公開可能です。その場合はワークフローは不要です。

## GAS 連携確認

`index.html` 内の `GAS_URL` は現在設定済みです。

GitHub Pages で公開後、ページを開いて次を確認します。

- 通報リストが読み込まれる
- 検索結果の `通報` ボタンでスプレッドシートへ追加される
- `取消` でスプレッドシート上の通報が削除される

うまく動かない場合は、GAS 側の Web アプリ公開設定で「アクセスできるユーザー」が `全員` または用途に合う範囲になっているか確認してください。
