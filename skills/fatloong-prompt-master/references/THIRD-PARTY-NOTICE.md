# 第三方来源与许可声明

本技能部分内容改编自开源项目。为遵守许可，在此完整声明。

---

## 一、引入清单

| 本地文件 | 来源 | 许可 | 修改情况 |
|---|---|---|---|
| `references/camera-codec.md` | [MapleShaw/seedance2.0-prompt-skill](https://github.com/MapleShaw/seedance2.0-prompt-skill) 的 `references/camera-codec.md` | MIT | 新增「零、九列表快速映射」一节；其余正文保留原貌 |

## 一b、参考来源（未复制）

| 来源 | 用途 | 许可 |
|---|---|---|
| [zenstory-ai/drama-skills](https://github.com/zenstory-ai/drama-skills) | Seedance 2.0 / 2.5 方言规范、时间戳容器写法的核对参考 | MIT |
| [MapleShaw/seedance2.0-prompt-skill](https://github.com/MapleShaw/seedance2.0-prompt-skill) | 相机四维编码、图片生成规范、实测经验（camera-codec 为直接引入） | MIT |

---

## 二、修改说明

对 `camera-codec.md` 的改动仅限：

1. 在文件开头增加来源声明
2. 新增「零、九列表快速映射」一节，把 fatloong 九列分镜表的景别、角度、备注对接到 Z/Y/X/F 坐标
3. 增加三条使用纪律（双轴运动上限、近景禁旋转、正文不写编码）
4. 在“中英文混合描述效果更好”一句后增加本技能的“统一中文”说明
5. 原文的坐标表、运镜词典、情绪速查表**未作改动**

## 三、未引入的内容

以下内容仅阅读参考，**未复制进本技能**：

- 25 格制作流水线
- 四条生成路径 A/B/C/D
- 六套剪辑公式
- dreamina CLI 集成
- 原仓库的 `projects/` 作品库与 `experiments/` 实测日志

这些内容可通过原仓库获取：
https://github.com/MapleShaw/seedance2.0-prompt-skill

## 四、MIT 许可全文

以下为原项目许可原文，适用于上述引入文件。

```
MIT License

Copyright (c) 2026 Seedance Prompt Skill Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
