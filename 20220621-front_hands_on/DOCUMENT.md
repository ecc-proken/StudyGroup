# Webサーバハンズオン - フロントエンド編

４年生が実際に制作しているWebサイトを使用したハンズオンです。  
`JavaScript`とそのフレームワークである`Next.js`を使用します。

## 前提

- Git [インストール資料](/articles/git_hands_on#Git%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)
- VSCode [インストール資料](/articles/git_hands_on#VSCode%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)

## 準備

### 　Node.jsとnpm

- `Node.js`
    - サーバーサイド（Webサイトなど）で`JavaScript`を使用する場合に使うWeb開発フレームワーク
- `npm`
    - JavaScriptのパッケージ管理ツール

#### DL

[Node.js](https://nodejs.org/)

<img src="./img/62aac2b21444fb8b12494482.png" style="width:640px;"/>

#### インストール

<img src="./img/62aac2e01444fb8b124944df.png" style="width:640px;"/>

<img src="./img/62aac3291444fb8b12494569.png" style="width:640px;"/>

### yarn

`yarn`は`JavaScript`のパッケージ管理ツールで`npm`と用途は同じ

今回使用するWebサイトのプロジェクトをDLしたいフォルダを`GitBash`で開く

<img src="./img/62aac4421444fb8b124947ef"/>

#### インストール

`yarn`をインストール

```bash
npm install -g yarn
```

<img src="./img/62aac4761444fb8b1249483d.png" style="width:640px;"/>

## 実践

[リポジトリ：ecc-proken/prc_hub-front](https://github.com/ecc-proken/prc_hub-front)

### GitHubからDL

さっき開いた`GitBash`で

```bash
git clone https://github.com/ecc-proken/prc_hub-front.git
```

<img src="./img/62aac4fb1444fb8b1249498a.png" style="width:640px;"/>

<img src="./img/62aac5111444fb8b124949c0.png" style="width:640px;"/>

エクスプローラからも確認できる

<img src="./img/62aac54d1444fb8b12494a1d.png" style="width:640px;"/>

VSCodeで開く

<img src="./img/62aac5fc1444fb8b12494ae9.png" style="width:940px;"/>

### windowsではそのまま実行できないため専用の設定をする。

ここからはコマンドを`VSCode`上の`GitBash`で実行してください。

↓のコマンドを全部コピーし、一度に実行する。

```bash
echo "/** @type {import('next').NextConfig} */
const nextConfig = {
  reactStrictMode: true,
  experimental: {
    outputStandalone: true,
  },
  swcMinify: false,
}

module.exports = nextConfig" > next.config.js
echo '{
    "presets": ["next/babel"]
}' > .babelrc
```


<img src="./img/62aac65b1444fb8b12494b7c.png" style="width:940px;"/>

### Webサーバアプリケーションを動かしてみる

#### 必要パッケージのDL

```bash
yarn
```

<img src="./img/62aac71c1444fb8b12494c98.png" style="width:640px;"/>

<img src="./img/62aac7201444fb8b12494cb6.png" style="width:640px;"/>

#### 環境変数の設定

`NEXT_PUBLIC_API_URL`という環境変数を`.env.local`というファイルに記述

```bash
echo "NEXT_PUBLIC_API_URL=https://prchub.tingtt.jp" > .env.local
```

#### 起動

```bash
yarn dev
```

<img src="./img/62aac74e1444fb8b12494cf8.png" style="width:640px;"/>

<img src="./img/62aac7511444fb8b12494d16.png" style="width:640px;"/>

#### 見てみよう！

http://localhost:3000/

<img src="./img/62aac8691444fb8b12494ed8.png" style="width:640px;"/>

<img src="./img/62aac86d1444fb8b12494ee7.png" style="width:640px;"/>

#### 止める

止めるときは`ctrl + c`

<img src="./img/62aac8bb1444fb8b12494f5f.png" style="width:640px;"/>

お疲れさまでした。