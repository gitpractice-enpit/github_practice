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
4. コミット間の差分を見る

```
% git reflog
f878356 HEAD@{0}: commit: add oneliner message
92624c9 HEAD@{1}: commit (initial): first commit
% git diff f878356..92624c9
diff --git a/readme.md b/readme.md
index 6b53b90..85e8053 100644
--- a/readme.md
+++ b/readme.md
@@ -1,3 +1 @@
# Chiemi's Repository
-* GitやGithubの勉強をしています   
```

5. Github上にレポジトリを作り、ローカルレポジトリをGithubにあげる

```
(GithubのWebページで新しいレポジトリを作成する)
% git remote add origin (リモートレポジトリのURL)
% git push -u origin master
```
