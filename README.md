# MikanOS Book

- [MikanOS](https://github.com/uchan-nos/mikanos) の練習レポジトリ

## 環境構築

macOS 前提

- X11 サーバをホストマシンにインストール

```bash
$ brew install --cask xquartz
```

- `XQuartz` の環境設定 > セキュリティタブ > 「ネットワーク・クライアントからの接続を許可」にチェックを入れる
- `XQuartz` を再起動して、ローカルからの接続許可を追加する

```bash
$ killall Xquartz && open -a Xquartz
$ xhost + localhost
```

- Dev Container 起動

```bash
$ devcontainer open .
```

## バイナリエディタ (Okteta)

- コンテナから以下のコマンドを実行

```bash
$ okteta
```

> [!TIP]
> - ウィンドウ右下端の 〼 のような部分をドラッグすることでウィンドウサイズの調整を行うことができる
> - Ctrl + + , Ctrl + - でエディタパネルの拡大縮小ができる
