# Nuxt-Docker
自身の環境を汚すことなくDockerにNuxt.js環境を構築します。  
(少しNuxt.jsを触って見たい方向け)

環境
- Mac Mojave 10.14.6
- Docker version 19.03.1, build 74b1e89
- docker-compose version 1.24.1, build 4667896b

## Required
[こちら](https://www.docker.com/products/docker-desktop)からDocker For Macのインストール  

※インストール方法に関しては[ドキュメント](https://docs.docker.com/docker-for-mac/install/)を参照ください。

## Usage
ターミナルを開き、下記コマンドで環境を構築します。
```
# コード配置
$ git clone https://github.com/tkdev01/nuxt-docker.git
$ cd nuxt-docker

# dockerイメージを構築する
$ docker-compose build

# コンテナを起動する
$ docker-compose up -d

# アクセス
$ open http://localhost:3000/
```

### Nuxt.jsの構築内容
```
create-nuxt-app v2.9.2
✨  Generating Nuxt.js project in .
? Project name nuxt-sample
? Project description sample
? Author name sample
? Choose the package manager Yarn
? Choose UI framework Bootstrap Vue
? Choose custom server framework None (Recommended)
? Choose Nuxt.js modules (Press <space> to select, <a> to toggle all, <i> to invert selection)
? Choose linting tools (Press <space> to select, <a> to toggle all, <i> to invert selection)
? Choose test framework None
? Choose rendering mode Universal (SSR)
```

## その他コマンド
```
# サーバーログの確認
$ docker-compose logs -f --tail 10 nuxt.js

# サーバの状態確認
$ docker-compose ps

# コンテナを落とす
$ docker-compose down
```

## ディレクトリ構成
```
Nuxt-sample
├── docker-compose.yml
└── web
    ├── Dockerfile
    └── app
        ├── Nuxt.jsのソース
        ├── ...
```