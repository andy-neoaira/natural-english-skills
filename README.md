# Natural English Skills

把中文意图变成自然的英文表达——而不是逐字翻译。

一组面向中文用户的 Agent Skills，用于把中文内容重新组织成**英语读者自然会读到的表达**。

目标不是把中文逐句翻译成英文，而是：

> 保留作者真正想表达的意思，同时让结果像原本就是用英语写出来的。

目前包含两个 Skill：

- `write-natural-english-post`：把中文内容改写成自然英文帖子
- `write-natural-english-reply`：结合英文原帖，把中文回复意图改写成自然英文回复

---

## 技能列表

### `write-natural-english-post`

用于把中文帖子、想法或观点重新写成自然、可直接发布的英文内容。

适合：

- X / Twitter
- Reddit
- Hacker News / 论坛
- 社群
- 技术社区
- 个人动态
- 产品或开发经历分享

输入：

```text
 最近一直在思考一个问题，用户真正的是需求什么？是一把螺丝刀还是一把瑞士军刀？ 开发者经常想把自己的产品构建成完美的，万能的，恨不得能解决任何问题。但用户更多时候可能只想解决眼下的一个问题，当用户
 需要一把螺丝刀时就给他一把螺丝刀，当用户又需要一把罐头起子时就再给他一把罐头起子，而不是先给他一把瑞士军刀后跟他说，请接受它，相信我，这里的起子你以后会用到的。
```

输出：

```text
英文帖子

Lately I've been thinking about what users actually need. A screwdriver, or a Swiss Army knife? Developers often want to build their product into something perfect and all-purpose, wishing it
could solve any problem. But more often than not, users just want to solve the one problem in front of them. When someone needs a screwdriver, give them a screwdriver. When they need a can
opener, give them a can opener. Don't hand them a Swiss Army knife and say, "Take it, trust me—you'll use this opener someday."

中文回译

最近我一直在想，用户真正需要的是什么。一把螺丝刀，还是一把瑞士军刀？开发者常常想把产品做成完美、全能的东西，恨不得它能解决所有问题。但更多时候，用户只想解决眼前的那一个问题。有人需要螺丝刀时，
就给他螺丝刀；需要罐头起子时，就给他罐头起子。不要递给他一把瑞士军刀然后说："拿着吧，相信我——这个起子你以后会用到的。"

英语读者视角

- 理解与感受：读者会读出这是一段关于产品设计的反思——对"过度构建"的温和批评，主张一次只解决一个问题。语气克制、有思考感，带一点自嘲式幽默（末句引用的那句"trust me"是点睛）。
- 自然度：句子短而直接，螺丝刀／瑞士军刀／罐头起子的比喻在英语里完全自洽，不需要额外解释。"more often than not" 保留了原文"更多时候"的保留态度。
- 翻译／AI 痕迹：整体干净，没有模板化开场或收尾。两句"give them… give them…"的排比源自原文本身的刻意对仗，不显得机械。唯一的书面感来自"wishing it could solve any problem"，但它贴切地表达了"恨不
  得"，无需改动。

```

Skill 不会逐句翻译，而是按照英语读者习惯重新组织表达，同时保留原本的经历、观点和语气。

---

### `write-natural-english-reply`

用于回复已有的英文帖子、评论或消息。

Skill 会同时理解：

1. 对方原本说了什么
2. 你真正想表达什么

然后根据上下文生成自然英文，而不是孤立翻译中文。

输入：

```text
 You got a product idea.
 You invest $100K, then discover 10 similar products already exist.
 What do you do now?

 最少省去你验证市场的时间，首先你的产品是有市场的，那么剩下的就做些微创新，努力做分销
```

输出：

```text
 英文回复
 You basically skipped market validation. Ten similar products means there's real demand. So differentiate a little and go all in on distribution.

 中文翻译
 你基本等于跳过了市场验证这一步。有十个类似产品，说明需求是真的存在。剩下的就是稍微做出点差异化，然后把精力全放在分销上。

 母语者视角
 - 理解：母语者会读出"这是好事不是坏事"的潜台词——竞争激烈恰好证明有市场，接下来只需差异化+猛攻分销。
 - 感受：务实、乐观、干脆，像创业圈里的过来人在给建议，不啰嗦。
 - 自然度：很自然；go all in on distribution 是创业者圈子的常用说法，比逐字翻译"work hard on distribution"更地道，也更有力度。
 - 翻译/AI 痕迹：没有明显痕迹。
```

而不是机械地把中文完整翻译成一句正式英文。

适合：

- X / Twitter 回复
- Reddit 评论
- 技术论坛
- Discord / Slack / 社群
- 普通英文聊天
- 英文评论区互动

---

## 该用哪个 Skill？

| 场景                                     | Skill                         |
| ---------------------------------------- | ----------------------------- |
| 我要把自己的中文内容写成英文帖子         | `write-natural-english-post`  |
| 我要回复一个已有的英文帖子               | `write-natural-english-reply` |
| 有英文上下文，需要根据上下文表达中文想法 | `write-natural-english-reply` |
| 没有需要回复的原帖，只是想表达自己的观点 | `write-natural-english-post`  |

