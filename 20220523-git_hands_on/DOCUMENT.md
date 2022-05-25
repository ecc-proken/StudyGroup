# Git / GitHub ハンズオン

## 準備

### Javaのインストール

#### ダウンロード

https://www.oracle.com/java/technologies/downloads からインストーラーをダウンロード

<img src="./img/62886bdc59cf2091615d0dd5.png" style="width:640px;"/>

Windowsを選択してインストーラーをDL

<img src="./img/62886bea59cf2091615d0df3.png" style="width:640px;"/>

#### インストール

ダブルクリックして実行
全て「次へ」でインストール

<img src="./img/62886c1259cf2091615d0ea4.png" style="width:640px;"/>


### Gitのインストール

#### ダウンロード

http://git-scm.com/download/ からインストーラをダウンロード

<img src="./img/62887a0a59cf2091615d120d.png" style="width:640px;"/>

Windowsを選択してインストーラーをDL

<img src="./img/62887a2f59cf2091615d125e.png" style="width:640px;"/>
<img src="./img/62887a4f59cf2091615d12ed.png" style="width:640px;"/>

#### インストール

ダブルクリックして実行

<img src="./img/62887a6059cf2091615d1369.png" style="width:640px;"/>

Windows TerminalでGit Bashを開けるようにする（しなくてもいいけどおすすめ）

<img src="./img/6288804859cf2091615d1731.png" style="width:640px;"/>

初期ブランチ名を`main`にする（しなくてもいいけどおすすめ）

<img src="./img/62887a6e59cf2091615d13ba.png" style="width:640px;"/>

PowerShellからGitを使えるようにしておく（しなくてもいいけどおすすめ）

<img src="./img/62887a7159cf2091615d13c5.png" style="width:640px;"/>

### VSCodeのインストール

#### ダウンロード

https://code.visualstudio.com/Download からインストーラをダウンロード
<img src="./img/62887eba59cf2091615d162d.png" style="width:640px;"/>

Windowsを選択してインストーラーをDL

<img src="./img/62887eba59cf2091615d1635.png" style="width:640px;"/>

#### インストール

ダブルクリックして実行

<img src="./img/62887eba59cf2091615d1621.png" style="width:640px;"/>
<img src="./img/62887eba59cf2091615d1622.png" style="width:640px;"/>

エクスプローラーからVSCodeを開けるようにする（しなくてもいいけどおすすめ）

<img src="./img/62887eba59cf2091615d1617.png" style="width:640px;"/>

#### 設定・拡張機能のインストール

日本語対応

<img src="./img/6288864559cf2091615d195c.png" style="width:950px;"/>

Gitを使いやすくするやつ

<img src="./img/6288864559cf2091615d1961.png" style="width:950px;"/>

ESLint（簡単に言うと隠れている警告を表示してくれるやつ）

<img src="./img/6288864559cf2091615d1981.png" style="width:950px;"/>

Prettier（コード（プログラム）を自動できれいにしてくれるやつ）

<img src="./img/6288864559cf2091615d197f.png" style="width:950px;"/>

コードを書きやすく色付けするやつ

<img src="./img/6288864559cf2091615d198c.png" style="width:950px;"/>

全角スペースに色を付けてくれるやつ（全角スペースが隠れててエラーは結構あるから大事）

<img src="./img/6288864559cf2091615d1994.png" style="width:950px;"/>

Javaを書いたり実行しやすくするやつ

<img src="./img/6288919b59cf2091615d1f53.png" style="width:950px;"/>

設定を開いて

<img src="./img/6288864559cf2091615d196a.png" style="width:950px;"/>

`format on save`で検索
セーブしたときに自動でコードを整形してくれるようにしておく

<img src="./img/6288864559cf2091615d1972.png" style="width:950px;"/>

`terminal default profile`で検索
VSCode上で開くターミナルをGit Bashにしておく

<img src="./img/6288951959cf2091615d2119.png" style="width:950px;"/>

## 実践

### フォルダを作成

フォルダの場所は好きなところで新規作成

<img src="./img/628896a559cf2091615d231b.png" style="width:950px;"/>

フォルダの名前を決める（例：`java_hello_git`）

<img src="./img/628896a559cf2091615d2324.png" style="width:950px;"/>

### VSCodeで作ったフォルダを開く

ファイル > フォルダーを開く
<img src="./img/6288961759cf2091615d21ed.png" style="width:950px;"/>
<img src="./img/6288961759cf2091615d21e5.png" style="width:950px;"/>

ショートカットから開く
<img src="./img/62889a7e59cf2091615d2870.png" style="width:640px;"/>

### Javaで`Hello, world!`

`Main.java`を作成

