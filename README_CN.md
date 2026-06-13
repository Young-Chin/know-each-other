# Know Each Other

> 一个让 Claude 真正了解*你这个人*的 Skill —— 不只是你想要什么。

大多数 AI 每次对话都从零开始。**Know Each Other** 为你建立一份持久的心理画像，让 Claude 能够适应你的思维方式、沟通偏好和决策模式，并在所有项目中持续生效。

---

## 工作原理

```
首次运行                      后续每次对话
─────────────────────        ──────────────────────────────
  深度对谈                    观察 → 建议 → 确认
       ↓
  心理学翻译                      📝 值得沉淀？
       ↓                          USER_PROFILE.md
  生成两个文件                       + 新观察到的模式
                                 SOUL.md
  ~/.claude/SOUL.md                 + 新的协作约定
  ~/.claude/USER_PROFILE.md
                                你确认 → 写入
```

### 两个核心文件

| 文件 | 内容 |
|------|------|
| `~/.claude/SOUL.md` | Agent 的性格配置：语气、反馈风格、主动程度、表达习惯 |
| `~/.claude/USER_PROFILE.md` | 你的心理画像：认知功能、决策方式、工作模式 |

两个文件全局共享 —— 在所有项目中通用。

---

## 三个阶段

**① 初始化** *（首次运行）*

自然流动的两段对谈 —— 不是问卷：

- **塑造你的 Agent** —— 你想要什么样的协作伙伴？
- **你是谁** —— 围绕 MBTI 四个维度展开的对话（E/I · N/S · T/F · J/P）

对谈结束后，Claude 完成*心理学翻译*：你的话 → 荣格认知功能（Ne、Ni、Te、Ti、Fe、Fi、Se、Si）→ 一份描述你*如何思考*的画像，而不只是你喜欢什么。

**② 更新建议** *（每次有价值的对话后）*

```
📝 本次对话有些内容值得沉淀到档案，供你确认：

USER_PROFILE.md → 已观察到的模式：
  + 「反复确认实现细节再推进 → Si 信号，倾向于依赖可靠流程」

SOUL.md → 特别约定：
  + 「代码默认不加注释」

确认后写入，或告诉我调整措辞。
```

**③ 静默更新** *（明确且持续的信号）*

一致出现的行为模式会被悄悄写入。涉及 MBTI 类型或主导认知功能的大调整，始终需要你确认。

---

## 触发方式

说出以下任意一句即可激活：

- *"你对我了解不够"*
- *"记住我的工作方式"*
- *"我想让你有一个稳定的性格"*
- *"你对我了解多少？"*
- *"帮我初始化档案"*

---

## 安装

```bash
# 复制到 Claude skills 目录
cp -r . ~/.claude/skills/know-each-other/
```

Skill 会自动出现在可用列表中。

### 会话启动时自动加载档案

初始化完成后，skill 会自动在 `~/.claude/settings.json` 中配置 **SessionStart hook**，让 `SOUL.md` 和 `USER_PROFILE.md` 的**完整内容**在每次会话启动时直接注入上下文——不是文件引用，是真实内容。

```json
"hooks": {
  "SessionStart": [{
    "hooks": [{
      "type": "command",
      "command": "... ; [ -f ~/.claude/SOUL.md ] && cat ~/.claude/SOUL.md; [ -f ~/.claude/USER_PROFILE.md ] && cat ~/.claude/USER_PROFILE.md; true"
    }]
  }]
}
```

从下一次会话的第一条消息起，Claude 就已经是你配置好的那个协作伙伴。

---

## 心理学框架

Skill 背后使用的理论体系：

- **MBTI 四维度** —— 初始化对谈的对话骨架
- **荣格八维认知功能** —— 真正的分析层（Ne/Ni/Te/Ti/Fe/Fi/Se/Si）
- **行为信号解读** —— 你*怎么说*和你*说什么*同样重要

完整参考资料 → [`references/personality-frameworks.md`](references/personality-frameworks.md)

---

*A [Kiro](https://kiro.ai) skill — built for Claude.*
