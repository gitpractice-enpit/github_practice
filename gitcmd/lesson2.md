## Gitコマンドメモ
### Lesson 2
1. ローカルレポジトリを作る

	```
 % mkdir chiemirepo <-名前は適当につけてください。Githubにあげます
 % cd chiemirepo
 % git init .
 
	```
2. ファイルreadme.mdをステージに上げてコミットする

	```
 (ファイルをreadme.mdを作って中身を適当に書く)
 % git status
  ...(略）
 Untracked files:
  (use "git add <file>..." to include in what will be committed)

	readme.md
  ...(略）
 % git add readme.md
 % git status
  ...(略）
  Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   readme.md
  ...(略）
 % git commit -m "initial commit"
	```
3. readme.mdを変更してコミットする

	```
 （ファイルの中身を適当に変更する）
 % git status
  ...(略）
  Changes not staged for commit:
  ...(略）
	modified:   readme.md 
  ...(略）
  % git add readme.md
  % git status
  ...(略)
  % git commit -m "（変更内容の概要を書く）"    
	```
4. 