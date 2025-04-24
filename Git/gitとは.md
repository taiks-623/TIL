## コード変更の流れ
* コードを変更しステージングエリアに追加
* 変更をコミットしてローカルリポジトリに保存
* プッシュすることでコミットをリモートリポジトリに送信しほかの開発者と共有する

## ほかの開発者が変更を加えた場合
* プルを使って変更を自分のローカルリポジトリに取り込む

## ブランチ
* プロジェクトの異なるバージョンを並行して開発するために使用
  - ブランチを作ると新しい開発戦に分岐する
  - 作業が完了したらメインブランチにマージして統合していく

## gitとGitHubの違い
* GitHubとは
  - gitのバージョン管理機能を利用するウェブベースのプラットフォーム
  - コードをオンライン上で保存、共有、協力して作業を行うためのサービス

## GitHubフロー
* 開発を行うためのブランチの管理手法
  - メインからcheckout
  - PullRequest(コードレビュー)
  - merge

## gitコマンド
* git init : 作業するディレクトリでGitを使用する宣言
* git add : 対象ファイルをステージングエリアに上げる(コミット対象にする)
* git commit : コミットする
* git status : 現在の状態を確認する
* git checkout -b [branch name] : 弁財のブランチから新規ブランチを作成
* git branch : ブランチの一覧を表示
* git push origin [branch name] : リモートリポジトリにプッシュ
* git pull origin [branch name] : リモートリポジトリをプル
* git clone[リポジトリURL] : リモートリポジトリをローカルに複製

## gitを使うための準備
* 最新バージョンのgitを用意
  - `brew install`
* ssh鍵作成
  - sshディレクトリの作成
    - `mkdir ~/.ssh`
  - .sshに移動
    - `cd ~/.ssh`
  - 鍵作成コマンドを打つ
    - `ssh-keygen -t rsa`
  - `ls`で確認して`id_rsa`と`id_rsa.pub`があればOK
* GitHubに鍵を登録
  - `cat id_rsa.pub`で表示
  - 内容をコピー
  - GitHubの右上のアイコンからSettingsを開いて左のメニューのSSH and GPG keysをクリック

## Gitflow
* ブランチを切る
* 編集したらステージングエリアに上げる `git add`
* その後コミットしてローカルリポジトリに上げる `git commit -m "commit message"`