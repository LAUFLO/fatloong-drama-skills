# 来源与署名

本仓库包含三套 Agent Skill。其中两套改编自 @山音 的开源项目，一套为原创。

---

## fatloong-screenwriting-master

| 项 | 内容 |
|---|---|
| 原始名称 | 山音超级编剧大师 |
| 原作者 | @山音（Shanyin-ai） |
| 原仓库 | https://github.com/Shanyin-ai/shanyin-screenwriting-master |
| 许可证 | MIT |
| 本版本修改 | 调整目录结构以适配 OpenCode；补充 frontmatter 的 license 字段；修改署名与联动说明 |
| 修改者 | @肥龙 |

## fatloong-director-master

| 项 | 内容 |
|---|---|
| 原始名称 | 山音超级导演大师 |
| 原作者 | @山音（Shanyin-ai） |
| 原仓库 | https://github.com/Shanyin-ai/shanyin-director-master |
| 许可证 | MIT |
| 本版本修改 | 调整目录结构以适配 OpenCode；补充 frontmatter 的 license 字段；修改署名与联动说明 |
| 修改者 | @肥龙 |

## fatloong-prompt-master

| 项 | 内容 |
|---|---|
| 原创作者 | @肥龙 |
| 许可证 | MIT |
| 定位 | 在编剧、导演两棒之后，把九列分镜表翻译成 Seedance 2.0 / 2.5 提示词 |

### 第三方内容

| 来源 | 用途 | 许可 | 处理 |
|---|---|---|---|
| [MapleShaw/seedance2.0-prompt-skill](https://github.com/MapleShaw/seedance2.0-prompt-skill) | 相机四维编码、图片生成规范、实测经验 | MIT | `references/camera-codec.md` 为直接引入并加映射层，其余为参考 |
| [zenstory-ai/drama-skills](https://github.com/zenstory-ai/drama-skills) | Seedance 2.0 / 2.5 方言规范核对 | MIT | 仅参考，未复制 |

完整第三方声明见 `skills/fatloong-prompt-master/references/THIRD-PARTY-NOTICE.md`。

---

## 使用限制说明

MIT 许可证允许自由使用、修改、分发和商业使用。

但原作者的 README 中另有说明：

> 保留版权：使用时需保留原作者「@山音」标识，禁止删除原创作声明
>
> 禁止商用 Skill 本身：本 Skill 文件禁止二次售卖、打包商用或作为付费产品核心组件

本仓库尊重上述要求：

1. 保留 @山音 的署名与仓库链接
2. 不将本仓库的 skill 文件作为付费产品单独售卖
3. 欢迎基于本仓库继续修改，但请保留 `NOTICE.md`

---

## 致谢

- @山音：编剧与导演两套方法论的原作者
- MapleShaw：相机四维编码与 Seedance 实测经验
- zenstory-ai：Seedance 方言规范的公开整理
