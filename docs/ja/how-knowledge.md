# How knowledge compounds（日本語）

![How knowledge compounds 図](../../assets/diagrams/how-knowledge-v2.png)

チャットは下書き。claim には証拠が要る。何が生き残るかは outcome が決める。

プロファイル図の詳細説明。[English](../how-knowledge.md) · 関連: [How I ship](./how-i-ship.md) · [ここでの Claude Code](./how-claude.md)

---

## 置き場所

| 置き場 | 役割 |
|--------|------|
| **Obsidian** | claim・判断メモ・調査の取り込み（第2の脳） |
| **repo docs / ADR** | **プロダクトに効く**決定——リポジトリ上の共有された正になるとき |
| **GitHub Issue** | **変更**のスコープ（受入条件、作業単位） |

「知識は全部 Obsidian」「すべてのリポが何でも SSOT」とは言わない。個人の判断・プロダクト決定・実装可能な変更のどれかで置き場が変わる。

---

## 段階

### CAPTURE（vault）

1. **証拠を観察する**  
   調査、現場フィードバック、レビュー、障害、ユーザー反応——失うと惜しいもの。

2. **claim を正規化する** → **Obsidian**  
   観察を、証拠・用途・リスク付きの claim にする。  
   ふわっとしたチャットが、後から戻れる形になる地点。

### DECIDE（docs のあと Issue）

3. **決定の文脈を記録する** → **repo**（プロダクトに効くとき）  
   チャットより長く生き残り、ソフトウェアの作り方に効くなら docs / ADR。  
   卒業前の判断メモは vault に残してよい。

4. **スコープと受入を定義する** → **GitHub Issue**  
   基準、一度に一つの変更。  
   docs と Issue は分ける: docs は *何が真か*、Issue は *次に何を変えるか*。

### BUILD（repo）

5. **ブランチで実装する**  
   スコープ内の変更。ツールとゲートの詳細は [How I ship](./how-i-ship.md)。

6. **振る舞いを検証する**  
   tests · build · hands-on（必要なとき）。「CI が緑だけ」ではない。

### LEARN（vault へ戻る）

7. **outcome を評価する**  
   信じたことを promote / revise / reject。  
   **learn → next claim（Obsidian）:** すべての outcome が claim に昇格するわけではない。弱めたり捨てたりする。

---

## 出荷との接続

知識 → Issue が、調査を制御された変更にする道。  
claim なしの出荷は同じ学びを繰り返す。  
outcome なしの claim は、体裁のいい意見にすぎない。

---

## これは何か／何ではないか

- 「全部 vault に永久保存」ではない  
- 「チャット履歴が正本」ではない  
- [How I ship](./how-i-ship.md) の代替ではない——変更の**周囲**の長い弧
