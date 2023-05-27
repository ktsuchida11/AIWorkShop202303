# AIWorkShop202303

個人のM1 MacではChatGPTのモジュールがうまく動かなかったのでコンテナにして動作を確認した

## コンテナの内容

- Chat GPT API接続するRESTAPIを作成
- 金融に関するデータを取得するためのRESTAPIを作成

## 初期設定

ChatGPT API接続　: https://platform.openai.com/
.envファイルをDataSourceAPI直下に作成してAPI_KEYを登録する

金融に関するデータを取得
データソースによってはAPI_KEYの取得が必要なものがあるので適宜追加する

## 使い方

Dockerが起動していることが前提条件

```
# コンテナの起動
DataSourceAPI $docker-compose build
DataSourceAPI $docker-compose up -d 

# sample request
DataSourceAPI $ curl -X POST localhost:8002/chatGPT -H "Content-Type: application/json" -d '{"role": "user", "content": "Hello!"}'

````
