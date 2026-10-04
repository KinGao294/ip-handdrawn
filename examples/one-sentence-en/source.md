# English 示例：一句话也能配图

三句英文，忠实转述自中文原文《AI时代最重要的三点思考》（[article.md](../kin-three-points/article.md)）的关键句。每句单独作为输入，各生成一张图，图里的手写批注全部用英文。

1. AI is not a 100-meter sprint; it's a 20-year marathon.
   → `images/01-marathon.png`（原文：「因为它确实不是一场百米冲刺，而是未来 5 年、10 年、20 年的一场马拉松。」）
2. AI has opened up the boundaries of every job.
   → `images/02-boundaries.png`（原文：「职业的边界被 AI 打开了，也更适合超级个体去闯。」）
3. Research gives me input, content gives me reach — two wheels turning together.
   → `images/03-two-wheels.png`（原文：「研究给我输入，输出给我放大……两个轮子一起转，飞轮才转得起来。」）

生成方式：Codex CLI，每张一次调用，附奶龙参考图，提示词从 stdin 传入：

```bash
codex exec --skip-git-repo-check -i assets/character/nailong/ref-front-clean.png - < examples/one-sentence-en/prompts/01-marathon.txt
```
