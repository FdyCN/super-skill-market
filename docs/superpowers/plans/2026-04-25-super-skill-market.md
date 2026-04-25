# Super Skill Market 实施计划

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 搭建一个以 README 为核心的 Claude Code Skills 精选集市，收录人物蒸馏和脑洞大开两类 skill，支持 PR 和 Issue 两种贡献方式。

**Architecture:** 纯静态 GitHub 仓库，无构建步骤。README.md 是主产品，以 Markdown 表格维护 skill 目录；CONTRIBUTING.md 说明贡献规则；顶部免责声明明确技术立场。

**Tech Stack:** Markdown、Git、GitHub

---

### Task 1：创建 README.md 主文件

**Files:**
- Create: `README.md`

- [ ] **Step 1：写 README.md**

```markdown
# Super Skill Market 🧠

> 精选 Claude Code Skills 集市 —— 人物蒸馏 & 脑洞大开

**免责声明**：本仓库为纯技术分享，收录任何人物的思维框架 skill 均与政治立场、意识形态无关，仅供学习与探索之用。

---

## 人物蒸馏

以历史或当代人物的思维框架为蓝本，帮助你从不同视角处理技术问题。

### 技术

| Skill | 简介 | 仓库 |
|-------|------|------|
| （欢迎提交） | — | — |

### 经济 & 投资

| Skill | 简介 | 仓库 |
|-------|------|------|
| （欢迎提交） | — | — |

### 哲学 & 智慧

| Skill | 简介 | 仓库 |
|-------|------|------|
| （欢迎提交） | — | — |

### 商业 & 管理

| Skill | 简介 | 仓库 |
|-------|------|------|
| （欢迎提交） | — | — |

---

## 脑洞大开

出乎意料的非常规视角，让你以完全不同的方式看待技术问题。

| Skill | 简介 | 仓库 |
|-------|------|------|
| （欢迎提交） | — | — |

---

## 如何贡献

**方式一：提 Pull Request**

1. Fork 本仓库
2. 在 README.md 对应分类的表格末尾加一行
3. 确保链接指向原始仓库（非 fork）
4. 提 PR，标题格式：`add: skill-name`

**方式二：提 Issue 提名**

在 [Issues](../../issues) 中按如下格式提名，维护者会录入：

```
Skill 名：xxx
分类：人物蒸馏 / 脑洞大开（子类：技术 / 经济&投资 / 哲学&智慧 / 商业&管理）
一句话简介：xxx
原始仓库链接：https://github.com/xxx/yyy
```

---

> 优先收录中文 skill，欢迎推荐！
```

- [ ] **Step 2：确认文件内容渲染正确**

在终端预览结构：
```bash
cat README.md
```
预期：两大分类（人物蒸馏、脑洞大开）、四个人物子分类均存在，免责声明在顶部。

- [ ] **Step 3：提交**

```bash
git add README.md
git commit -m "feat: add README with skill directory structure"
```

---

### Task 2：创建 CONTRIBUTING.md 贡献指南

**Files:**
- Create: `CONTRIBUTING.md`

- [ ] **Step 1：写 CONTRIBUTING.md**

```markdown
# 贡献指南

感谢你愿意为 Super Skill Market 贡献！

## 收录标准

- 必须是 Claude Code `.md` 格式的 skill（可通过 `Skill` 工具调用）
- 必须有公开可访问的原始仓库链接
- 简介须一句话说清 skill 的视角和用途
- 本仓库不存储 skill 文件本体，只维护索引

## 分类说明

| 分类 | 适合哪些人物或主题 |
|------|------------------|
| 技术 | 科学家、工程师、发明家（费曼、图灵、冯·诺依曼等） |
| 经济 & 投资 | 经济学家、投资人（巴菲特、芒格、凯恩斯等） |
| 哲学 & 智慧 | 哲学家、思想家、古典智慧（苏格拉底、王阳明、老子等） |
| 商业 & 管理 | 企业家、管理者（乔布斯、稻盛和夫、曾国藩等） |
| 脑洞大开 | 出乎意料的非常规视角，不限主题 |

## PR 格式

表格每行格式：

```markdown
| `skill-name` | 一句话简介 | [作者/仓库名](https://github.com/...) |
```

PR 标题格式：`add: skill-name`

## Issue 提名格式

```
Skill 名：xxx
分类：人物蒸馏 / 脑洞大开（子类：技术 / 经济&投资 / 哲学&智慧 / 商业&管理）
一句话简介：xxx
原始仓库链接：https://github.com/xxx/yyy
```

## 免责声明

收录任何人物的思维框架 skill 均为技术探索，与政治立场、意识形态无关。
```

- [ ] **Step 2：确认文件存在**

```bash
cat CONTRIBUTING.md
```
预期：包含收录标准、分类说明、PR 和 Issue 两种格式。

- [ ] **Step 3：提交**

```bash
git add CONTRIBUTING.md
git commit -m "docs: add CONTRIBUTING guide with PR and Issue submission formats"
```

---

### Task 3：最终验收

- [ ] **Step 1：检查仓库结构**

```bash
ls -la
```
预期输出包含：
```
README.md
CONTRIBUTING.md
docs/
```

- [ ] **Step 2：确认 README 两大分类和四个子分类均存在**

```bash
grep -n "##" README.md
```
预期：
```
## 人物蒸馏
### 技术
### 经济 & 投资
### 哲学 & 智慧
### 商业 & 管理
## 脑洞大开
## 如何贡献
```

- [ ] **Step 3：确认免责声明存在**

```bash
grep -n "免责声明" README.md CONTRIBUTING.md
```
预期：两个文件中各出现一次。

- [ ] **Step 4：查看提交历史**

```bash
git log --oneline
```
预期至少 3 条提交记录。
