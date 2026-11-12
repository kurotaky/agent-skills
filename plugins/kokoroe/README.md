# kokoroe

作者がAIとの作業で受けた指摘と、うまくいった進め方から抜き出した心得を集めたガイドライン群です。AIが必要だと判断した時に読み込みます。手動でも起動できます。

## 含まれるスキル

- **writing**: どこに書く時も変わらない文章の書き方。「効く」「ゲート」のような回りくどい語を避け、何が起きるかを言い切る
- **code-comment**: コメントには今の状態だけを書き、変更の経緯を書かない。コードを消す時はコメントごと消す
- **user-decision**: ユーザーに確認する時と確認せずに進める時の線引き。元に戻せない操作の最後の一手をユーザーに残す事と、報告の訂正の仕方
- **second-opinion**: Codex CLIに自分の主張を反証させ、指摘を自分で確かめてから採用する進め方
- **git-worktree**: worktreeのブランチの起点を確かめ、PRに無関係なcommitを混ぜない

## 使い方

```bash
/kokoroe:writing
/kokoroe:code-comment
/kokoroe:user-decision
/kokoroe:second-opinion
/kokoroe:git-worktree
```

## インストール方法

マーケットプレイスを登録してから、pluginをインストールします。

```bash
/plugin marketplace add kurotaky/agent-skills
/plugin install kokoroe --marketplace kurotaky/agent-skills
```

既にマーケットプレイスを登録済みの場合、新しいスキルをインストールするには [マーケットプレイスの更新](../../README.md#スキルをうまくインストールできない場合) が必要です。
