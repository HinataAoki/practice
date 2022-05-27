# git の使い方

## github のアカウントを作成

google 使ったことあんならわかんだろ

## 導入する

- 導入したいディレクトリに移動する `cd 〇〇/〇〇/〇〇`
- git を導入するコマンドを打つ `git init`

- 自分の git アカウントの情報を入力します。
  - `git config --global user.name "Smash Bros"`
  - `git config --global user.email smashbros@example.com`

## Git の良さ

- 変更の履歴が残る
- 戻したい変更まで戻ることができる
- PC 内で保存しておく必要がない
- 共同開発が可能

## よく使うのは大きく分けて 4 つ

これらの操作はまとめて覚える

1. ファイルの追加(add, commit)
2. ほかの人の変更の取り込み(pull)
3. ブランチの生成(branch)
4. マージ

## git をクローンする

すでにレポジトリがあるときにはクローンします `git clone https:.....`

## 開発を始めるときは

ほかの人の変更を自分のファイルに反映させましょう
`git pull`

## git にファイルを追加する

作成した、もしくはファイルに変更を加えて、レポジトリに更新をかけたいときには

### 手順 1:add

`git add 〇〇.hoge`
または
`git add .`
これですべてのファイルを add できます。

### 手順 2:commit

コミットします
コミットの際には何の変更をしたかを誰にでもわかるように書いておきましょう。
`git commit -m"ここにメッセージ"`

### 手順 3:push

プッシュします
`git push`

## ブランチについて

ブランチは現在の状態をコピーしたもの
ブランチを作ることによって、例えばそのブランチ内での変更をしても、本体のほうには変更が行かないので、ミスがあったときに修正してから本体のほうに反映できる。

![branch_image](https://firebasestorage.googleapis.com/v0/b/hina-blog.appspot.com/o/branch_image.jpg?alt=media&token=7eae3cbf-3dfc-463f-9c92-8e07f60a6b76)

### ブランチの確認

`git branck`

### ブランチの作成

korehatestdayo_branch という名前のブランチを作る時には
`git branch korehatestdayo_branch`

### ブランチを切り替える

korehatestdayo_branch に移動するとき
`git checkout korehatestdayo_branch`

## マージする

![push](https://firebasestorage.googleapis.com/v0/b/hina-blog.appspot.com/o/push_image.jpg?alt=media&token=2d7283a2-7bb0-4bcf-8ef7-e714192f611f)
一つのブランチに統合します。

基本的には GUI 操作でマージは行うような気がします。

1. Github のウェブページに移動して、マージリクエストを作成
2. マージする

### まずは現在のブランチの確認

`git branch`
-> \*korehatestdayo_branch

### 統合したいブランチに移動

`git checkout master`

### master であることを確認して、master にマージ

`git merge korehatestdayo_branch`
これで korehatestdayo_branch での変更が master に反映されました。

<br><br><br><br><br><br><br><br><br>

## 実戦練習

ここに名前を書いて、上の手順に従って更新してみよう

- HinataAoki
- Cody
- Mahiro
