## コンフリクトを解消する
Pull Requestを送ったらコンフリクトしてしまい、どうして良いか分からずレポジトリを消してしまった場合の対処。

### やることの概要
* ローカルレポジトリのmasterを最新にし、ブランチとマージする。
* その時にローカルレポジトリでコンフリクトが生じるので手動で解消する。
* コンフリクトを解消したブランチをコミットしてpushすると、リモートレポジトリでマージが可能になります。

### 手順
1. fetchする：リモートレポジトリの最新状況をローカルに取得します
	
	```
	% git fetch
	```
1. ブランチをmasterとマージさせる

	```
	% git checkout conflictdemo_C
	% git merge master
	```
	ここでコンフリクトが発生したと言われます。
	
	```
	Auto-merging member.md
	CONFLICT (content): Merge conflict in member.md
	Automatic merge failed; fix conflicts and then commit the result.
	```
	ファイルを開くとこんな風になってます。
	
	```
	# 作成者
	* chiemi627, 子育て頑張り中
	
	<<<<<<< HEAD
	* コンフリクトのデモンストレーション
	  * ブランチAが書き込みをしましたよ
	  
	* ブランチCからもプルリクしてみます
	=======
	* コンフリクトの説明用デモ
	  * ブランチAが書き込みしましたよ。
	  * ブランチBでの書き込みです。
	  * ブランチCから追記。コンフリクトは起きませんよね。
	>>>>>>> master  
	```
	* <<<<<<< HEADから=======までがブランチの内容で、
	その下からmasterまでがmasterの内容です。
	* 自動ではマージできなかったので、手動で編集します。
	* 例えばこんな感じで。

	```
   # 作成者
   * chiemi627, 子育て頑張り中

   * コンフリクトのデモンストレーションです
     * ブランチAが書き込みしましたよ。
     * ブランチBでの書き込みです。
     * ブランチCからもプルリクしてみます。                        	
	```
	* <<<<<<<<や========はもう必要ないので消してください。
1. コミットする

	```
	% git add member.md
	% git commit -m "conflictdemo_Cの衝突解消"
	``` 
1. pushする

	```
	% git push origin conflictdemo_C
	```
	* GithubのPull Requestを確認してください。
	* 自動マージができるようになっています。
