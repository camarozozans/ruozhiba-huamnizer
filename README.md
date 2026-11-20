# ruozhiba - 弱智吧语料回复人性化skill

用弱智吧语料做的「回复人味过滤」skill

## 背景

百度弱智吧那套问答里的技术，比它看起来的值钱。这个Skill教会模型在日常对话中用更加拟人的回复；更重要的是它学习了近10年贴吧老哥的语料，赋予了模型“用魔法打败魔法”的能力

| 文件 | 条数 | 回复中位长度 | 来源 |
|---|---|---|---|
| `ruozhiba-train.json` | 9408 | 19 字 | `https://github.com/riyuexingchennnn/ruozhiba` |
| `ruozhiba-val.json` | 800 | 20 字 | 同上 |
| `ruozhiba_qa.json` | 1496 | 89 字 | `https://market.aliyun.com/detail/cmodxFHHI7G81SGVD61P.html` |

## 版本分支

| | 版本 | frontmatter | 行为 |
|---|---|---|---|
| `ruozhiba-auto` | 1.1.0 | 无特殊开关 | 出现在模型目录里，每条回复前自动过一遍，每5秒自动检查，适合日常聊天 |
| `ruozhiba-manual` | 2.0.0 | `disable-model-invocation: true` | 模型看不见，需要在发起请求时附带，适合改稿 |

## 目录

```
ruozhiba-auto/
  SKILL.md
  references/
    intensity.md        定档细则、关系松紧、升降档判据
    mechanisms.md       十机制带语料原例
    failure-modes.md    演砸的十种死法
    corpus-evidence.md  语料统计与样本分级
ruozhiba-manual/        （同上，SKILL.md 不同）
```

