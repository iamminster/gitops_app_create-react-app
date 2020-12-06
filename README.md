# create-react-app_gke
create-react-appをGKE上にデプロイするサンプルリポジトリです。

# ローカル環境構築手順

## ビルド
```
docker-compose build
```

## node_moduleインストール

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

ビルド
```
docker-compose build
```

コンテナ一時起動
```
docker-compose run --rm node sh
```

コンテナ内でアプリ新規作成
```
create-react-app .
```

終わったらコンテナ終了
```
exit
```