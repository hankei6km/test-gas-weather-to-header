# test-gas-weather-to-header

`https://www.jma.go.jp/bosai/forecast/` の `https://www.jma.go.jp/bosai/forecast/data/forecast/130000.json` から情報を取得し、Noteion のページ(データベース)ヘッダーへ設定する GAS 用スクリプト。

## 使い方

1. Google Apps Script プロジェクトを作成
1. ライブラリーを追加
    1. コードエディターのファイル名一覧が表示される部分の「ライブラリ +」をクリック
    1. 「スクリプト ID」フィールドに `1aNOkTIUB6u8WQmBydsnFh6Yjh5FsZ1U1b-1cre8Oo5b0hEgwyDquolYv` を入力し検索をクリック
    1. バージョンを選択(通常は最新版)
    1. 「ID」を `UpdateHeader` へ変更
    1. 「追加」をクリック
1. `code.js` の内容を `コード.gs` へ貼り付ける
1. スクリプトプロパティへ以下を追加する
    - `notion_api_key` - Notion のインテグレーション
    - `notion_page_id` - ヘッダーを更新するページ(またはデータベース)の id
1. 確認のために実行する
    - 権限の確認などを求められるで内容を確認し許可する

更新対象のページでタイトルが変更されたことを確認したら、時間指定のトリガーを設定すると定期的に更新される。


## 備考

このスクリプト作成当初は Unsplash Source を利用してカバー画像も更新していたが、サービスが停止されたので該当部分はコメントアウトしてある。他に Notion のサーバーから画像を参照できる URL を提供している API サービスがあれば、そちらを利用することで天気の内容にあわせてカバー画像を更新できるかもしれない。


## License

MIT License

Copyright (c) 2024 hankei6km

