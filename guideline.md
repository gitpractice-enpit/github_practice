## 自習ガイドライン
### 注意：
* このテキストにはe-Learning動画コンテンツを元にした自習の流れが書かれています。
* GitやGithubの詳細な説明はありません。GitやGithubについては参考資料等をみながら各自調べましょう。
* 各レッスンで課題を出しています。成績には影響しませんが、5/17の講義準備で参考にします。是非提出してください。（超簡単です）

## Lesson 1 : 環境を整えよう

1. e-Learning動画コンテンツを入手する
 * URLとアカウント情報は[manaba](https://manaba.tsukuba.ac.jp/ct/page_785369c785019_805428805)から入手のこと（enPiT履修者限定のため）
 * 以下動画を使いながら自習すると良いでしょう
2. Githubのアカウントを作成
3. Gitを使う環境を整える
   * GUI派の皆さん：SourceTreeをインストール
      * Gitが入ってなければインストールされるはず
   * コマンド派の皆さん：ターミナルでGitをインストール

### 参考資料
* 「Git and Github集中特訓」の動画 (１〜５本目）
  * 動画ではSourceTreeを使うことが前提になっています。

### 課題
* Githubアカウントをmanabaでお知らせ下さい
	* [manabaの課題へのリンク（筑波大生用）](https://manaba.tsukuba.ac.jp/ct/course_785019_query_798012)
	* [manabaの課題へのリンク(参加校生)](https://manaba.tsukuba.ac.jp/local/course_785019_query_798012)  
	* Github演習のためのグループ（http://github.com/gitpractice-enpit）に追加します

## Lesson 2 : ローカルレポジトリを作ってGithubにあげよう
1. ローカルレポジトリを作りましょう
2. ファイルを作って中身を適当に書き、ステージに上げてコミットしてみよう
3. さらに何か書いたり消したりしてコミットしてみよう
4. コミット間の差分を見てみよう
5. [Githubでリモートレポジトリをつくり、ローカルレポジトリをリモートにあげよう](doc/remoteadd.md)

### 参考資料
* 「Git and Github集中特訓」の動画（６〜９本目）
  * Lesson2の1-4までしか解説されてません
  * 5についてはリンク先のページを参考になんかやってみてください。
* [Gitコマンド派のLesson2メモ帳](gitcmd/lesson2.md)

### 課題
* GithubにあげたレポジトリのURLをmanabaでお知らせ下さい。
	* [manabaの課題へのリンク(筑波大生)](https://manaba.tsukuba.ac.jp/ct/course_785019_query_798028)
	* [manabaの課題へのリンク(参加校生)](https://manaba.tsukuba.ac.jp/local/course_785019_query_798028)

## Lesson 3: リモートレポジトリをフォークしていじろう
1. http://github.com/gitpractice-enpit/practicememo.git をフォークしよう
2. ローカルリポジトリにクローンしよう
3. membersディレクトリの下に<アカウント名>.mdというファイルを追加し、自己紹介を書いてコミットしよう
4. リモートレポジトリにプッシュしよう

### 参考資料
* 「Git and Github集中特訓」の動画（１０〜１６本目）

### 課題
* フォークしたURLを教えてください
	* [manabaの課題へのリンク(筑波大生)](https://manaba.tsukuba.ac.jp/ct/course_785019_query_798034)
	* [manabaの課題へのリンク(参加校生)](https://manaba.tsukuba.ac.jp/local/course_785019_query_798034)

## Lesson 4: プルリクエストを送ろう
1. http://github.com/gitpractice-enpit/practicememo.gitにプルリクエストを送ろう

### 参考資料
* 「Git and Github集中特訓」の動画（１７本目）

### 課題
* プルリク送ってください
  * プルリクきたらすぐにマージします。そしてcollaboratorに追加します。

## Lesson 5: リセットをしてみよう
1. practicememoのローカルレポジトリのファイルをいじってステージに上げてそれをとり消そう
2. practicememoのローカルレポジトリのファイルをいじってコミットしてそれをとり消そう

### 参考資料
* 「Git and Github集中特訓」の動画（１８本目）

### 課題
* 特になし

## Lesson 6: ローカルでブランチを切ってマージしよう
ブランチの練習ついでにForkしたレポジトリの最新状態を取り込みます。

1. practicememoでdiaryブランチを作ろう
2. diaryブランチにチェックアウトしてdiary/<アカウント名>.mdファイルを作って今日の作業メモを書いてコミットしよう
3. masterにチェックアウトしてfork元のレポジトリをfetchしよう
  * え、これ何やってるの？イミワカランという人は[こちら](doc/fetch_merge.md)
4. masterにdiaryブランチをマージしよう

### 参考資料
* 「Git and Github集中特訓」の動画（２０〜２２本目）

### 課題
* マージし終わったレポジトリをfork元にプルリクしよう

## Lesson 7: Fork使わないプルリクをしよう
### 前提
* practicememoレポジトリのcollaboratorに追加されていること。
* されていなかったらご一報ください。

### 手順
1. practicememoのmasterブランチでpullしよう
2. <アカウント名>_<diary>ブランチを作ってチェックアウトしよう
3. diary/<アカウント名>.mdファイルを編集してステージに上げてコミットしよう
4. <アカウント名>_<diary>ブランチをプッシュしよう
5. Githubサイト上でプルリクエストを送ろう

### 参考資料
* https://b.pyar.bz/blog/2014/01/22/github-flow/ 

### 課題
* プルリクエスト送ってください（つまり上記の5.をやってください）

## Lesson 8: プルリクされたものをレビューしよう
1. https://github.com/gitpractice-enpit/practicememo のpull requestメニューを見てみよう
2. 差分を見てコメントをしてみよう。
3. プルリクされたリモートブランチをローカルに持ってきてmasterにマージして見てみよう
  * そこで何か気がつけばコメントをしてください。
4. マージして良さそうなものにマージOKのコメントをつけましょう。

### 課題
* practicememoの誰のpull requestにどんなコメントをしたかmanabaに報告しましょう。

## Lesson 9: プルリクされたものをマージしよう
（近日公開予定）

## Lesson 10: Issueを使ってみよう
（近日公開予定）

## Lesson 11: Issueを解決してみよう
（近日公開予定）
