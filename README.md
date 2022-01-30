# git の基本的な使い方

## 習得する必要のあること
git add . 
git add <filename>

git branch 
git branch <new branch name>
git branch -d <target branch> 

git checkout <branch name>

git log
git log --oneline --graph

git push
git merge
git pull

git status

#コミットをきれいにする 基本的にはpushしていないもの。
git commit --amend
git rebase
git rebase -i
git rebase -i HEAD~3

# コミット修正について
## git commit --amend 
直前のコミットを修正する

## rebase コミットの順番を入れ替える、削除する
完了したら git rebase --continue

## rebase コミットを纏める
```
例
$ git rebase -i HEAD~3

pick a5227db 1111
pick dab658f 222
pick b18bf3d 333
pick 900d91a 444

を

squash a5227db 1111
squash dab658f 222
squash b18bf3d 333
squash 900d91a 444

としてコミットメッセージを "rebase12345" とかにすると
69f6caeとなる。rebase12345

% git log --oneline -n 3
69f6cae (HEAD -> dev01) rebase12345
de1e56a (origin/main, origin/HEAD, main) delete dev.txt
d6fd43a Merge pull request #6 from bui2jp/feature/dev1

```



 
 

git remote
git remote -v
 
