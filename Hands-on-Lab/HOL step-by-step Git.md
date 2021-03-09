![Microsoft Cloud Workshop](images/ms-cloud-workshop.png)

Hands-on lab  
Mar 2021

## **Contents**

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [**準備**](#準備)
- [**Exercise 1**](#exercise-1)
  - [ローカルリポジトリを作成し、ファイルを Commit する](#ローカルリポジトリを作成しファイルを-commit-する)
  - [Exercise 1 達成条件](#exercise-1-達成条件)
- [**Exercise 2**](#exercise-2)
  - [Branch を作成して Commit すること](#branch-を作成して-commit-すること)
  - [Exercise 2 達成条件](#exercise-2-達成条件)
- [**Exercise 3**](#exercise-3)
  - [Merge する](#merge-する)
  - [Exercise 3 達成条件](#exercise-3-達成条件)
- [**Exercise 4**](#exercise-4)
  - [merge で Conflict を発生させて解決する](#merge-で-conflict-を発生させて解決する)
  - [Exercise 4 達成条件](#exercise-4-達成条件)
- [**Exercise 5**](#exercise-5)
  - [リモートリポジトリを作成してローカルリポジトリと同期する](#リモートリポジトリを作成してローカルリポジトリと同期する)
  - [Exercise 5 達成条件](#exercise-5-達成条件)
- [**Exercise 6**](#exercise-6)
  - [リモートリポジトリから Clone してから Push する](#リモートリポジトリから-clone-してから-push-する)
  - [Exercise 6 達成条件](#exercise-6-達成条件)
- [**Exercise 7**](#exercise-7)
  - [Commit を 取り消す](#commit-を-取り消す)
  - [Exercise 7 達成条件](#exercise-7-達成条件)
- [**Exercise 8**](#exercise-8)
  - [Merge を 取り消す](#merge-を-取り消す)
  - [Exercise 8 達成条件](#exercise-8-達成条件)
- [**Challenge Exercise**](#challenge-exercise)
  - [Branch を切り損ねた対応をする](#branch-を切り損ねた対応をする)

<!-- /code_chunk_output -->

# **準備**

- ローカル環境
  - Visual Studio Code のインストール
    <https://azure.microsoft.com/ja-jp/products/visual-studio-code/>

  - Git のインストール  
    <https://git-scm.com/>

  - Git Graph のインストール (VS Code プラグイン)
    <https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph>

***

# **Exercise 1**

## ローカルリポジトリを作成し、ファイルを Commit する

- ローカルリポジトリは C:\gitroot フォルダ配下に作成してください。
- ローカルリポジトリ名は firstRepo としてください。
- Commit を２つ作ってください。
- 1つ目の Commit について
  - 作成するファイル名は file1.txt としてください。
  - file1.txt には以下の内容を保存してください。

  ```text
  first line in file1
  ```

  - Commit メッセージには以下を入力してください。

  ```text
  add file1
  - file1.txtを追加
  ```

- 2つ目の Commit について
  - 作成するファイル名は file2.txt としてください。
  - file2.txt には以下の内容を保存してください。

  ```text
  first line in file2
  ```

  - Commit メッセージには以下を入力してください。

  ```text
  add file2

  - file2.txtを追加
  ```

## Exercise 1 達成条件

- C:\gitroot\firstRepo がリポジトリになっていること
- file1.txt が Commit されていること
- Commit ログが２つあり、それぞれの Commit の内容が指定通りであること
- コーチが結果を確認して OK であること

***

# **Exercise 2**

## Branch を作成して Commit すること

- Exercise 1 の２つ目の Commit から Branch を作ってください。
- Branch 名は BranchA としてください。
- BranchA ブランチで file2.txt を以下の内容に編集して Commit してください。

  ```text
  first line in file2
  this line was add in branchA
  ```

  - Commit メッセージには作業内容をわかりやすく入力してください。

- main ブランチ に切り替えてください。
- file1.txt を以下の内容に編集して Commit してください。

  ```text
  first line in file1
  this line was add in main
  ```

  - Commit メッセージには作業内容をわかりやすく入力してください。

## Exercise 2 達成条件

- BranchA に Commit が１つあること
- main に Commit が３つあること
- コーチが結果を確認して OK であること

***

# **Exercise 3**

## Merge する

- branchA ブランチを main ブランチへ merge してください。
- merge する時の Commit メッセージは適切なものを自分で入力してください。
- merge 後、 branchA を削除してください。

## Exercise 3 達成条件

- Conflict することなく merge が完了した
- branchA が削除されていること
- file1.txt の内容が下記になっていること

  ```text
  first line in file1
  this line was add in main
  ```

- file2.txt の内容が下記になっていること

```text
  first line in file2
  this line was add in branchA
```

- コーチが結果を確認して OK であること

***

# **Exercise 4**

## merge で Conflict を発生させて解決する

- file3.txt を main ブランチに追加して Commit してください。
  - file3.txt には以下の内容を保存してください。
  - Commit メッセージはわかりやすいものにしてください。

  ```text
  first line in main
  ```

- file3.txt を追加した Commit に対して Branch を切ってください。
- Branch 名は BranchB としてください。
- Branch で file3.txt を次のように編集して Commit してください

  ```text
  first line in branchB
  ```

- branchB ブランチを main ブランチへ merge してください。
- file3.txt のConflict を次のように解決してください。

  ```text
  first line in main
  second line in branchB
  ```

- merge 時の Commit メッセージは適切なものを自分で入力してください。
- merge 後、 branchB を削除してください。

## Exercise 4 達成条件

- Conflict を解決して merge が完了したこと
- branchB が削除されていること
- file3.txt の内容が下記になっていること

  ```text
  first line in main
  second line in branchB
  ```

- コーチが結果を確認して OK であること

***

# **Exercise 5**

## リモートリポジトリを作成してローカルリポジトリと同期する

- aaa

## Exercise 5 達成条件

- aaa

***

# **Exercise 6**

## リモートリポジトリから Clone してから Push する

- aaa

## Exercise 6 達成条件

- aaa

# **Exercise 7**

## Commit を 取り消す

- aaa

## Exercise 7 達成条件

- aaa

***

# **Exercise 8**

## Merge を 取り消す

- aaa

## Exercise 8 達成条件

- aaa

***

# **Challenge Exercise**

## Branch を切り損ねた対応をする

直上の手順で作成した Remote リポジトリに対して、誰かが自分より先にコードを Push してしまった状態を作ります。

1. 第三者となって Remote リポジトリから Clone してください。
1. 直上の手順で新規作成したファイルの1行目を変更し、Commit & Push してください。
1. 直上のリポジトリに移動し、ファイルの１行目を変更し、Commit & Push してください。

エラーが発生します。このエラーを解消してください。

- Conflict は第三者の編集内容を２行目として解消してください。
