# Rails + PostgreSQL Docker 環境構築手順

## 前提条件

- Docker / Docker Compose がインストールされていること

## 手順

1. リポジトリをクローン
   `git clone https://github.com/あなたのユーザー名/rails-docker.git`
2. クローンしたディレクトリへ移動
   `cd rails-docker`
3. コンテナをビルド＆起動
   `docker-compose up -d --build`
4. 初回のみマイグレーションを実行
   `docker-compose exec web bin/rails db:migrate`
5. 以下 URL にブラウザでアクセスし動作確認
   `http://localhost:3000`
   "Tasks New task" と表示されれば OK
