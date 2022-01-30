コミットの修正
コミットをまとめる

33333

commitメッセージの書き換え
push していないcommit の修正

git commit --amend 直前のコミットを修正する
git rebase -i 複数のコミットをまとめる 

githubで修正

# git-work
merge
1. fast Forward :  ブランチのポインタが進むだけ　新たなコミットはできない
2. Auto Merge   :  マージコミットという新たなコミットができる
                   マージコミットは親を２つ持っている
3. コンフリクト：
  
GitHub Flowとは
 単純なフロー
　
　mainからブランチ作成
  branch ->  pullrequest -> main -> deploy 

  mainブランチは常にリリースできる状態を保つ
  直接mainの変更は行わない
　mainへはかならずPRを通す
　mainの変更はすぐにデプロイする

特徴
　シンプルなワークフロー
　単純なので誰でも参加しやすい
git rebase master

Merge : コミットがいっぱいできる
        コンフリクトの解決が簡単
　　　履歴を残したい場合はこちら

Rebase: 履歴をきれいにできる
　　　　コンフリクトの解決が面倒


コンフリクトの解消の違い


rebaseの場合、それぞれのコミット単位でrebaseが実施される
コンフリクトがある場合、それぞれでコンフリクトが発生する






