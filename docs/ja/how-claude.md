# How Claude Code works here（日本語）

![How Claude Code works here 図](../../assets/diagrams/how-claude-v4.png)

Claude Code はリポジトリ内の**実装者**であり、プロダクトオーナーではない。

プロファイル図の詳細説明。[English](../how-claude.md) · 関連: [How I ship](./how-i-ship.md) · [知識が積み上がる仕組み](./how-knowledge.md)

---

## 役割の分割

| Claude Code が **読む** | Claude Code が **する** | Claude Code が **持たない** |
|-------------------------|-------------------------|------------------------------|
| Issue · 受入条件 | スコープ内のブランチ変更 | プロダクトスコープ |
| プロジェクトルール · 関連 docs | tests · build | レビュー判断 |
| | | **main へのマージ** |

hands-on 検証を Claude 単独とは書かない。図の DOES は、Claude が回しがちな自動チェック中心。必要なときの人間の hands-on は残る。

---

## 実装のあと（How I ship と同じ順序）

フルの ship ループと揃え、ゲートを飛ばさない。

1. **Codex レビュー**  
   Issue スコープに対する敵対レビュー。指摘は候補。

2. **人間の判断**  
   指摘の採否は自分が決める。Claude が「どの指摘を残すか」を決めない。

3. **PR を開く（Claude Code）**  
   Claude が PR を開き、Issue をリンクし、判断を記録する。  
   **PR を開くこと ≠ マージすること。**

4. **自分がマージする（人間ゲートのみ）**  
   main へのマージは自分。ChatGPT が議論を手伝うことはあるが、マージ決定は人間。

---

## なぜこの形か

- **「AI が出荷した」劇を避ける。** 実装の手伝いはするが、スコープとマージは持たない。  
- **private の実践と一致。** 人間がブレイン（決定・マージ）、Claude がプログラマ（ブランチ・PR）、PR 前に敵対レビュー。  
- **How I ship より短い。** ここは Claude の境界の話であり、マルチツール全体の物語ではない。

---

## これは何か／何ではないか

- 「Claude Code がマージしてくれる」ではない  
- 「Claude がロードマップを持つ」ではない  
- [How I ship](./how-i-ship.md) の完全な代替ではない（フレーミング、Issue 制御、本番、revise 経路など）

---

## クロスリファレンス

| 知りたいこと | 読む |
|--------------|------|
| マルチツールの全体ループ | [How I ship](./how-i-ship.md) |
| claim と Issue の出どころ | [知識が積み上がる仕組み](./how-knowledge.md) |
