# 画像をアプロードして、ドット絵に変換するアプリ

## 環境構築

### 各種バージョン

- フロントエンド
  - Vue ^3.4.21
- バックエンド
  - Python ^3.12
  - FastAPI ^0.110.3

### 起動方法

#### 前提

- パッケージ管理用の node.js と poetry がインストール済みであること(私の実行環境は、node: v20.10.0、poetry: version 1.8.2)
- IDE は、Visual Studio Code(以下略、VSCode)を使用すること

### ソースのクローン

GitHub からソースをクローンし、以下の作業はクローンしたルート階層で行うこと

### パッケージのインストール

VSCode の上部メニューから、「ターミナル(T)」　 → 　「タスクの実行」　 → 　「dev」　 → 　「タスクの出力をスキャンせず実行」

### アプリケーションの実行

VSCode の「実行とデバッグ(Ctrl + Shift + D)」を開き、「App」を選択して実行する  
フロントエンドとバックエンドの local 環境が起動するので「[http://localhost:5173/](http://localhost:5173/)」にアクセスする

## 使用方法

1. 「UPLOAD IMAGE FILE(JPG OR PNG)」と記載されているインプット要素をクリックし、アップロードする画像を選択する(アイコン画像向けに設定しているため、正方形に近いサイズの画像推奨)
2. 「SHOW IMAGE」ボタンをクリックする
3. 表示された画像の下部のバーで変換する画像の粒度を選択する（デフォルトは 10px）
4. 「CONVERT TO PIXEL」ボタンをクリックする
5. 「DOWNLOAD IMAGE」ボタンをクリックすると、変換した画像をダウンロードできる

## Docker で起動する

1. DockerDesktop をインストールしておく
2. ソースをクローンする
3. `docker compose build`
4. `docker compose up`
5. [http://localhost:5173/](http://localhost:5173/)にアクセスする
