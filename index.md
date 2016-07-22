--- 
layout: template1 
---
## Gitのインストール
1. 現在(2016/06)では、[git for windows](https://git-for-windows.github.io/)というサイトからダウンロードできます。サイトのdownloadボタンを押すと64bitか32bitかは勝手に判断してくれるはずです。(選ぶ操作がなかった)
2. ダウンロードが完了すると、ダウンロードした実行形式ファイル(.exe)を実行してインストールしていきます。英語だらけでわからんという人は、以下の通りで大丈夫です。
3. 
上部に太字で"Select Components"と書かれているコンポーネントの選択画面では、何も変更しないでNextボタンを押下して下さい。
4. 
次に上部に太字で"Adjusting your PATH environment"と書かれた環境変数の設定画面に移ります。そこではGit Bashというプロンプトのみを使用する場合は一番上の「Use Git Bash only」を選択してNextボタンを押下してください。
5. 次に上部に太字で"Configuring the line ending conversions"と書かれた改行コードの変換画面に移ります。そこでは、GitHubではMacやLinuxで使用されているLF(Line Feed)で改行が行われています。WindowsはCRLF(Carriage Return + Line Feed)で改行するのでGitが自動変換を行ってくれる設定があるのでその設定である「Checkout Windows-style,commit Unix-style line endings」を選択してください。
6. これで無事にアプリケーションに「Git Bash」が追加されていると思うので、起動してください。するとコマンドプロンプト風のCLI(command line interface)が立ち上がると思うので、そこから初期設定を行うのですが、これは次回書いていきたいと思います。

{% include click_me.html %}
