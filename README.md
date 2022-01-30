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

## コミットを修正
git commit --amend で１個づつ修正していく
完了したら git rebase --continue

## コミットの順番を入れ替える、削除する


## コミットを纏める
git rebase -i HEAD~3

 
 

git remote
git remote -v
 
