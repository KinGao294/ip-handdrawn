# 输入一整篇文章，自动识别高光片段，生成生动形象的 IP 配图。

> **Nailong-image** — Feed in a whole article; it spots the highlight passages and draws vivid hand-drawn 16:9 illustrations starring your own IP. 奶龙 (Nailong) is just the built-in sample.

**推荐搭配：[Codex](#codex) · [Cursor](#cursor) · [Grok Bot](#grok-bot)**（Claude Code 等支持 Agent Skills 的工具也能用）

它会先通读全文，挑出最值得画的「认知锚点」——核心判断、转折、闭环、对比，给出配图策略（shot list），再逐张生成 16:9 横版手绘配图：纯白背景、黑色手绘线稿、大量留白，**你的 IP 是画面里唯一的彩色主角**，亲自完成核心动作，再配几句红 / 蓝手写批注。

**主角可以换成任何你喜欢的 IP / 吉祥物。** 仓库自带的「奶龙」只是一个示例 IP，也是没选 IP 时的默认主角。

## 效果示例：奶龙 ×《AI 时代我最近想得最多的三个点》

原文：[article.md](examples/kin-three-points/article.md) ｜ 配图策略：[shotlist.md](examples/kin-three-points/shotlist.md) ｜ 提示词：[prompts/](examples/kin-three-points/prompts/) ｜ 奶龙档案：[ips/nailong.md](ips/nailong.md)

每张图上方引用的是它对应的原文段落（来自 [article.md](examples/kin-three-points/article.md)，按 [shotlist.md](examples/kin-three-points/shotlist.md) 对应），下面一句说明画了什么。

### 01 不是冲刺，是马拉松

> 所以我希望在接下来的人生里，真的能做到少熬夜、多运动，养成良好的作息习惯，然后和 AI 打一场持久战。 因为它确实不是一场百米冲刺，而是未来 5 年、10 年、20 年的一场马拉松。

🎨 奶龙拆掉百米跑道的起跑器挂上吊床，在 5 年 / 10 年 / 20 年的里程牌旁穿着跑鞋打盹——睡觉就是补给站。

![01 不是冲刺，是马拉松](examples/kin-three-points/images/01-marathon.png)

### 02 80% 的力气花在揣摩上

> 为什么要做这个决定？因为我后来发现，在一份工作里，100% 的时间里可能只有 20% 是真正想做的那件事，剩下 80% 都是非常琐碎、又很费力的工作。举两个例子：准备 ppt 汇报时，一个措辞你需要反复揣摩几十轮；开会时老板一个眼神停顿两秒，你就要当面揣摩他是认可还是不满——这种揣摩心思的工作，是真正消耗心力的。

🎨 奶龙举着巨型放大镜研究悬在半空的「老板眉毛」，身后是「第37版」ppt 草稿堆，真正想做的画架被冷落在角落。

![02 80% 的力气花在揣摩上](examples/kin-three-points/images/02-boss-eyebrow.png)

### 03 剪开岗位的围栏

> 但这几年，AI 来啦，我认为 AI 时代，我们的职业选择是比以往更宽的。 以前你做这个岗位，就只能做这个岗位；现在不是了。比如我以前完全不会做视频，AI 来了之后我开始会做视频剪辑甚至动效设计了。职业的边界被 AI 打开了，也更适合超级个体去闯。

🎨 奶龙用刀刃写着「AI」的大剪刀剪开「岗位」栅栏，抱着摄像机和翻页动画本迈向开阔的外面。

![03 剪开岗位的围栏](examples/kin-three-points/images/03-cut-the-fence.png)

### 04 AI 是那根支点

> AI 把杠杆放下了，每个人都有机会把自己的专长放大。这是一个更适合超级个体的时代，我们值得认真地试一试。

🎨 小小的奶龙压着「专长」砖块，借「AI」支点撬起比自己大十倍的气球。

![04 AI 是那根支点](examples/kin-three-points/images/04-lever.png)

### 05 两个轮子一起转

> 一年下来我发现，研究 AI 工具和做自媒体内容 IP，是一件非常互补的事。 研究给我输入，输出给我放大——输入没有输出，沉淀不下来；输出没有输入，很快就会枯竭。 两个轮子一起转，飞轮才转得起来。

🎨 奶龙骑着自制自行车：前轮是工具（输入），后轮是文章纸卷（输出），两个轮子一起转车才往前走。

![05 两个轮子一起转](examples/kin-three-points/images/05-two-wheels.png)

### 06 自己挖的护城河

> 当然，我们 SpacexAI 社区目前有 30 多个中文微信社群，如果你有一些好的想法，不只是想在线下和自己渠道分享，也想通过直播、文章或视频的方式做线上分享，也欢迎来找我聊。 这方面我非常开放——AI 时代需要有更多人把自己脑子里的专业知识拿出来分享，既能帮到别人，也能一点点把"个人影响力"^_^护城河建起来。

🎨 奶龙把一页页笔记铲进河道，分享出去的知识反而挖宽了「个人IP」沙堡的护城河。

![06 自己挖的护城河](examples/kin-three-points/images/06-moat.png)

> 📌 这 6 张成图里的奶龙形象稳定一致，**同时也是奶龙的补充角色参考图**，可以和 [`assets/character/nailong/`](assets/character/nailong/) 一起作为 `-i` 参考传入。

## 换成你自己的 IP

第一次使用时，skill 会自动引导你：

1. **看效果**：先给你看上面的奶龙案例，说明它能做什么。
2. **问你要不要换 IP**：不换就继续用奶龙。
3. **建立你的 IP**：
   - 上传一张你的 IP 图片，**或者**让它帮你生成一张定妆图（正面全身、纯白背景、无道具、无文字）；
   - 保存到 `assets/character/<ip-slug>/ref-front.png`；
   - 按 [`ips/_template.md`](ips/_template.md) 写一份角色档案 `ips/<ip-slug>.md`：名字、外形、**招牌色**（全图唯一的角色色彩）、性格、动作风格、禁忌；
   - 在 [`config/active-ip.md`](config/active-ip.md) 里把它设为当前 IP——从此它就是你这份 skill 的默认主角。
4. **开始配图**：把你的文字给它，先出 shot list，再逐张生成。

也可以手动完成上面第 3 步；随时说「换 IP」就能重新走一遍。奶龙档案 [`ips/nailong.md`](ips/nailong.md) 一直保留，可随时切回。

## 安装

本仓库本身就是一个 skill 目录（入口是 [SKILL.md](SKILL.md)）。建议 `git clone` 成可写目录，因为换 IP 时 skill 会往里写入你的参考图、档案和配置。**最推荐在 Codex、Cursor、Grok Bot 里使用。**

### Codex

```bash
git clone https://github.com/KinGao294/Nailong-image.git ~/.codex/skills/nailong-image
```

然后在 Codex 里直接说「给这篇文章配图」。Codex 自带图像生成，最适合逐张出图（见下方「用法」里的命令行写法）。

### Cursor

```bash
# 全局（所有项目可用）
git clone https://github.com/KinGao294/Nailong-image.git ~/.cursor/skills/nailong-image
# 或仅当前项目
git clone https://github.com/KinGao294/Nailong-image.git .cursor/skills/nailong-image
```

Cursor 会自动加载 `SKILL.md`；在 Agent 里说「给这篇文章配图」，或输入 `/nailong-image` 调用。需要生图时，可让 Agent 在终端里调用 Codex CLI（见「用法」）。

### Grok Bot

把仓库链接发给 Grok Bot，并说：

> 把 https://github.com/KinGao294/Nailong-image clone 到你的电脑里，把 SKILL.md 保存成我的私有 skill，参考图和案例都用这个目录里的。

保存后在桌面端输入框里打 `/` 选择这个 skill 即可使用；如果 `/` 菜单里没有，到 Settings → Plugins → Yours 里为当前 Bot 启用它。

### 其他工具（Claude Code 等）

Claude Code：`git clone https://github.com/KinGao294/Nailong-image.git ~/.claude/skills/nailong-image`。其他支持 Agent Skills 的工具同理 clone 到对应 skills 目录；不支持 skills 的，把 `SKILL.md` 作为规则 / 系统提示加载，并保证它能读写本目录下的 `config/`、`ips/`、`assets/`。

## 用法

装好后直接把文章丢给助手，说「给这篇文章配图」「帮这段话画张图」「先出个 shot list」即可——它会自己挑出高光段落来画。

需要手动生图时，以 Codex CLI 为例——**一次调用只出一张图**，先附 IP 参考图，再从 stdin 传提示词（`-i` 可接多个文件，所以提示词用 `-` 读 stdin）：

```bash
codex exec --skip-git-repo-check -i assets/character/nailong/ref-front-clean.png - < prompt.txt
# 换成你的 IP：
codex exec --skip-git-repo-check -i assets/character/<ip-slug>/ref-front.png - < prompt.txt
```

提示词结构可参考 [`examples/kin-three-points/prompts/`](examples/kin-three-points/prompts/)，把奶龙描述换成你 IP 档案里的锁定句和招牌色。

## 风格规则速览

- **16:9 横版**，**纯白背景**，黑色手绘线稿，大量留白。
- **IP 的招牌色是全图唯一的角色色彩**，其他物件一律纯黑线稿、不填色。
- **IP 必须是核心动作主体**，不能只站在旁边当装饰。
- 只加**少量红 / 蓝中文手写批注**，宁少勿错。
- 禁止 PPT / 信息图感，禁止左上角类型标题、水印、签名。
- 每张图只讲一个核心结构；每篇文章重新发明隐喻，不复刻旧图。
- 参考图只锁定 IP 形象，不照抄场景和动作；同一篇文章 IP 前后一致。

完整工作流（shot list → 单张生成 → QA → 保存）见 [SKILL.md](SKILL.md)。

## 目录结构

```text
SKILL.md                         # Skill 本体（含首次使用引导）
config/active-ip.md              # 当前激活的 IP（默认 nailong）
ips/_template.md                 # IP 档案模板
ips/nailong.md                   # 示例 IP：奶龙
assets/character/nailong/        # 奶龙参考图（默认 ref-front-clean.png）
assets/character/<ip-slug>/      # 你自己的 IP 参考图（引导时创建）
examples/kin-three-points/       # 奶龙完整案例：原文 + shot list + 成图 + 提示词
LICENSE                          # MIT
```

## License

[MIT](LICENSE) © Kin
