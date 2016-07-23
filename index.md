--- 
layout: template1 
---
## Gitのインストール(Windows版)
1. [git for windows](https://git-for-windows.github.io/)というサイトに行きます。
2. 
2. ダウンロードが完了すると、ダウンロードした実行形式ファイル(.exe)を実行してインストールしていきます。英語だらけでわからんという人は、以下の通りで大丈夫です。
3. 
上部に太字で"Select Components"と書かれているコンポーネントの選択画面では、何も変更しないでNextボタンを押下して下さい。
4. 
次に上部に太字で"Adjusting your PATH environment"と書かれた環境変数の設定画面に移ります。そこではGit Bashというプロンプトのみを使用する場合は一番上の「Use Git Bash only」を選択してNextボタンを押下してください。
5. 次に上部に太字で"Configuring the line ending conversions"と書かれた改行コードの変換画面に移ります。そこでは、GitHubではMacやLinuxで使用されているLF(Line Feed)で改行が行われています。WindowsはCRLF(Carriage Return + Line Feed)で改行するのでGitが自動変換を行ってくれる設定があるのでその設定である「Checkout Windows-style,commit Unix-style line endings」を選択してください。
6. これで無事にアプリケーションに「Git Bash」が追加されていると思うので、起動してください。するとコマンドプロンプト風のCLI(command line interface)が立ち上がると思うので、そこから初期設定を行うのですが、これは次回書いていきたいと思います。

## githubアカウント作成
1. [github](https://github.com/) というサイトに行きます。
	- **Pick a username**にユーザ名
	- **Your email address**にあなたのメールアドレス
	- **Create a password**にパスワードを入れます
	- 最後に**Sign up for Github**をクリックします
	- ![]({{site.baseurl}}/screenshots/github01.png)
2. https://github.com/join/plan というページに遷移しています。
	- **Unlimited public repositories for free**.が選択されていることを確認します
	- **Continue**をクリックします
	- ![]({{site.baseurl}}/screenshots/github02.png)
3. https://github.com/join/customize というページに遷移しています。
	- **skip this step**をクリックします
	- ![]({{site.baseurl}}/screenshots/github03.png)
4. https://github.com/dashboard というページに遷移したら　アカウント作成完了!
	- ![]({{site.baseurl}}/screenshots/github04.png)
5. 最後にメールを確認
	- **[GitHub] Please verify your email address**. というメールが着ているのを確認
    - **Verify email address** をクリック
    
## demo アプリをforkしてみよう
1. https://github.com/freddiefujiwara/nikotama-2016-aug-frontend/ というページに行きます
	- 右上にある**Fork**というアイコンをクリック
    - ![]({{site.baseurl}}/screenshots/fork01.png)
2. https://github.com/[あなたのアカウント]/nikotama-2016-aug-frontend というページができたらfork完了

## demo アプリをクローンしてみよう
1. https://github.com/[あなたのアカウント]/nikotama-2016-aug-frontend/ に行きます。
	- 緑のボタンClone or downloadをクリックします
    - ![]({{site.baseurl}}/screenshots/clone01.png)
2. 中に表示されているテキストボックスをコピーしておきます.
3. 先ほどセットアップした黒い画面コンソールにて下記を打ち込みます

```bash
$ git clone https://github.com/nikotama201601/nikotama-2016-aug-frontend.git                             ```
そうすると。。。

```bash
Cloning into 'nikotama-2016-aug-frontend'...
remote: Counting objects: 203, done.                                                                                          
remote: Compressing objects: 100% (97/97), done.                                                                              
remote: Total 203 (delta 51), reused 0 (delta 0), pack-reused 103                                                             
Receiving objects: 100% (203/203), 1.13 MiB | 650.00 KiB/s, done.
Resolving deltas: 100% (88/88), done.
Checking connectivity... done.
```
上記のような表示がでてきて... done.となったらclone完了

4. ファイルを確認してみよう
下記のコマンドを打って　clone したフォルダに移動しています

```bash
$ cd nikotama-2016-aug-frontend/ 
$ ls -lha
```

そうすると下記のようにファイルが見えるはずです

```bash
total 1.9M                                                                                                                    
drwxrwxr-x  4 fumikazu fumikazu 4.0K Jul 23 11:11 .
drwxr-xr-x 24 fumikazu fumikazu 1.9M Jul 23 11:11 ..
drwxrwxr-x  2 fumikazu fumikazu 4.0K Jul 23 11:11 api
drwxrwxr-x  8 fumikazu fumikazu 4.0K Jul 23 11:11 .git
-rw-rw-r--  1 fumikazu fumikazu 1.1K Jul 23 11:11 index.html                                                                  
-rw-rw-r--  1 fumikazu fumikazu 1.1K Jul 23 11:11 LICENSE                                                                     
-rw-rw-r--  1 fumikazu fumikazu   29 Jul 23 11:11 README.md
```

## アプリを動かしてみよう 
1. index.html というファイルをブラウザで開いてみます
そうすると。。　下記のような"CLick ME!"というボタンがあるのでおしてみてください

{% include click_me.html %}

## アプリを編集してみよう
1. index.html をテキストエディタで開いてみよう

```JavaScript
$nikotama.get('https://rawgit.com/freddiefujiwara/nikotama-2015-Aug/master/api/get.js',function(data){
```

という行を

```JavaScript
$nikotama.get('https://api.github.com/users/freddiefujiwara',function(data){
```

に変更して保存しよう

2. index.html をもう一回ブラウザで開いてみます.
そうすると。。　下記のような"CLick ME!"というボタンがあるのでおしてみて　前と動きが変わったことを確認してください

{% include click_me_github.html %}
