# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？
- A.リポジトリはフォルダ（箱）のような物、リモートリポジトリはネット上にあり、複数人で共有できるリポジトリ。ローカルリポジトリは自身のPC上にある自身が使用するリポジトリ


## プッシュとマージの違いは何でしょうか？
- A.プッシュはローカルリポジトリの内容をリモートリポジトリに上げる（反映）操作　⇨ git push origin  ブランチ名
  
+ マージはメインブランチ以外のブランチで作業した内容をメインブランチに統合する操作　例えばmainにブランチ名Bを統合させたいときはgit branch でmain
に移動した状態で⇨ git merge ブランチ名B  

## コミットとプッシュの違い
- コミットはaddによってステージング（更新する準備ができた状態）に上げた変更を履歴として記録すること。記録しないとリモートリポジトリに上げられない
+ プッシュはコミットした変更をリモートリポジトリに反映させること　　　　　⇨ git push origin(リモートリポジトリのディフォルト名)　ブランチ名


## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
- わかりやすくどんな変更を行ったかわかるようなコメントにする。
+ 例えば'index.htmlの1列目のカードの表示名を変更'のように具体的に書きます。


## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
- プルリクエストはブランチをリモートリポジトリに上げそこからメインリポジトリにマージする際にレビュワーにレビュー（チェック）してもらう。
+ ローカルでマージしたメインブランチをリモートリポジトリに上げるフローは上記に比べて工程が少なく早いがチェック無しに統合するので欠陥があった際は大規模な修正が必要になる（pushしてしまうと戻せなくなるため）



## コンフリクトを起こしてしまった場合、どう対処すべきですか？
- 例えばAが先にマージしていた物にBが後から追加した場合は
+ 1.Aを取り込む 　
* 2.Bを取り込む
- 3.両方を取り込む
+ 3を選ぶ場合はエディタで両方のコードを取り込んだ状態で上書きするが相手のコードを完全に理解してないといけないため、被った相手とよく話し合う必要がある。