
# coffee-mode for xyzzy

CoffeeScript用メジャーモード


## インストール
- NetInstallerからインストール

    http://youz.github.com/xyzzy/packages.l を登録し、パッケージ`*scrape*`より
    インストールして下さい。

- 手動インストール

    coffee-mode.lを`*load-path*`に配置してください。


## node.js と CoffeeScriptのインストール
ソースのコンパイル、実行、インタラクティブ実行を行うにはnode.jsと
CoffeeScriptのインストールが必要です。

- [node.js](http://nodejs.org)
- [CoffeeScript](http://jashkenas.github.com/coffee-script/)

## .xyzzy設定例

    (require "coffee-mode")
    (setq coffee:*command-path* "c:/path/to/node.exe c:/path/to/coffee-script/bin/coffee"
          coffee:*compiled-buffer-mode* 'jscript-mode)
    (push '("\\.coffee$" . coffee-mode) *auto-mode-alist*)


## デフォルトキーバインド

- C-c l -- list-function (関数一覧表示)
- C-c r -- evaluate-buffer (バッファ全体の内容をCoffeeScriptで実行し、結果を表示)
- C-c C-r -- evaluate-region (リージョンの内容をCoffeeScriptで実行し、結果を表示)
- C-c c -- compile-buffer (バッファ全体の内容をJavaScriptにコンパイルし、結果を表示)
- C-c C-c -- compile-region (リージョンの内容をJavaScriptにコンパイルし、結果を表示)
- C-c C-s -- compile-file-and-show (編集中のファイルをJavaScriptにコンパイルし、作成されたJSファイルを開く)
- C-c i -- repl (CoffeeScriptのreplを起動)
- C-c C-x r -- evaluate-buffer-in-repl (バッファ全体の内容をrepl上で評価)
- C-c C-x C-r -- evaluate-buffer-in-repl (リージョンの内容をrepl上で評価)
- TAB -- indent-or-dabbrev-expand

## repl バッファ用キーバインド
- C-j -- 改行
- TAB -- indent-or-dabbrev-expand
- C-c C-z -- 終了

他は`*shell-mode-map*`と同じです。


## Author
Yousuke Ushiki (<citrus.yubeshi@gmail.com>)

[@Yubeshi](http://twitter.com/Yubeshi/)

## License
GPLv2
