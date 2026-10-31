# 肥龙 AI 短片三棒 Skill

> 编剧 → 导演 → 提示词。把一部短片从故事想法，推到可直接生成的提示词。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 这是什么

三套 Agent Skill，各管一段，串起来是一条完整的 AI 短片创作链路。

| 棒次 | Skill | 输入 | 输出 |
|---|---|---|---|
| 第一棒 | 编剧大师 | 故事想法 | 剧本 |
| 第二棒 | 导演大师 | 剧本 | 九列分镜表 |
| 第三棒 | 提示词大师 | 分镜表 + 导演定调 | Seedance 提示词表 |

三棒可以单独用，也可以连着跑。连着跑的好处是：每一棒的产出都是下一棒的明确输入，不会出现“分镜和提示词对不上”。

## 三棒链路

```
故事想法
   ↓  编剧大师：破题 → 梗概 → 人物 → 世界观 → 结构 → 场景 → 写作 → 医生
剧本
   ↓  导演大师：定调 → 节奏 → 微调 → 分镜 → 输出
九列分镜表
   ↓  提示词大师：核对 → 锚定 → 关键帧 → 视频提示词 → 输出
Seedance 提示词表
```

## 三套 Skill

### 1. 肥龙超级编剧大师

覆盖 1–3 分钟概念超短片、5–10 分钟叙事短片、90 分钟长片、多集剧集。

八步工作流：破题、梗概、人物弧光、前史世界观、结构大纲、场景列表、场景写作、剧本医生。

核心铁律：不写心理描写、不写括号暗示、用动作代替解释、台词口语化。

### 2. 肥龙超级导演大师

从剧本出发，完成导演定调、节奏规划、剧本微调、分镜拆解，输出标准九列分镜表。

内置数十种影片类型的导演风格模板库，支持类型交叉组合。分镜表含九列：镜号、时长、摄影角度、景别、画面内容、场景、声音、备注、叙事目的。

### 3. 肥龙超级提示词大师

把分镜表翻译成 Seedance 2.0 / 2.5 的图片与视频提示词。

核心能力：

- 风格、角色、场景三种锚定串，保证跨镜一致性
- 关键帧图片提示词，按“必出 / 可复用 / 可跳过”筛选
- 图生视频提示词，只写变化，不重复图片已有信息
- 生成单元合并，解决分镜 1–2 秒、模型最短 4 秒的冲突
- 崩脸陷阱、篇幅纪律、平台合规自检

支持模型：Seedance 2.0、Seedance 2.5。

---

## 安装

三套 skill 的目录名必须保持原样，否则 Agent 无法识别。

### OpenCode

```bash
git clone https://github.com/<your-name>/fatloong-skills.git
cp -r fatloong-skills/skills/* ~/.config/opencode/skills/
```

Windows：

```powershell
Copy-Item "fatloong-skills\skills\*" "$env:USERPROFILE\.config\opencode\skills\" -Recurse
```

### Claude Code

```bash
cp -r fatloong-skills/skills/* ~/.claude/skills/
```

### BeefTV

在 Skills 中安装，或把 `skills/` 下的目录复制到本地 skills 路径。

---

## 快速开始

装好后，按顺序对话即可：

**第一步，写剧本：**

```
用编剧大师，帮我写一个 75 秒的科幻喜剧短片，主题是“路人甲抢主角”
```

**第二步，拆分镜：**

```
用导演大师，把这个剧本拆成九列分镜表，16:9
```

**第三步，写提示词：**

```
用提示词大师，把分镜表写成 Seedance 2.0 的提示词
```

每一棒都会在关键节点暂停，等你确认后再继续。

---

## 目录结构

```
fatloong-skills/
├── README.md
├── LICENSE
├── NOTICE.md
├── skills/
│   ├── fatloong-screenwriting-master/
│   │   ├── SKILL.md
│   │   └── references/
│   ├── fatloong-director-master/
│   │   ├── SKILL.md
│   │   └── references/
│   └── fatloong-prompt-master/
│       ├── SKILL.md
│       └── references/
└── docs/
    └── install.md
```

---

## 来源与致谢

编剧、导演两套 skill 改编自 **@山音** 的开源项目：

- [Shanyin-ai/shanyin-screenwriting-master](https://github.com/Shanyin-ai/shanyin-screenwriting-master)
- [Shanyin-ai/shanyin-director-master](https://github.com/Shanyin-ai/shanyin-director-master)

提示词 skill 为原创，其中相机四维编码改编自 [MapleShaw/seedance2.0-prompt-skill](https://github.com/MapleShaw/seedance2.0-prompt-skill)，Seedance 方言参考了 [zenstory-ai/drama-skills](https://github.com/zenstory-ai/drama-skills)。

完整署名与修改说明见 [NOTICE.md](NOTICE.md)。

---

## 许可

MIT License。允许自由使用、修改、分发。

请保留原作者署名，不要删除 `NOTICE.md` 中的来源说明。

