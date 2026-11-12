---
name: git-worktree
description: >-
  git worktreeで作業を始める時の心得。worktreeのブランチがどのcommitから作られたかを確かめ、PRに無関係なcommitを混ぜない事を定める。
  修正やPRのためにworktreeを作った時、worktreeでcommitやpushをする前に読み込む。
---

# git worktreeで作業を始める時の心得

worktreeを作った時と、worktreeでcommitする前は、以下の基準に従う。

## 心得1. worktreeの起点を確かめる

worktreeを作るツールによっては、default branchではなく、作業中のブランチのHEADから新しいブランチを作る。そのままPRを作ると、作業中のブランチのcommitが混ざり、差分が無関係な変更で膨らむ。

worktreeを作ったら、commitする前に、default branchとの差分に自分のcommit以外が無いかを確かめる。`git log --oneline origin/<default branch>..HEAD` で確かめられる。

## 心得2. 混ざっていたら起点から作り直す

無関係なcommitが混ざっていたら、default branchの最新を取得し、そこにresetしてから作業をやり直す。既に自分のcommitがあるなら、resetの後にcherry-pickで載せ直す。
