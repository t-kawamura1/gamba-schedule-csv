1. 最初のイメージ立ち上げコマンド：

ワーキングディレクトリの指定（-w /home/app）コンテナを命名(--name pptr)、権限設定（--cap-add=SYS_ADMIN）、バインドマウント（-v /Users/tkawamura/javascript/soccer-schedule:/home/app）、イメージ名指定、bash立ち上げ
```bash
$ docker run -it -w /home/app --name pptr --cap-add=SYS_ADMIN -v /Users/tkawamura/javascript/soccer-schedule:/home/app  ghcr.io/puppeteer/puppeteer:19.5.2 bash
```

2. プロジェクト作成
```bash
$ npm init -y
```

3. puppeteerインストール
```bash
$ npm i puppeteer
```

4. csv-parseインストール
```bash
$ npm i csv-parse
```

5. iconv-liteインストール(Shift-JISのCSVを開く場合は必要、今回は不要)
```bash
$ npm i iconv-lite
```

6. 起動済みコンテナのbash立ち上げコマンド
```bash
$ docker exec -it -w /home/app pptr bash
```

7. スクリプト実行コマンド
```bash
$ node gamba-schedule.js
```