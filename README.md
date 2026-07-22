# Rails Ajax Task

「Webエンジニア ステップアップコース（Ruby）」で使用する、
お気に入り機能のAjax化を学ぶためのRailsアプリケーションです。

## Requirements

- Ruby 4.0.5
- Bundler 4.0.10
- Ruby on Rails 8.1.3
- PostgreSQL 18.4
- Node.js 24.18.0
- Yarn 1.22.22

## Setup

```sh
bundle install
yarn install --frozen-lockfile
bundle exec rails db:prepare
```

`bin/setup`でもRuby Gem、JavaScriptパッケージ、データベースをまとめて準備できます。

## Start the server

```sh
bundle exec rails server
```

既定では <http://localhost:3000> で起動します。

## Test

```sh
bundle exec rails test
bundle exec rspec
```

GitHub Actionsでは、課題評価用のRSpecを別リポジトリから取得して実行します。

## Environment variables

ローカル開発では通常、環境変数の設定は不要です。必要に応じて次を設定します。

- `DATABASE_URL`: PostgreSQL接続URL
- `RAILS_MAX_THREADS`: PumaとActive Recordの最大スレッド数
- `PORT`: Railsサーバーの待受ポート
- `RAILS_MASTER_KEY`: productionで暗号化credentialsを利用する場合のmaster key
- `rails_ajax_task_DATABASE_PASSWORD`: `DATABASE_URL`を使わないproduction接続のパスワード
