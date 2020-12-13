# gitops_app_create-react-app
GitOpsのアプリリポジトリのサンプルです。

こちらのQiita記事で使用しています。  
https://qiita.com/Nishi53454367/items/4a4716dfbeebd70295d1

# ローカル環境構築手順

## ビルド
```
docker-compose build
```

## node_modulesインストール

コンテナ一時起動
```
docker-compose run --rm node sh
```

コンテナ内でnode_modulesインストール
```
yarn install
```

終わったらコンテナ終了
```
exit
```

## コンテナ起動
```
docker-compose up -d
```

## 画面起動
http://localhost:3000

# 備忘録: アプリ新規作成手順

## ビルド
```
docker-compose build
```

## コンテナ一時起動
```
docker-compose run --rm node sh
```

## コンテナ内でアプリ新規作成
```
create-react-app .
```

## 終わったらコンテナ終了
```
exit
```