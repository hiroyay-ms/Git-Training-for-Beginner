![Microsoft Cloud Workshop](images/ms-cloud-workshop.png)

Hands-on lab  
Mar 2021

<br />

**Contents**

 
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [**要約および学習目標**](#要約および学習目標)
    - [**事前準備**](#事前準備)
- [**Git リポジトリの作成から Commit まで**](#git-リポジトリの作成から-commit-まで)
  - [Git リポジトリの作成と Initial Commit](#git-リポジトリの作成と-initial-commit)
  - [ファイルの作成と編集](#ファイルの作成と編集)
  - [Stage](#stage)
  - [Commit](#commit)
- [**Branch の作成から Merge まで**](#branch-の作成から-merge-まで)
  - [Branch の作成](#branch-の作成)
  - [新規ファイルの作成と編集](#新規ファイルの作成と編集)
  - [Stage & Commit](#stage-commit)
  - [Merge](#merge)
- [**Conflict を解決する**](#conflict-を解決する)
  - [main ブランチへ切り替え](#main-ブランチへ切り替え)
  - [ファイル編集して Stage & Commit](#ファイル編集して-stage-commit)
  - [新しい Branch を作成](#新しい-branch-を作成)
  - [同じファイルを編集して Stage &  Commit](#同じファイルを編集して-stage-commit)
  - [Mergeする（Conflictさせる)](#mergeするconflictさせる)
  - [Conflict を解消して Stage & Stage & Commit](#conflict-を解消して-stage-stage-commit)
- [**間違えた Commit を修正する**](#間違えた-commit-を修正する)
  - [Stage し忘れたファイルがあった場合](#stage-し忘れたファイルがあった場合)
  - [Branch を切り忘れて main ブランチに Commit した場合](#branch-を切り忘れて-main-ブランチに-commit-した場合)
- [**Remote(Bare) リポジトリの作成から Push まで**](#remotebare-リポジトリの作成から-push-まで)
  - [Remote(Bare) リポジトリの作成](#remotebare-リポジトリの作成)
  - [Clone](#clone)
  - [ファイルを新規作成して Stage & Commit](#ファイルを新規作成して-stage-commit)
  - [Push](#push)
- [**Challenge Remote リポジトリに誰かが先に Push してしまった場合のエラーを解消する**](#challenge-remote-リポジトリに誰かが先に-push-してしまった場合のエラーを解消する)

<!-- /code_chunk_output -->


<br />

# **要約および学習目標**

### **事前準備**

- ローカル環境
  - Visual Studio Code のインストール

    Visual Studio Code  
    <https://azure.microsoft.com/ja-jp/products/visual-studio-code/>

  - Git のインストール  
    <https://git-scm.com/>

  - Git Graph のインストール (VS Code プラグイン)
    <https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph>

<br />

***

# **Git リポジトリの作成から Commit まで**

## Git リポジトリの作成と Initial Commit

aaa

## ファイルの作成と編集

aaa

## Stage

aaa

## Commit

aaa

***

# **Branch の作成から Merge まで**

## Branch の作成

aaa

## 新規ファイルの作成と編集

aaa

## Stage & Commit

aaa

## Merge

aaa

***

# **Conflict を解決する**

## main ブランチへ切り替え

aaa

## ファイル編集して Stage & Commit

aaa

## 新しい Branch を作成

aaa

## 同じファイルを編集して Stage &  Commit

aaa

## Mergeする（Conflictさせる)

aaa

## Conflict を解消して Stage & Stage & Commit

aaa

***

# **間違えた Commit を修正する**

以下の手順は、Remote リポジトリに Push する前であれば有効な手順です。もし Push してしまった場合は Commit を取り消すための Commit である「 Revert 」を使用します。

## Stage し忘れたファイルがあった場合

Commit を削除して、Stage した直後の状態になります。
```powershell
git reset --soft HEAD^
```

この手順を応用すると、Commit してはいけなかったファイルを Commit から取り除くこともできます。

**注意**
これは最新の Commit をミスしてしまった場合の手順です。２つ前以上古い履歴の Commit への修正は　コマンドを使用してできないわけではありませんが、お勧めしません。


## Branch を切り忘れて main ブランチに Commit した場合

慌てないで、その場ですぐ新しい Branch を作ります。

```powershell
git branch newBranch
```

main ブランチを１つ前の状態に戻します。最後のコミットは 新しい Branch が参照しているため、消えることはありません。

```powershell
git reset --hard HEAD^
```

この手順では１つだけ Commit してしまった場合に対応していますが、複数回前の Commit から Branch を切ることもできます。
(main ブランチを戻した位置が、Branchを切りたかった Commitになる)

***

# **Remote(Bare) リポジトリの作成から Push まで**

## Remote(Bare) リポジトリの作成

aaa

## Clone

aaa

## ファイルを新規作成して Stage & Commit

aaa

## Push

aaa

***

# **Challenge Remote リポジトリに誰かが先に Push してしまった場合のエラーを解消する**

直上の手順で作成した Remote リポジトリに対して、誰かが自分より先にコードを Push してしまった状態を作ります。

1. 第三者となって Remote リポジトリから Clone してください。
1. 直上の手順で新規作成したファイルの1行目を変更し、Commit & Push してください。
1. 直上のリポジトリに移動し、ファイルの１行目を変更し、Commit & Push してください。

エラーが発生します。このエラーを解消してください。

- Conflict は第三者の編集内容を２行目として解消してください。

