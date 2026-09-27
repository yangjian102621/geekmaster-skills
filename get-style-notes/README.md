# get-style-notes

把任意网页链接、文章或长文本，整理成一篇「得到 GET 笔记」风格的结构化中文阅读笔记。

**Turn any URL, article, or long text into a structured Chinese reading note, inspired by the note style of Dedao's "GET Notes" (得到 GET 笔记).**

> ⚠️ 本项目与得到 App / GET 笔记无任何隶属关系，仅致敬并借鉴其广受欢迎的笔记范式。
> Not affiliated with Dedao. "GET 笔记" is a trademark of its respective owner; this project only references the note-taking style.

## 为什么不是又一个「总结工具」

市面上大多数摘要技能的逻辑是"把长文压短"。这个技能的逻辑是**转述**：像一位编辑读完文章后讲给你听。输出质量由三条硬性红线保证：

1. **观点必须带原文证据** —— 每条核心观点后面必须跟原文的数据、案例或引证，只有论点没有论据的条目直接不合格；
2. **金句一字不改** —— 摘录区只收原文原话，逐字保真，改写过的句子不许进金句区；
3. **拿不准的不写** —— 任何原文里不存在的数字、人名、观点一律不出现；遇到抓不到正文的付费墙 / 登录墙文章，宁可如实告知并停下，也不用残缺内容硬写。

## 笔记结构

每篇笔记固定为五个部分：

| 部分 | 内容 |
|---|---|
| 一句话总结 | ≤ 60 字，直接给结论 |
| 核心观点 | 3-5 条，每条观点短语 + 2-4 句转述 + 原文证据 |
| 金句摘录 | 1-3 句原文原话，一字不改 |
| 概念卡片 | 原文关键术语的大白话解释 |
| 值得记住 | 1-3 条由原文自然引出的启发或行动 |

## 示例

同一套结构，覆盖演讲趋势、商业案例、经济学理论三类内容：

- [罗振宇「时间的朋友 2016」跨年演讲](./examples/luozhenyu.md)
- [刘润《18 年后，那位司机又给我上了一节 MBA 课》](./examples/liurun.md)
- [薛兆丰《火车票价还不够高》](./examples/xuezhaofeng.md)

## 安装

```bash
# 方式一：skills CLI（推荐）
npx skills add yangjian102621/geekmaster-skills@get-style-notes

# 方式二：手动复制到工具的技能目录（ZCode / Claude Code 为 ~/.agents/skills/）
git clone https://github.com/yangjian102621/geekmaster-skills.git
cp -r geekmaster-skills/get-style-notes ~/.agents/skills/
```

不同工具的技能目录可能不同，请按所用工具的文档放置。

## 使用

安装后，在支持 Skills 的 AI 助手里用自然语言触发：

- 「帮我记个笔记：https://example.com/article」
- 「把这篇文章总结成 GET 笔记风格：<链接>」
- 「读一下这篇 https://… 做成结构化笔记」

也可以直接丢本地文件路径（Markdown / TXT / DOCX / PDF）。

## 工作原理

技能本体只有一个 [SKILL.md](./SKILL.md)：定义输入获取链路（defuddle / 环境内置抓取 / Jina Reader / curl 依次降级）、固定笔记模板和三条验收红线。不依赖任何外部 API 或私有服务，任何能读网页、写文件的 AI 助手都能跑。

## License

[MIT](../LICENSE)
