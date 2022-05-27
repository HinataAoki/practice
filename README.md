# git の使い方

## github のアカウントを作成

google 使ったことあんならわかんだろ

# アカウント登録

Github にアカウントを作ったら PC に自分の Github アカウントを登録しましょう。

### 自分の git アカウントの情報を入力します。

- コマンドプロンプト(win) or ターミナル(mac)を起動して

```
git config --global user.name "Smash Bros"
git config --global user.email smashbros@example.com
```

## どうやって Github を始めるの？

2 択の読み合い

1. 自分が新たにレポジトリを作る
2. すでにあるレポジトリに参加する

### 1. 新たに作る

わかりやすいのでウェブの Github のページから行いましょう。
![How To make new repository](/IMG/Howtomakenewrepository.png)

### 2. すでにあるレポジトリに参加する(clone)

こっちの方がよくあるパターンかもしれません。

すでにレポジトリがあるときにはクローンします
自分の任意のパスに移動して

```
cd hogehoge/hogehoge
```

以下のコマンドを入力

```
git clone https://github.com/eastgeeksmash/practice.git
```

![How to clone](/IMG/gitclone.png)

## これでスタートラインに立ちました！

ではここからどのように使うかを詳しく見ていきましょう。

## よく使うのは大きく分けて 4 つ

これらの操作はまとめて覚える

1. ほかの人の変更の取り込み(pull)
2. ファイルの追加(add, commit)
3. ブランチの生成(branch)
4. マージ

### 1.他の人の変更を取り込む(pull)

`この操作が最重要です！！！`  
これを忘れると本当にめんどくさいことになるので、まずは pull しましょう。  
ほかの人の変更を自分のファイルに反映させましょう。
任意の git が入っているフォルダにカレンとディレクトを移動して

```
git pull
```

繰り返しになりますが、この操作は作業を開始するときに忘れないでください！  
`QM スピリットをつけ忘れるくらい罪です。`

### git にファイルを追加する

作成した、もしくはファイルに変更を加えて、レポジトリに更新をかけたいときに以下の作業を行います。

#### 手順 1:add

`git add 〇〇.hoge`
または
`git add .`
これですべてのファイルを add できます。

#### 手順 2:commit

コミットします
コミットの際には何の変更をしたかを誰にでもわかるように書いておきましょう。
`git commit -m"ここにメッセージ"`

#### 手順 3:push

プッシュします
`git push`

### ブランチについて

ブランチは現在の状態をコピーしたもの
ブランチを作ることによって、例えばそのブランチ内での変更をしても、本体のほうには変更が行かないので、ミスがあったときに修正してから本体のほうに反映できる。

![branch_image](https://firebasestorage.googleapis.com/v0/b/hina-blog.appspot.com/o/branch_image.jpg?alt=media&token=7eae3cbf-3dfc-463f-9c92-8e07f60a6b76)

#### ブランチの確認

`git branck`

#### ブランチの作成

korehatestdayo_branch という名前のブランチを作る時には
`git branch korehatestdayo_branch`

#### ブランチを切り替える

korehatestdayo_branch に移動するとき
`git checkout korehatestdayo_branch`

### マージする

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

# 実践練習

[practice.md](practice.md)に移動して名前を追記してみましょう！
