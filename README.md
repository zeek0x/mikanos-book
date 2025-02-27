# MikanOS Book

- [MikanOS](https://github.com/uchan-nos/mikanos) の練習レポジトリ

## 環境構築

### 構成

```plaintext
+-------------------------- Host (macOS) --------------------------+
| +------- XQuartz --------+      +----------- OrbStack ---------+ |
| | +--- Qemu Window ---+  |      | +--- Container (Ubuntu) ---+ | |
| | |                   |  |      | |      +--- Qemu ---+      | | |
| | |  [Hello, World!]  |<-------X11-------|  $ qemu    |      | | |
| | |                   |  |      | |      +------------+      | | |
| | +-------------------+  |      | |                          | | |
| |                        |      | |                          | | |
| | +-- Okteta Window ---+ |      | |                          | | |
| | | 00 00 ff ff 01 02  | |      | |     +--- Okteta ---+     | | |
| | | 00 00 ff ff 01 02  |<-------X11-----|  $ okteta    |     | | |
| | | 00 00 ff ff 01 02  | |      | |     +--------------+     | | |
| | +--------------------+ |      | +--------------------------+ | |
| +------------------------+      +------------------------------+ |
+------------------------------------------------------------------+
```

### 手順

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

### バイナリエディタ (Okteta) を起動

- コンテナから以下のコマンドを実行

```bash
$ okteta
```

> [!TIP]
> - ウィンドウ右下端の 〼 のような部分をドラッグすることでウィンドウサイズの調整を行うことができる
> - Ctrl + + , Ctrl + - でエディタパネルの拡大縮小ができる

## トラブルシューティング

### XQuartz が起動しない

起動しても数秒でアプリケーションが終了してしまう場合は `.xinitrc` を削除（または退避）させて再起動する。

### xhost:  unable to open display

`xhost + localhost` を実行時にこのエラーが表示される場合、`DISPLAY` 環境変数が設定されてないことが原因なので設定する。

```console
$ export DISPLAY=:0.0
```

### bash: build: command not found

`build` は edksetup.sh が提供しているので読み込み直す

```
$ cd $HOME/edk2
$ source edksetup.sh
Loading previous configuration from /home/vscode/edk2/Conf/BuildEnv.sh
Using EDK2 in-source Basetools
WORKSPACE: /home/vscode/edk2
EDK_TOOLS_PATH: /home/vscode/edk2/BaseTools
CONF_PATH: /home/vscode/edk2/Conf
```