最简单的判断方法：

> **有英文原帖 → reply**
> **没有英文原帖 → post**

---

## 安装

### 方式一：从 Releases 下载

从 GitHub Releases 下载对应 Skill：

```text
write-natural-english-post.zip
write-natural-english-reply.zip
```

解压后会得到：

```text
write-natural-english-post/
└── SKILL.md
```

或者：

```text
write-natural-english-reply/
└── SKILL.md
```

然后把整个 Skill 目录放进你的 Agent Skills 目录。

常见位置例如：

```text
~/.agents/skills/
```

最终结构：

```text
~/.agents/skills/
├── write-natural-english-post/
│   └── SKILL.md
└── write-natural-english-reply/
    └── SKILL.md
```

不同 Agent 对 Skill 的目录、发现方式和加载规则可能不同，请同时参考你所使用 Agent 的文档。

---

### 方式二：克隆仓库

```bash
git clone https://github.com/andy-neoaira/natural-english-skills.git
```

然后复制需要的 Skill：

```bash
cp -R natural-english-skills/write-natural-english-post ~/.agents/skills/
cp -R natural-english-skills/write-natural-english-reply ~/.agents/skills/
```

---

## 使用方式

安装完成后，不需要使用固定 Prompt 模板。

直接描述你的需求即可。

### 写帖子

例如：

```text
把下面这段中文改成适合发到 X 的自然英文：

最近重新开始折腾 Linux 了。
忙活了一晚上，最后其实只是换了个主题。
不过还挺开心的。
```

也可以简单说：

```text
把这段写成英语母语者会自然发出来的英文帖子。
```

---

### 写回复

提供原帖和你的中文回复意图：

```text
原帖：

What editor do you use every day?

我想回复：

还是 Neovim。已经形成肌肉记忆了，而且我喜欢自己控制配置。
```

也可以直接说：

```text
帮我把这个回复改成自然英文，不要翻译腔。
```

Skill 会根据英文原帖理解上下文，而不是只翻译最后一句中文。

---

## 设计理念

### 自然英文，而不是逐句翻译

中文和英文组织信息的方式不同。

Skill 可以：

- 调整语序
- 拆句或合句
- 删除没有实际作用的连接词
- 使用更自然的英语搭配
- 根据上下文省略已经明确的信息

但不会为了“英语更漂亮”而改变作者真正表达的意思。

---

### 保留作者的语气

Skill 不会默认把用户改写成：

- 营销文案
- 励志演讲
- LinkedIn 风格长文
- AI 式总结
- 夸张的网络人格

例如：

```text
我感觉这个工具还不错，但暂时不会用在正式项目里。
```

不会被增强成：

```text
This incredible tool has completely changed the way I work...
```

原文中的：

- 不确定程度
- 情绪强度
- 第一人称判断
- 自嘲
- 谨慎
- 批评
- 技术细节

都会尽量保留。

---

### 不编造上下文

Skill 不应该自行添加用户没有提供的：

- 经历
- 数据
- 结果
- 事实
- 产品评价
- 推荐
- 立场
- 行动号召

自然表达不意味着制造内容。

---

### 减少翻译腔和 AI 腔

Skill 会重点检查：

- 中文语序直接搬到英文
- 不自然但语法正确的搭配
- 过度正式的连接词
- 无意义的开场白
- 三段式排比
- 过度对称的句型
- 营销式总结
- 自动升华主题
- 不必要的 hashtag / emoji
- 过多破折号和感叹号
- 把一句简单回复扩写成完整文章

目标不是“骗过 AI detector”。

目标只是让文字本身更自然。

---

## 输出格式

默认情况下，Skill 可以同时提供：

```text
英文

<最终英文>

中文回译

<最终英文实际表达出来的中文含义>

读者视角

<英语读者可能如何理解这段内容>
```

中文回译的目的不是再次翻译原始中文，而是帮助用户确认：

> 最终英文实际上表达了什么。

如果只需要可以直接复制的英文，可以明确告诉 Agent：

```text
只要英文。
```

或者：

```text
Only give me the final English version.
```

---

## Skill 目录结构

每个 Skill 都是独立、可复制的目录：

```text
natural-english-skills/
├── README.md
├── LICENSE
│
├── write-natural-english-post/
│   └── SKILL.md
│
└── write-natural-english-reply/
    └── SKILL.md
```

每个 `SKILL.md` 使用 YAML frontmatter 描述 Skill：

```yaml
---
name: write-natural-english-post
description: ...
---
```

Skill 本身保持独立，因此可以只安装其中一个，而不需要安装整个仓库。

---

## 为什么做这个项目？

普通翻译工具解决的是：

```text
中文 → 正确英文
```

这个项目更关注：

```text
中文作者真正想表达的意思
          ↓
理解语境和语气
          ↓
重新按照英语表达习惯组织
          ↓
自然英文
```

尤其适合已经能够阅读一些英文，但在主动表达时容易出现：

- 中文式英语
- 翻译腔
- 太正式
- AI 腔
- 不知道英语里实际会怎么说

这些问题的中文用户。

---

## 许可证

MIT 许可证。

你可以自由使用、修改和再分发这些 Skills。
