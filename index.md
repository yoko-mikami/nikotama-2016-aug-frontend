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
	![]({{site.baseurl}}/Screenshot%202016-07-23%20at%2009.07.27.png)
    - ** Pick a username **に　ユーザ名
    - ** Your email address ** にあなたのメールアドレス
    - ** Create a password ** にパスワードを入れます
    - 最後にSign up for Githubをクリックします
    
{% include click_me.html %}
