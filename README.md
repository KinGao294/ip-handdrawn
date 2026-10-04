# Nailong-image · 奶龙正文配图 Skill

> A skill for generating hand-drawn 16:9 article illustrations starring the 奶龙 (Nailong) mascot.

把中文文章里的关键判断、流程、隐喻，变成一张干净、有记忆点、一眼能看懂的手绘解释图——由胖乎乎的橙黄色小奶龙来「认真做一件有点荒诞但成立的事」。

完整规则见 [SKILL.md](SKILL.md)，可直接放进你的 AI 助手（Codex / Claude / Cursor 等）的 skills 目录使用。

## 风格规则速览

- **16:9 横版**，**纯白背景**，黑色手绘线稿，大量留白。
- **奶龙是唯一的彩色元素**：保留招牌橙黄色，其他物件一律纯黑线稿、不填色。
- **奶龙必须是核心动作主体**，不能只是站在旁边当装饰。
- 只加**少量红 / 蓝中文手写批注**，宁少勿错。
- 禁止 PPT / 信息图感，禁止左上角类型标题、水印、签名。
- 每张图只讲一个核心结构；每篇文章重新发明隐喻，不复刻旧图。
- 参考图只锁定奶龙形象（体型、大绿眼睛、奶油色肚皮），不照抄场景和动作。

## 怎么用

1. **出策略**：把文章丢给助手，先产出 shot list（放在哪段后、核心意思、结构类型、奶龙在做什么、标注词），默认 4–8 张。
2. **逐张生成**：每张图单独调用一次生图，**先附奶龙参考图，再给提示词**。以 Codex CLI 为例：

   ```bash
   codex exec --skip-git-repo-check -i assets/character/ref-front-clean.png - < prompt.txt
   # 例如直接复用案例提示词：
   codex exec --skip-git-repo-check -i assets/character/ref-front-clean.png - < examples/kin-three-points/prompts/01-marathon.txt
   ```

   注意：`-i` 可以接多个文件，所以提示词要用 `-` 从 stdin 传入，避免被当成图片路径。默认参考图是 `ref-front-clean.png`（干净正面定妆图），`ref-front.png` 为备用。

   一次调用只出一张图，不要把多张拼在一起。提示词结构可参考 [`examples/kin-three-points/prompts/`](examples/kin-three-points/prompts/)。
3. **QA 与迭代**：检查奶龙是否走样、是否只是装饰、画面是否太满、中文是否写错、背景是否干净，有问题就重生成。
4. **保存**：按 `assets/<article-slug>-illustrations/01-topic.png` 顺序命名，不覆盖已有文件。

## 目录结构

```text
SKILL.md                     # Skill 本体
assets/character/            # 奶龙角色参考图（默认 ref-front-clean.png）
examples/kin-three-points/   # 完整案例：原文 + shot list + 成图 + 提示词
LICENSE                      # MIT
```

## 案例：《AI 时代我最近想得最多的三个点》

原文：[article.md](examples/kin-three-points/article.md) ｜ 配图策略：[shotlist.md](examples/kin-three-points/shotlist.md) ｜ 提示词：[prompts/](examples/kin-three-points/prompts/)

> 📌 **案例图同时也是奶龙角色参考图。** 除 `assets/character/` 下的参考图外，下面 6 张成图里的奶龙形象稳定一致，也可以作为 `-i` 参考图传入，帮助锁定不同动作、姿态下的奶龙。

**01 不是冲刺，是马拉松** —— 奶龙拆掉起跑器挂上吊床，在 5 年 / 10 年 / 20 年的里程牌旁打盹：睡觉就是补给站。

![01 不是冲刺，是马拉松](examples/kin-three-points/images/01-marathon.png)

**02 80% 的力气花在揣摩上** —— 奶龙举着放大镜研究悬在半空的「老板眉毛」，真正想做的画架被冷落在角落。

![02 80% 的力气花在揣摩上](examples/kin-three-points/images/02-boss-eyebrow.png)

**03 剪开岗位的围栏** —— 奶龙用写着「AI」的大剪刀剪开「岗位」栅栏，抱着摄像机和翻页动画本迈出去。

![03 剪开岗位的围栏](examples/kin-three-points/images/03-cut-the-fence.png)

**04 AI 是那根支点** —— 小小的奶龙压着「专长」砖块，借「AI」支点撬起比自己大十倍的气球。

![04 AI 是那根支点](examples/kin-three-points/images/04-lever.png)

**05 两个轮子一起转** —— 前轮是工具（输入），后轮是文章纸卷（输出），奶龙蹬着两个轮子一起转才能往前走。

![05 两个轮子一起转](examples/kin-three-points/images/05-two-wheels.png)

**06 自己挖的护城河** —— 奶龙把一页页笔记铲进河道，分享出去的知识反而挖宽了「个人IP」的护城河。

![06 自己挖的护城河](examples/kin-three-points/images/06-moat.png)

## License

[MIT](LICENSE) © Kin
