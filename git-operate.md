# 設定
インストール確認
get --version

ユーザー名とメールアドレス設定
* git config --global user.name "UserName"
* git config --global user.email "UserEmail"

ユーザー名とメールアドレスの確認
* git var GIT_COMMITTER_IDENT
* git var GIT_AUTHOR_IDENT

問題対処。
git status コマンドで日本語ファイル名が化ける
git config --global core.quotepath false

全設定の確認
* git config -l


# 基本操作
: カレントディレクトリを git 管理開始
git init

: ステージングに追加 (.gitignore を除くカレント以下すべて対象)
git add .
* まとめてadd -- git add -A


: 状態確認
git status

: ステージングに取り消し (.gitignore を除くカレント以下すべて対象)
git reset .

: コミット (スペースをタイトルに使う場合は " で囲むこと)
git commit -m "コミットタイトルメッセージ"

: コミット内容を修正したいとき
git commit --amend -m "cssを修正"

: 履歴を確認
git log

: GUI で履歴を確認
gitk

: リモートリポジトリの一覧を表示
git remote

: リモートリポジトリを追加
git remote add <remotename> <url>

: 登録済みのリモートリポジトリの名前を変更
git remote rename <remotename <newname>

: リモートリポジトリにプッシュ(master はブランチ名)
git push <remotename> master


# ブランチ操作
: ブランチ一覧
git branch

: ブランチを作成
git checkout <branchname>

: ブランチへ移動
git checkout <branchname>

: ブランチ名を変更
git branch -m <oldbranch> <newbranch>

: コミットログ図表示 (ブランチポインタの指すコミット、歴史の分岐も表示)
git log --oneline --decorate --graph --all
