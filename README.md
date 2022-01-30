# git-work

mergeには３つ
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



feature2  
Pull Request

git hub flow 
