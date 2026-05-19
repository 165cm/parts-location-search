# parts-location-search

部品在庫の棚位置検索ページです。GitHub Pages ではリポジトリ直下の `index.html` を公開します。

## GitHub Pages 公開手順

1. GitHub に新規リポジトリ `parts-location-search` を作成します。
2. このフォルダをそのリポジトリへ push します。
3. GitHub の `Settings` > `Pages` を開きます。
4. `Build and deployment` の `Source` を `Deploy from a branch` にします。
5. `Branch` を `main`、フォルダを `/ (root)` にして `Save` します。
6. 数分後、以下の形式で公開されます。

```text
https://<GitHubユーザー名>.github.io/parts-location-search/
```

## GAS 連携確認

`index.html` 内の `GAS_URL` は現在設定済みです。

GitHub Pages で公開後、ページを開いて次を確認します。

- 通報リストが読み込まれる
- 検索結果の `通報` ボタンでスプレッドシートへ追加される
- `取消` でスプレッドシート上の通報が削除される

うまく動かない場合は、GAS 側の Web アプリ公開設定で「アクセスできるユーザー」が `全員` または用途に合う範囲になっているか確認してください。
