# 预包装食品标签全文审核

用于 Codex 的食品标签审核技能包，依据 GB 7718—2025 全文及所附广告营销与包装法规汇编，输出条款依据、问题清单和可供设计修改的建议。

## 安装

将本仓库下载或克隆到 `~/.codex/skills/review-food-label-gb7718`，确保该目录下直接包含 `SKILL.md`。

```bash
git clone https://github.com/s822631635-dotcom/review-food-label-gb7718.git ~/.codex/skills/review-food-label-gb7718
```

## 使用

在 Codex 中调用 `$review-food-label-gb7718`，提供包装各面、标签文字及产品资料，并说明生产或进口时间、目标上市时间和审核模式。

示例：使用 $review-food-label-gb7718 审核这份食品包装，区分当前合规和新版预审，并给出修改清单。

## 文件说明

- `SKILL.md`：审核流程、证据边界和输出要求。
- `agents/openai.yaml`：技能显示名称与默认提示。
- `references/standard-full.md`：GB 7718—2025 提取文本。
- `references/checklist.md`：逐项审核清单。
- `references/official-sources.md`：官方来源导航。
- `references/compilation-guide.md`：法规汇编使用导航。
- 其余参考文件：法规汇编 PDF、HTML、主体及附录转录。

## 适用边界

GB 7718—2025 于 2027 年 3 月 16 日实施。实施前依新版检查应标为“新版预审”；正式审核须核验适用时点的官方标准、过渡安排和配套规定。附件中的日期及效力说明不等于本次实时核验。技能输出不能替代配方、实测、检测、资质或完整法律判断。

参考资料的来源与校验说明见 `references/compilation-guide.md`。本仓库未另行授予第三方参考资料的再许可。
