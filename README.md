# 红楼人物海报提示词

依据《红楼梦》原文、判词和脂批，为单个人物创作有性格、有叙事的中文生图提示词。默认采用疏朗工笔、低饱和矿物色与竖版 4:5 构图。

## 能做什么

- 支持金陵十二钗，以及晴雯、香菱、袭人等人物。
- 先核对文学依据，再把人物性格与命运意象转化为姿态、空间和画面关系。
- 区分正文事实、脂批解读、续书情节与视觉演绎。
- 默认输出画面主题、原文依据、完整中文提示词和题字建议；说“只要提示词”即可简化输出。
- 用户只要提示词时，不会自动生成图片。

## 安装

下载本仓库，将包含 `SKILL.md` 的整个目录命名为 `honglou-portrait-prompt`，放进所用智能体的技能目录。Codex 可放在 `~/.codex/skills/honglou-portrait-prompt/`。保留 `agents/` 与 `references/`，不要只复制入口文件。

## 使用示例

```text
请使用 $honglou-portrait-prompt，为林黛玉创作一份工笔人物海报生图提示词。
```

```text
使用 $honglou-portrait-prompt，画史湘云醉眠芍药裀。竖版 4:5，保留轻快明朗的性格，只要提示词。
```

```text
使用 $honglou-portrait-prompt，为贾探春设计海船远行主题的海报提示词，构图疏朗，不生成画内文字。
```

没有指定人物时，技能会先询问人物；“金陵十二钗主题”默认指系列主题，不会擅自改成十二人同框。

## 资料准备

本仓库包含技能与方法参考，不包含整部小说语料库。

- 有本地资料时，向智能体提供实际语料目录；推荐目录含 `sources/` 与 `foreshadowing/`，详见[语料检索指南](references/corpus-guide.md)。
- 没有本地资料时，可联网检索、打开原文核对，并注明实际版本及来源。
- 没有可核对的资料时，技能会说明限制，不伪造原文引文。

## 文件说明

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 技能入口、创作流程和完成自查 |
| [agents/openai.yaml](agents/openai.yaml) | 技能显示名称与默认调用提示 |
| [references/corpus-guide.md](references/corpus-guide.md) | 语料定位、版本边界及人物入口 |
| [references/visual-style.md](references/visual-style.md) | 留白、构图、线描设色与文字规范 |
| [references/tanchun-example.md](references/tanchun-example.md) | 探春的取证与空间转译完整示例 |

公开内容已使用通用路径；请按自己的资料位置检索，不需要复现作者的本机目录。
