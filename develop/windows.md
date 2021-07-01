# Windows向け開発環境の構築

## エディタ

メモ帳でプログラムを書くこともできますが、一般的にはプログラミングに便利な機能が入ったエディタを使います。  
特にこだわりがなければMicroSoftが提供する[Visual Studio Code](https://code.visualstudio.com)をおすすめします。　　
上のリンクのページから「Download for Windows」をクリックしてインストーラをダウンロード→実行してインストールします。

## Gitクライアント

Windowsでソースコードの取得・更新などを行うために[Git for Windows](https://gitforwindows.org)を使います。  
上のリンクのページから「Download」をクリックしてインストーラをダウンロード→実行してインストールします。

## スモウルビー3 GUI

Node.js（JavaScriptのランタイム…プログラムを動かすプログラム）上で動作するスモウルビーです。

### Node.js

[Node.js](https://nodejs.org)のページから「LTS」（「Current」ではなく）のインストーラをダウンロード→実行してインストールします。

### GitHubのソースコード

[スモウルビーのGitHubリポジトリ](https://github.com/smalruby/smalruby3-gui)からクローン（プログラムを自分のPCにダウンロードすること）します。

1. コマンドプロンプトを起動する
2. 作業するフォルダに移動する
3. 次のコマンドでクローンする

    ```cmd
    git clone https://github.com/smalruby/smalruby3-gui
    ```

4. cloneしたフォルダに移動する

    ```cmd
    cd smalruby3-gui
    ```

5. npm（Node.jsが使うライブラリ）をインストールする

    ```cmd
    npm install
    ```

6. 自分のPCでスモウルビーが動作するか確認する→ブラウザが開いてスモウルビーの画面が表示されればOK（終了する場合は「ctrl」と「c」を同時押しします）

    ```cmd
    npm start
    ```

## GitHubアカウント

GitHubはGitリポジトリを管理するサービスです。  
スモウルビーはGitHub上で開発されています。

### GitHubのアカウント作成

※ すでにアカウントを持っている場合はスキップしてください

[GitHub](https://github.com)のページから「Sign up」をクリックして登録します。

* Username：基本的に変更しないアカウント名です。氏名を入力する欄は別にあります
* Email address：アカウント登録するとメールが届きます。メールのリンクをクリックすると登録完了です

### スモウルビーのフォーク

スモウルビーを自分のリポジトリとしてコピーします。

また、クローンされたリポジトリのリモートリポジトリを自分のアカウントのものに変更します。

1. [スモウルビーのGitHubリポジトリ](https://github.com/smalruby/smalruby3-gui)のページにある「fork」をクリックする
2. コマンドプロンプトを開いてsmalruby3-guiのフォルダに移動する（上でnpm startを実行したフォルダです）
3. リモートリポジトリを変更する（<アカウント名>にはGitHubのUsernameを入れてください）

    ```cmd
    git remote rename origin upstream
    git remote add origin https://github.com/<アカウント名>/smalruby3
    ```

## スモウルビー（DXRuby）

スモウルビー3 GUIとは異なる環境で実行するスモウルビーです。

https://qiita.com/takaokouji/items/78c889497bb790d738fc#smalruby
