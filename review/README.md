# 审查分册清单

- 库版本：v2.1.1 ｜ 源库 sha256：`f88abeb35e857f62058f847bc0d524f1ae72581da9a227cf719efa1522db9542`
- 每册的 sha256 与字符数见 `mirror/meta.json` 的 `files` 表（册内自指会形成循环，因此指纹统一记在 meta.json）。
- 分册是同一份库的不同排版，不是新事实源，可由 `tools/build_mirror.py` 整体重建。

| 分册 | 内容 | 覆盖 | 规模 |
|---|---|---|---|
| `review/L1_character_1.md` | 人物（第 1 册，共 7 册） | 实体 75 个 | 28488 字符 |
| `review/L1_character_2.md` | 人物（第 2 册，共 7 册） | 实体 75 个 | 24087 字符 |
| `review/L1_character_3.md` | 人物（第 3 册，共 7 册） | 实体 75 个 | 28703 字符 |
| `review/L1_character_4.md` | 人物（第 4 册，共 7 册） | 实体 75 个 | 26641 字符 |
| `review/L1_character_5.md` | 人物（第 5 册，共 7 册） | 实体 75 个 | 29647 字符 |
| `review/L1_character_6.md` | 人物（第 6 册，共 7 册） | 实体 75 个 | 29526 字符 |
| `review/L1_character_7.md` | 人物（第 7 册，共 7 册） | 实体 75 个 | 5338 字符 |
| `review/L1_location_1.md` | 地点（第 1 册，共 2 册） | 实体 43 个 | 29513 字符 |
| `review/L1_location_2.md` | 地点（第 2 册，共 2 册） | 实体 43 个 | 28953 字符 |
| `review/L1_world_rule.md` | 世界规则 | 实体 26 个 | 22018 字符 |
| `review/L1_group.md` | 群体 | 实体 23 个 | 22645 字符 |
| `review/L1_event.md` | 事件 | 实体 20 个 | 26715 字符 |
| `review/L1_item.md` | 物品 | 实体 6 个 | 5647 字符 |
| `review/L1_race.md` | 种族 | 实体 6 个 | 7244 字符 |
| `review/L1_era_history_1.md` | 历史时代（第 1 册，共 2 册） | 时代分页 37 个 | 29191 字符 |
| `review/L1_era_history_2.md` | 历史时代（第 2 册，共 2 册） | 时代分页 37 个 | 11010 字符 |
| `review/L1_era_mainline_1.md` | 主线时代（第 1 册，共 4 册） | 时代分页 87 个 | 29513 字符 |
| `review/L1_era_mainline_2.md` | 主线时代（第 2 册，共 4 册） | 时代分页 87 个 | 29850 字符 |
| `review/L1_era_mainline_3.md` | 主线时代（第 3 册，共 4 册） | 时代分页 87 个 | 29538 字符 |
| `review/L1_era_mainline_4.md` | 主线时代（第 4 册，共 4 册） | 时代分页 87 个 | 14070 字符 |
| `review/L1_era_afterstory_1.md` | 后日谈时代（第 1 册，共 3 册） | 时代分页 110 个 | 29642 字符 |
| `review/L1_era_afterstory_2.md` | 后日谈时代（第 2 册，共 3 册） | 时代分页 110 个 | 29248 字符 |
| `review/L1_era_afterstory_3.md` | 后日谈时代（第 3 册，共 3 册） | 时代分页 110 个 | 29964 字符 |
| `review/L1_facts_1.md` | facts 断言全集 第1册 | 1865 条 facts | 27221 字符 |
| `review/L1_facts_2.md` | facts 断言全集 第2册 | 1865 条 facts | 27996 字符 |
| `review/L1_facts_3.md` | facts 断言全集 第3册 | 1865 条 facts | 29749 字符 |
| `review/L1_facts_4.md` | facts 断言全集 第4册 | 1865 条 facts | 29900 字符 |
| `review/L1_facts_5.md` | facts 断言全集 第5册 | 1865 条 facts | 29756 字符 |
| `review/L1_facts_6.md` | facts 断言全集 第6册 | 1865 条 facts | 27335 字符 |
| `review/L1_relations.md` | 关系表 | 240 条关系 | 31524 字符 |
| `review/L1_timeline.md` | 时间线 | 86 个时间点 | 7682 字符 |
| `review/L2_全量基线.md` | 全量基线（L0+实体+关系+时间线） | 全库 | 355106 字符 |

## 回传建议格式

```markdown
## 建议 N
- 目标：实体 id / 关系 id / 时间点 id
- 类型：事实矛盾｜时代错位｜关系缺失｜命名不一致｜出处缺失｜正文污染｜其他
- 位置：哪一册、哪一段 / 哪条 fact_id
- 现状：（引用库内原文，≤100 字）
- 建议：（改成什么 / 补什么 / 删什么）
- 依据：小说第 X 章 / 图鉴条目 X / 库内自相矛盾之处
- 置信度：高｜中｜低（推测）
```
