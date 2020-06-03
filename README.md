# kitolab

> Labo homepage

## Build Setup（開発の流れ）

- node.jsがインストールされている事が条件

```bash
# install dependencies
# 依存パッケージのインストール
# 一番最初に行う
$ npm install

# serve with hot reload at localhost:3000
# ホットリロード状態で実行
# このコマンドを実行してからブラウザでlocalhost:3000にアクセスするとサイトにアクセスできる。この状態でファイルを変更すると即座にブラウザ上のプレビューに反映される。
$ npm run dev

# build for production and launch server
# 使わないから無視
$ npm run build
$ npm run start

# generate static project
# 静的ファイルに出力
# これを実行するとファイルが./dist以下に展開されるので、その中身をFTP等で研究室ホームページのサーバーにアップロードする。
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
