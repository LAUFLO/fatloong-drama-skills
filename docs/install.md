# 安装说明

## 目录要求

每个 skill 的目录名必须与 `SKILL.md` 里的 `name` 完全一致：

| 目录名 | name |
|---|---|
| `fatloong-screenwriting-master` | `fatloong-screenwriting-master` |
| `fatloong-director-master` | `fatloong-director-master` |
| `fatloong-prompt-master` | `fatloong-prompt-master` |

改目录名会导致 Agent 拒绝加载。

---

## OpenCode

### 全局安装

```bash
mkdir -p ~/.config/opencode/skills
cp -r skills/* ~/.config/opencode/skills/
```

Windows PowerShell：

```powershell
New-Item -ItemType Directory -Path "$env:USERPROFILE\.config\opencode\skills" -Force
Copy-Item "skills\*" "$env:USERPROFILE\.config\opencode\skills\" -Recurse -Force
```

### 项目级安装

放到项目根目录的 `.opencode/skills/` 下：

```bash
mkdir -p .opencode/skills
cp -r skills/* .opencode/skills/
```

### 验证

重启会话后，提问一个触发词即可：

```
帮我拆分镜
```

如果导演 skill 被加载，会先问剧本类型或直接进入导演定调。

---

## Claude Code

```bash
mkdir -p ~/.claude/skills
cp -r skills/* ~/.claude/skills/
```

或项目级：

```bash
mkdir -p .claude/skills
cp -r skills/* .claude/skills/
```

---

## BeefTV

BeefTV 的 Skills 使用同一套 `SKILL.md` 格式。

两种方式：

1. 在 BeefTV 的 Skills 市场里导入
2. 把 `skills/` 下的目录复制到本地 skills 路径

注意：BeefTV Agent 有自主创作倾向，使用提示词 skill 时建议明确要求“逐字使用给定文本，不得改写”。

---

## 常见问题

### skill 不出现

1. 检查 `SKILL.md` 是否全大写
2. 检查 frontmatter 是否有 `name` 和 `description`
3. 检查目录名是否与 `name` 一致
4. 检查是否放在正确的 skills 路径下

### 三个 skill 同时触发

描述里都带“大师”“分镜”等词，可能同时命中。

解决：用更明确的开头，比如“用编剧大师……”“用导演大师……”。

### 只想用其中一套

可以只复制需要的目录，三套之间没有代码依赖。

但导演大师的输出是提示词大师的输入，缺了导演这棒，提示词大师需要你手动提供分镜表。

---

## 更新

```bash
cd fatloong-skills
git pull
cp -r skills/* ~/.config/opencode/skills/
```

覆盖前建议先备份自己改过的文件。

---

## 卸载

删除对应目录即可：

```bash
rm -rf ~/.config/opencode/skills/fatloong-screenwriting-master
rm -rf ~/.config/opencode/skills/fatloong-director-master
rm -rf ~/.config/opencode/skills/fatloong-prompt-master
```
