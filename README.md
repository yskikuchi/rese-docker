# プロジェクト名

Rese（リーズ）

## 概要

Rese グループの飲食店予約サービスです。

デモページ: https://rese-lara-nuxt.herokuapp.com

## 機能一覧

### ユーザー

-   会員登録・ログイン
    -   新規会員登録時のメール認証
-   飲食店一覧を表示
    -   ジャンル・エリア・店名で絞り込み
-   お気に入り店舗登録・削除
-   予約機能
    -   日時・人数を指定して予約
    -   予約の削除
    -   予約の変更
-   Stripe による事前決済機能
-   訪れた飲食店の評価機能

### 店舗代表者

-   店舗情報の作成・更新
-   店舗の予約確認
-   店舗画像の追加
-   予約者へのメール送信機能

### 管理者

-   上記店舗代表者の機能
-   店舗代表者の作成

## 環境

-   Docker 20.10.12
-   PHP 7.4.1
-   laravel 8.81.0
-   Nodejs 14.15.0
-   Nuxt v2.15.8
-   MySQL 8.0.28

## インストール

```
$ git clone https://github.com/yskikuchi/rese-docker
$ cd rese-docker
$ cp .env.local.example .env
```
.envに必要情報を入力

### 1. Nuxt

```
$ cd nuxt/
$ yarn install

$ cp .env.local.example .env
```

### 2. laravel

```
$ docker compose up -d
```

```
$ cd src
$ composer install
$ cp .env.local.example .env

$ php artisan key:generate
```

.envファイルのデータベースを修正後

```
$ docker compose exec php /bin/bash
$ php artisan migrate
$ php artisan db:seed
```


### 3. localhostにアクセス

localhostで{WEB_PORT}、{FRONT_PORT}で設定したポート番号を使用してアクセスしてください。

