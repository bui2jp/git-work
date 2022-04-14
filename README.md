# git の基本的な使い方

## 最低限、習得する必要のあること
```
git branch 
git branch <new branch name>
git branch -D <target branch> 

git checkout <branch name>
git checkout -b <branch name>

git status

git log
git log --oneline --graph

git add . 
git add <filename>

git commit
git commit -m
git commit --amend

git merge
git rebase

git push
git pull

git remote
git remote -v
```

# rebaseでのコミット修正について

rebaseの２つの主要な機能
```
1. 繋げ直す
2. 纏める
```

失敗したらしたら git rebase --abort  
完了したら git rebase --continue  


## rebaseでコミットを繋げ直す
```
$ git rebase [main]
```

## rebaseで複数のコミットを纏める
```
$ git rebase -i [まとめる地点のひとつ前のID]
```

例
```
$ git rebase -i HEAD~3

pick a5227db 1111
pick dab658f 222
pick b18bf3d 333
pick 900d91a 444

を (squashのsに変更)

pick a5227db 1111
s dab658f 222
s b18bf3d 333
s 900d91a 444

としてコミットメッセージを "rebase12345" とかにすると
69f6caeとなる。rebase12345

% git log --oneline -n 3
69f6cae (HEAD -> dev01) rebase12345
de1e56a (origin/main, origin/HEAD, main) delete dev.txt
d6fd43a Merge pull request #6 from bui2jp/feature/dev1

```

# Merge と Rebase の違い

| ---- | Merge | Rebase | 
| ---- | ---- | ---- |
| 既存のコミットに影響を | 与えない | 与える |

rebase は共同開発の現場では、他人のコミットを変更してしまう可能性がある。利用する場合注意して。push していない、ローカルの開発内容であれば基本的に Rebase しても問題なし。
