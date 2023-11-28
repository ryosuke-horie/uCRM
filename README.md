# docker_php-nginx-pgsql

## 開発環境用Docker
開発用に使用するDockerを構築します。
Nginx, PHP, PostgresQLを入れた汎用的な開発環境を用意します。

## 手順
1. docker compose up -d
2. docker exec -it docker_php-nginx-pgsql-web-1 bash
3. composer create-project "laravel/laravel=8.*" webApp
4. docker compose down
5. docker compose up -d
6. docker exec -it docker_php-nginx-pgsql-web-1 bash
7. chmod -R 777 strage/
8. localhost:8888 にアクセスするとLaravelのウェルカムページが表示される。

## メモ
今持っているPCのスペック的にLaravelプロジェクト作成時に4つほどインストールエラーが発生する。
エラーが発生したら、`composer install`を実行すると解決可能。