```java
// Main.java
class Main {
	public static void main(String[] args) {
		System.out.println("Hello, world!");
        }
}
```
<img src="./img/6288986a59cf2091615d24b5.png" style="width:950px;"/>

実行（Java Extention Packの機能）
<img src="./img/6288986a59cf2091615d24c6.png" style="width:950px;"/>

コマンド ver.

ターミナルを開く [Ctrl + `]
<img src="./img/6288986a59cf2091615d24c9.png" style="width:950px;"/>

ターミナルに次のコマンドを入れる
```bash
$ java Main.java
```
<img src="./img/6289e9243c94150a6284b264.png" style="width:950px;"/>

### GitHub登録

https://github.com

### Gitの設定

```bash
$ git config --global user.email "<メールアドレス>"
$ git config --global user.name "<ユーザー名>"
```

<img src="./img/6289eab03c94150a6284b966.png" style="width:950px;"/>

### フォルダをGitで管理

<img src="./img/6289d2bb3c94150a62849252.png" style="width:950px;"/>


コマンド ver.

```bash
$ git init
```

<img src="./img/6289d2bb3c94150a6284924a.png" style="width:950px;"/>

### Gitでコミット（新しいバージョンを作る）

次のバージョンに変更を追加する（ステージ）

<img src="./img/6289d3003c94150a6284934d.png" style="width:950px;"/>

コミットメッセージ（新しいバージョンの変更点：何の機能を追加したか）を書いてコミット
（ctrl + Enterでもできる）

<img src="./img/6289d3003c94150a6284934e.png" style="width:950px;"/>

Gitログ（変更記録）を見る

<img src="./img/6289d3f73c94150a6284969d.png" style="width:950px;"/>


<details><summary>コマンド ver.</summary>


```bash
# Main.javaをコミットに含める
$ git add Main.java

# コミットメッセージをつけてコミット
$ git commit -m '[add] Hello, world!'
```
<img src="./img/6289d3d23c94150a62849629.png" style="width:950px;"/>

</details>



### GitHubでリモートリポジトリ作成

リポジトリ作成

<img src="./img/6289da0d3c94150a62849c26.png" style="width:950px;"/>

リポジトリ名、公開/非公開を決める

<img src="./img/6289da0d3c94150a62849c03.png" style="width:950px;"/>
<img src="./img/6289da0d3c94150a62849c0e.png" style="width:950px;"/>

URLのコピー

<img src="./img/6289da0d3c94150a62849c16.png" style="width:950px;"/>

### リモートリポジトリ登録

リモートの追加

<img src="./img/6289e46d3c94150a6284a778.png" style="width:950px;"/>

コピーしたURLを入力してEnter

<img src="./img/6289e46d3c94150a6284a776.png" style="width:950px;"/>

`origin`と入力してEnter

<img src="./img/6289e46d3c94150a6284a780.png" style="width:950px;"/>

### リモートリポジトリにプッシュ（アップロード）

<img src="./img/6289e34d3c94150a6284a5e9.png" style="width:950px;"/>



<details><summary>コマンド ver.</summary>

originという名前をつけてリモートリポジトリを追加する

```bash
$ git remote add origin <コピーしたurl>
```

head（今いるバージョン）をoriginにプッシュする

```bash
$ git push origin head
```

<img src="./img/6289da0d3c94150a62849c00.png" style="width:950px;"/>

</details>

### 確認

<img src="./img/6289da0d3c94150a62849c1e.png" style="width:950px;"/>


### 新しいバージョンを作ってプッシュしてみる

```diff
-       System.out.println("Hello, world!");
+       System.out.println("Hello, git!");
```

<img src="./img/6289df8f3c94150a6284a168.png" style="width:950px;"/>
<img src="./img/6289df8f3c94150a6284a175.png" style="width:950px;"/>

#### コミット

<img src="./img/6289df8f3c94150a6284a19c.png" style="width:950px;"/>
<img src="./img/6289df8f3c94150a6284a174.png" style="width:950px;"/>
<img src="./img/6289e5063c94150a6284a977.png" style="width:950px;"/>

#### プッシュ

<img src="./img/6289e4ec3c94150a6284a8e1.png" style="width:950px;"/>
<img src="./img/6289e5a63c94150a6284abbc.png" style="width:950px;"/>


<details><summary>コマンド ver.</summary>

```bash
$ git add Main.java
$ git commit -m '[update] hello world -> hello git'
$ git push origin head
```

<img src="./img/6289df8f3c94150a6284a178.png" style="width:950px;"/>

</details>

#### 確認

<img src="./img/6289df8f3c94150a6284a18e.png" style="width:950px;"/>
<img src="./img/6289df8f3c94150a6284a187.png" style="width:950px;"/>