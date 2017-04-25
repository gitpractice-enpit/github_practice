## Lesson6の状況解説

### 何をやっているのか
レポジトリをForkすると、その後Fork元が更新されたりして、Forkしてきたコードが古くなる場合があります。

![](img/fork_merge2.png)

その時masterを最新の状態にして、ローカルの状態とマージしてあげましょう。

### masterをfork元の最新状態と同期してマージする手順
![](img/fork_merge3.png)

1. fork元に名前をつける（ここではupstreamという名前をつけている）

  ```
% git remote add upstream https://github.com/....  
  ```
  
2. masterへ移動してfetchする
 
  ```
  % git checkout master
  % git fetch upstream
  ```
  
3. mergeする
 
  ```
  % git merge diary

  ```
