﻿# How to use [Jupyter](http://ground.u-aizu.ac.jp:8888)

### Table of contents
1. [Notebookを開く](#1-notebookを開く)
	1. [新規作成して編集](#11-新規作成して編集)
	2. [既存ファイルをアップロードして編集](#12-既存ファイルをアップロードして編集)
	3. [ディレクトリの作成](#13-ディレクトリの作成)
2. [編集画面での操作方法](#2-編集画面での操作方法)
	1. [ソースコードの記述と実行](#21-ソースコードの記述と実行)
	2. [Markdownの記述](#22-markdownの記述) 
3. [ファイルの提出](#3-ファイルの提出)
4. [Jupyter Notebook Viewerの使い方](#4-jupyter-notebook-viewerの使い方)
5. [カーネルの再起動](#5-カーネルの再起動)
6. [演習ガイド](#6-演習ガイド)
	1. [最初の1回目だけやる操作](#61-最初の1回目だけやる操作)
	2. [演習時の操作](#62-演習時の操作) 

---

## 1. Notebookを開く

Jupyter上でNotebookファイル(`*.ipynb`)を編集するためには、Notebookファイルを新規作成するか既存のNotebookファイルをアップロードする必要があります。

### 1.1. 新規作成して編集

![](https://i.imgur.com/QAoYgch.png)

Jupyterのホーム画面上にある **New** というボタンをクリックすると、新規作成メニューが展開されます。テキストファイル(`*.txt`)やフォルダを作成したり、コンソール画面を起動することもできますが、今回はNotebookファイルの新規作成をするのでその下の **Notebooks** の一覧から選択します。(今回は **Ruby** を選択します)

![](https://i.imgur.com/PU4yXnM.png)

すると、上のようなNotebookの編集画面が開かれます。無事編集画面が開かれたら、編集画面での操作方法のチャプターを見て実際にJupyterを使ってみましょう。

### 1.2. 既存ファイルをアップロードして編集

コンピュータ上に既にNotebookファイルがある場合は、それをJupyter上にアップロードして編集することができます。

![](https://i.imgur.com/p98BGKg.png)

**New** の隣にある **Upload** ボタンをクリックするとファイルマネージャが起動するので、コンピュータ上のアップロードしたいNotebookファイルを選択してください。

アップロードしたNotebookファイルはJupyterのファイル一覧の画面にそのファイル名が表示されるので、クリックして編集画面を開いてください。

### 1.3. ディレクトリの作成

ディレクトリを作成するとNotebookファイルやテキストファイルなどを中にまとめて入れて整理することができます。

![](https://i.imgur.com/uWLAcgi.png)

Notebookファイルを新規作成するときと同様に、**New** から **Folder** を選択してディレクトリを新規作成してください。

新しいディレクトリが作成されます。

![](https://i.imgur.com/qyoWxfK.png)

ディレクトリは作成した直後は`Untitled Folder`という名前になっています。ディレクトリの名前を変更するには、名前を変更したいディレクトリのチェックボックスにチェックを入れて、上の **Rename** をクリックしてください。

## 2. 編集画面での操作方法

![](https://i.imgur.com/PU4yXnM.png)

Jupyterは **ドキュメント兼インタプリタ** のようなもので、編集画面にはいくつかのメニューやアイコンと、テキストの編集ボックス(cell, セル)があります。

* メニュー
	* **File** ... 新規ファイルの作成やファイルを開いたり、保存やダウンロードなどができます。また、チェックポイントを復元することもできます。
	* **Edit** ... セルをコピー＆ペースト・移動・削除したり、複数のセルを結合することができます。
	* **Insert** ... 現在のセルの上下の位置にセルを挿入することができます。
	* **Cell** ... セル内のコードを実行し、その結果などに対する操作も選ぶことができます。セルのタイプを変更することもできます。
* アイコン
	* 基本的にメニューから実行できる操作のショートカットアイコンになっています。

また、画面上部のタイトルをクリックするとファイル名を自由に変更することができます。演習に使うRuby用のNotebookは全員が同一のリポジトリからクローンしたものなので、Jupyter上にファイルをアップロードしたときに全てのファイル名が同じになり **区別がつかなくなってしまいます** 。そういったことを避けるために、ファイルを新規作成、もしくはアップロードしたときには必ず **自分の学籍番号** を **ファイル名の先頭** に付けるようにしましょう。

(例: `Sample.ipynb` -> `s1250123-Sample.ipynb`)

### 2.1. ソースコードの記述と実行

セルのタイプを **Code** にするとNotebookで指定された言語のインタプリタとしてソースコードを記述・逐次実行することができます。

![](https://i.imgur.com/BvxBj1p.png)

今回はRubyですので、試しにRubyのシンタックスでソースコードを書いてみてください。

**Ctrl + Enter** を押すと、そのコードが実行されます。
**Shift + Enter** を押すと、コードが実行されるのと同時に新しいセルに編集スコープが移動します。

![](https://i.imgur.com/P6fqMCD.png)

変数や関数などは複数のセルの間で共有されています。**Out** に表示されるのは最後に評価された式の値だけなので、自分で見やすいように工夫して書いてみてください。

### 2.2. Markdownの記述

セルのタイプをMarkdownに変更すると、Notebook中にMarkdownのシンタックスを使ってドキュメントを埋め込むことができます。

Notebookファイル中のMarkdownのセルはCodeのセルの動作に影響を与えないので、ノートやメモを取りたいとき、プログラムの解説などを書きたいときなどに使うと良いでしょう。

![](https://i.imgur.com/6ReRqSn.png)

Markdownの場合もセルを評価する場合には同様に **Ctrl + Enter**、もしくは **Shift + Enter** を押してください。Markdownの場合にはOutは表示されず、記述したMarkdownのコードがそのままプレビューされます。

![](https://i.imgur.com/Xp0zGVi.png)

一つのNotebook中には複数のタイプのセルを混在させることができるので試してみてください。

cf. [Markdown記法サンプル集](http://qiita.com/tbpgr/items/989c6badefff69377da7)

## 3. ファイルの提出

今回の演習では、編集が終わってコンピュータ上にダウンロードしたNotebookファイルは元のリポジトリに入れ直してGitHub Organization上のリモートリポジトリに提出してもらいます。

![](https://i.imgur.com/1IjAIRV.png)

Notebookファイルをダウンロードするときには複数のファイルフォーマットを選択することができます。今回の演習ではテンプレートのファイル同様に`.ipynb`を選択するようにしましょう。

また、Jupyterは実践的プログラミングを受講している学生全員で１つのものを使っています。ファイル一覧の画面が汚くならないように、Notebookファイルの編集・保存と **コンピュータ上へのダウンロード** が終わったらJupyter上の自分のNotebookファイルは **自分で削除** するようにしましょう。

![](https://i.imgur.com/JtTLmhV.png)

削除したいファイルのチェックボックスにチェックを入れ、**ゴミ箱の赤いアイコン** をクリックすると削除確認画面が出るのでDeleteをクリックしてファイルを削除してください。

削除されていないNotebookファイルは、コンピュータ上にダウンロードされている・いないに関わらずTAが定期的に **全て削除** しますので演習が終わったら必ずNotebookファイルをダウンロードしてJupyter上のファイルを削除するようにしてください。

## 4. Jupyter Notebook Viewerの使い方

**Jupyter Notebook Viewer** 上ではGitHub Organizationのリモートリポジトリ内のNotebookファイルを確認することができるので、Notebookファイルの提出後の確認などに使ってみてください。

![](https://i.imgur.com/Oy3VyDZ.png)

[Notebook Viewer / SCCP2016](http://nbviewer.jupyter.org/github/SCCP2016/)

## 5. カーネルの再起動

Notebook中のセルは自由に任意のセルを後からでも編集することが可能ですが、過去のセルを再編集して再評価したときに以降のセルで予期しない動作を引き起こす場合があります。

以下はその一例です。<sub>※アニメーションになっています。</sub>

![](https://i.imgur.com/Q735p52.gif)

`A`クラスに`x`というインスタンス変数を持たせて、コンストラクタ内で`x`を引数で初期化しています。その次のセルで`a`という変数に`A`クラスのインスタンスを引数を`10`として代入し、`a.x`を呼び出しています。もちろんここでは`a.x`は`10`と表示されます。

しかし、セルを遡って`A`のクラス定義の`attr_reader`をコメントアウトして順に再評価した場合でも、`a.x`はコメントアウト前と同様に呼び出すことが出来てしまいます。

(`A`のクラス定義中では`x`というインスタンス変数はコメントアウトされていて、**本来は呼び出すことが出来ない** のが正しい。)

これは **`A`のクラス定義がコメントアウト前の状態で束縛されたままである** ことが原因で起こる現象です。

この場合には **Kernel** のメニューからKernelを **Restart** してセルを順に再評価するようにしましょう。そうすれば`a.x`は呼び出すことが出来なくなっているはずです。

## 6. 演習ガイド

実践的プログラミング2016後期では、演習を進めるにあたって複数のツールやコマンドなどをいくつか使うことになります。以下にコマンドの例を挙げておきますので、困ったときや忘れてしまったときは参照してみてください。

### 6.1. 最初の1回目だけやる操作

1. テンプレートリポジトリのclone
```
$ git clone https://github.com/SCCP2016/<repo_name>.git

# <repo_name> ... botter_introduction, Document_rubytutorial-on-jupyter
```

2. リモート情報の削除 **(必ずやる)**
```
$ cd ./<repo_name>
$ rm -rf ./.git
```

3. リモート情報の再登録
```
$ git remote add origin git@github.com:SCCP2016/<student_num>-<repo_name>.git

# <student_num> ... sXXXXXXX (your student number)
```

4. リモートリポジトリにpush
```
$ git push origin master
```

### 6.2. 演習時の操作

1. Notebookファイルのリネーム
```
$ mv <file_name> <student_num>-<file_name>

# Jupyterにアップロードした後に判別しやすいように先に名前を変える。
```

2. Notebookファイルのアップロード<br>「[1.2. 既存ファイルをアップロードして編集](#12-既存ファイルをアップロードして編集)」を参考にして指定されたファイルをJupyterにアップロードしてから開く。

3. ファイルの編集

4. ファイルのダウンロードとJupyter上からの削除<br>「[3. ファイルの提出](#3-ファイルの提出)」を参考にしてNotebookファイルをダウンロードして上書きし、正常に上書きできたらJupyter上の当該ファイルを削除する。

5. 提出
```
$ git add <path_to_file>
$ git commit -m "<commit_msg>"
$ git push origin master

# <path_to_file> ... 演習で使ったファイルのパス。3でダウンロードして上書きしたもの。
# <commit_msg> ... 分かりやすいものが好ましい
```

6. 提出確認<br>提出したファイルは「[4. Jupyter Notebook Viewerの使い方](#4-jupyter-notebook-viewerの使い方)」にもある通りJupyter Notebook Viewerから確認することができる。