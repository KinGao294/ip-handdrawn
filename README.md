# 输入一整篇文章，AI 自动识别高光片段，生成生动形象的 IP 手绘配图

**IP 手绘配图**（ip-handdrawn-illustrations）—— Drop in any article (Chinese or English); AI finds the highlights and draws vivid hand-drawn illustrations starring your own mascot.

**只需要任意一篇文章，中英文都行。**

## 你能得到什么

- **省时间**：不用自己想「这里该配什么图」。AI 读完全文，自己挑出最值得画的段落。
- **更好懂**：抽象的观点，变成一眼就能看懂的画。
- **有记忆点**：你自己的 IP 当主角，读者一看就知道是你。

画风统一：白底、黑色手绘线条、IP 是画里唯一有颜色的角色，再加几句红 / 蓝手写小字。

推荐在 **[Codex](#codex)**、**[Cursor](#cursor)**、**[Grok Bot](#grok-bot)** 里用。

## 三步用起来

1. **装上**：把这个仓库装进你的 AI 助手（见下面的[安装](#安装)）。
2. **丢文章**：把文章发给它，说一句「给这篇文章配图」。中文、英文都可以，一段话也行。
3. **拿图**：它先告诉你打算在哪几段配图、每张画什么；然后一张张画出来发给你。不满意就让它重画。

默认主角是「奶龙」。想换成你自己的 IP，[看这里](#换成你自己的-ip)。

## 看看效果：奶龙 ×《AI 时代我最近想得最多的三个点》

下面 6 张图，都是 AI 从[《AI 时代我最近想得最多的三个点》原文](examples/kin-three-points/article.md)里自己挑出段落画的。每张图上面是对应的原文，下面一句话说明画了什么。

### 01 不是冲刺，是马拉松

> 所以我希望在接下来的人生里，真的能做到少熬夜、多运动，养成良好的作息习惯，然后和 AI 打一场持久战。 因为它确实不是一场百米冲刺，而是未来 5 年、10 年、20 年的一场马拉松。

🎨 奶龙拆掉起跑器，挂上吊床。在 5 年、10 年、20 年的路牌旁穿着跑鞋打盹——睡觉就是补给站。

![01 不是冲刺，是马拉松](examples/kin-three-points/images/01-marathon.png)

### 02 80% 的力气花在揣摩上

> 为什么要做这个决定？因为我后来发现，在一份工作里，100% 的时间里可能只有 20% 是真正想做的那件事，剩下 80% 都是非常琐碎、又很费力的工作。举两个例子：准备 ppt 汇报时，一个措辞你需要反复揣摩几十轮；开会时老板一个眼神停顿两秒，你就要当面揣摩他是认可还是不满——这种揣摩心思的工作，是真正消耗心力的。

🎨 奶龙举着大放大镜，研究半空中的一根「老板眉毛」。身后是第 37 版 PPT，真正想做的画架被冷落在角落。

![02 80% 的力气花在揣摩上](examples/kin-three-points/images/02-boss-eyebrow.png)

### 03 用 AI 剪开岗位的围栏

> 但这几年，AI 来啦，我认为 AI 时代，我们的职业选择是比以往更宽的。 以前你做这个岗位，就只能做这个岗位；现在不是了。比如我以前完全不会做视频，AI 来了之后我开始会做视频剪辑甚至动效设计了。职业的边界被 AI 打开了，也更适合超级个体去闯。

🎨 奶龙拿着写着「AI」的大剪刀，剪开「岗位」栅栏，抱着摄像机走了出去。

![03 用 AI 剪开岗位的围栏](examples/kin-three-points/images/03-cut-the-fence.png)

### 04 AI 是那根支点

> AI 把杠杆放下了，每个人都有机会把自己的专长放大。这是一个更适合超级个体的时代，我们值得认真地试一试。

🎨 小小的奶龙压住「专长」砖块，借「AI」支点，撬起比自己大十倍的气球。

![04 AI 是那根支点](examples/kin-three-points/images/04-lever.png)

### 05 两个轮子一起转

> 一年下来我发现，研究 AI 工具和做自媒体内容 IP，是一件非常互补的事。 研究给我输入，输出给我放大——输入没有输出，沉淀不下来；输出没有输入，很快就会枯竭。 两个轮子一起转，飞轮才转得起来。

🎨 前轮是 AI 工具（输入），后轮是文章纸卷（输出）。奶龙蹬着两个轮子一起转，车才往前走。

![05 两个轮子一起转](examples/kin-three-points/images/05-two-wheels.png)

### 06 分享出去，挖成自己的护城河

> 当然，我们 SpacexAI 社区目前有 30 多个中文微信社群，如果你有一些好的想法，不只是想在线下和自己渠道分享，也想通过直播、文章或视频的方式做线上分享，也欢迎来找我聊。 这方面我非常开放——AI 时代需要有更多人把自己脑子里的专业知识拿出来分享，既能帮到别人，也能一点点把"个人影响力"^_^护城河建起来。

🎨 奶龙把一页页笔记铲进河道。分享得越多，「个人IP」沙堡的护城河就越宽。

![06 分享出去，挖成自己的护城河](examples/kin-three-points/images/06-moat.png)

> 📌 这 6 张图里的奶龙形象前后一致，也可以当作奶龙的补充参考图使用。

## 换成你自己的 IP

奶龙只是示例。你可以换成任何你喜欢的形象：吉祥物、宠物、你自己画的小人都行。

第一次用的时候，AI 会主动问你要不要换。要换的话，它会带你做这几件事：

1. **给它一张你的 IP 图片**。没有现成的？描述一下，让 AI 帮你画一张：正面、全身、白底、不带道具和文字。
2. **介绍一下你的 IP**：叫什么、长什么样、主色是什么、什么性格、平时爱怎么动。AI 会帮你整理成一份角色档案。
3. **设为默认**：之后每次配图，主角都是你的 IP。想切回奶龙，说一声就行。

随时说「换 IP」，可以重新来一遍。

## 安装

建议用 `git clone` 安装（不要只下载 SKILL.md），因为换 IP 时会把你的图片和档案存进这个目录。

### Codex

```bash
git clone https://github.com/KinGao294/ip-handdrawn-illustrations.git ~/.codex/skills/ip-handdrawn-illustrations
```

装好后在 Codex 里说「给这篇文章配图」。Codex 自带画图能力，最省事。

### Cursor

```bash
# 所有项目都能用
git clone https://github.com/KinGao294/ip-handdrawn-illustrations.git ~/.cursor/skills/ip-handdrawn-illustrations
# 或者只给当前项目用
git clone https://github.com/KinGao294/ip-handdrawn-illustrations.git .cursor/skills/ip-handdrawn-illustrations
```

装好后在 Cursor 的 Agent 里说「给这篇文章配图」，或输入 `/ip-handdrawn-illustrations`。

### Grok Bot

把下面这句话发给 Grok Bot：

> 把 https://github.com/KinGao294/ip-handdrawn-illustrations clone 到你的电脑里，把 SKILL.md 保存成我的私有 skill，参考图和案例都用这个目录里的。

保存后，在输入框打 `/` 选它就能用。如果 `/` 里找不到，去 Settings → Plugins → Yours 里为当前 Bot 打开它。

### 其他工具

Claude Code 也能用：`git clone https://github.com/KinGao294/ip-handdrawn-illustrations.git ~/.claude/skills/ip-handdrawn-illustrations`。其他支持 Agent Skills 的工具，clone 到它的 skills 目录即可。

---

## 给想深究的人

### 它具体怎么工作

1. **读全文**：判断文章语言（中文 / 英文），找出最值得画的「高光段落」——核心观点、转折、前后对比、循环、常见坑这类，一看图就能懂的地方。
2. **出配图计划**（shot list）：每张图放在哪段后面、讲什么、IP 在做什么、图里写哪几个字。默认 4–8 张，短文 1–3 张。
3. **一张一张画**：每张只讲一件事，每篇文章都重新想比喻，不套旧图。
4. **检查**：IP 有没有走样、有没有只站在旁边、画面是不是太满、字有没有写错。有问题就重画。
5. **保存**：存到 `assets/<文章名>-illustrations/01-xxx.png`，按顺序编号，不覆盖已有文件。

完整规则见 [SKILL.md](SKILL.md)。

### 画风规则

- 16:9 横版，纯白背景，黑色手绘线稿，大量留白。
- IP 的主色是全图唯一的角色色彩；其他东西一律黑色线条、不上色。
- IP 必须在做画面的核心动作，不能只当装饰。
- 只写少量红 / 蓝手写字，用文章的语言（中文文章写中文，英文文章写英文）。宁少勿错。
- 不要 PPT / 信息图的感觉，不要左上角标题、水印、签名。
- 参考图只用来锁定 IP 长相，不照抄它的姿势和场景。

### 用 Codex 命令行手动出图

一次只出一张。先附 IP 参考图，再从 stdin 传提示词（`-i` 可以接多个文件，所以提示词用 `-` 读 stdin）：

```bash
codex exec --skip-git-repo-check -i assets/character/nailong/ref-front-clean.png - < prompt.txt
# 换成你的 IP：
codex exec --skip-git-repo-check -i assets/character/<ip-slug>/ref-front.png - < prompt.txt
```

提示词写法可以参考 [`examples/kin-three-points/prompts/`](examples/kin-three-points/prompts/)，把奶龙的描述换成你 IP 档案里的内容。案例的配图计划见 [shotlist.md](examples/kin-three-points/shotlist.md)。

### 换 IP 的文件在哪

- [`config/active-ip.md`](config/active-ip.md)：当前用哪个 IP（默认 `nailong`）。
- [`ips/_template.md`](ips/_template.md)：角色档案模板；你的档案存为 `ips/<ip-slug>.md`。
- [`ips/nailong.md`](ips/nailong.md)：示例 IP 奶龙的档案。
- `assets/character/<ip-slug>/ref-front.png`：你的 IP 参考图；奶龙的在 [`assets/character/nailong/`](assets/character/nailong/)。

### 目录结构

```text
SKILL.md                         # Skill 本体（含首次使用引导）
config/active-ip.md              # 当前激活的 IP（默认 nailong）
ips/_template.md                 # IP 档案模板
ips/nailong.md                   # 示例 IP：奶龙
assets/character/nailong/        # 奶龙参考图（默认 ref-front-clean.png）
assets/character/<ip-slug>/      # 你自己的 IP 参考图（引导时创建）
examples/kin-three-points/       # 奶龙完整案例：原文 + 配图计划 + 成图 + 提示词
LICENSE                          # MIT
```

## License

[MIT](LICENSE) © Kin
