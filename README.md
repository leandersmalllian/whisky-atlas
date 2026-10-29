# 威士忌世界地图 / Whisky Atlas

一个以 **WhiskyNotes（whiskynotes.be）** 的独立品鉴为参考的中文威士忌视觉档案。

## 打开方式（优先用单文件版）

**推荐双击项目根目录的 `whisky-atlas.html`。** 这是单文件版：CSS、JS、世界地图和全部 163 张图片都已内嵌，不依赖 `assets/` 路径，适合文件预览器、聊天窗口和离线分发。

源码版在当前目录：`index.html` + `assets/`，适合继续编辑。如果预览器不读取同级资源，图片就会显示不出来——这不是图片丢失，改用单文件版即可。

重新生成单文件版：

```bash
python3 build_standalone.py
# 输出到 ../whisky-atlas.html
```

也可以在当前目录运行源码版：

```bash
python3 -m http.server 8907
# http://127.0.0.1:8907
```

## 收录范围

- **163 款**威士忌：以主流在售核心款、常见独立装瓶与 WhiskyNotes 近年高分酒款为主。
- **名称中英对照**：卡片与详情页以中文名为主，保留英文原名。
- **六步工艺配图**：发芽、糖化、发酵、蒸馏、熟成、调配/装瓶各有一张内嵌 SVG 线稿，移动端两列排列。
- **88 家**蒸馏所 / 装瓶中心，覆盖 **18 个国家与地区**。
- **年度榜单**：2026 / 2025 / 2024 三个年份的 WhiskyNotes 90+ 威士忌记录，按评论发布年份归档。
- **273 条** WhiskyNotes 92+ 历史分数记录（97–92），包含最老、最贵与最高 ABV 的站点记录。
- **8 类**桶型：波本、雪莉、波特、朗姆、葡萄酒、水楢、新橡木、STR。
- 价格为中国大陆常见零售/电商参考区间（人民币，2026），不是实时报价；稀有酒为拍卖/估价。
- 图片：163 张产品图，来自 WhiskyNotes 评论、品牌官网与零售公开产品页；按酒款名称逐款核对，部分为旧版/不同容量包装。仅用于识别与评论。
- 原 “The English Chapter 7” 已停产且没有可靠产品图，已替换为同厂在售的 “The English Original”。

> “所有市面上的威士忌”在逻辑上不可能穷举：全球有数千个 SKU，每年还有数百个新装瓶。本项目追求的是**可读的覆盖**，不是库存数据库。页面中的“数据边界”已明确说明这一点。

## 站点章节如何进入项目

| WhiskyNotes 章节 | 在本项目中的呈现 |
|---|---|
| Whisky reviews | 阅读区、163 款酒档案、风味坐标 |
| By distillery | 世界地图 → 国家 → 产区 → 蒸馏所 |
| 年度榜单 / All-time | 2026 / 2025 / 2024 年度 90+、273 条 92+ 全时名单、97 分专席 |
| Links | 阅读区底部“站点信任的链接” |
| About | 方法论、独立声明、数据边界 |
| Sherry casks | 桶型区的“雪莉桶真相” |
| Best of 2024 / 2025 | 年度选择、性价比、市场观察 |

## 目录

```
index.html            页面结构
styles.css            视觉与响应式
app.js                数据渲染、地图、图表、筛选、弹窗
assets/data.json      原始结构化数据
assets/data.js        页面使用的数据
assets/hall.js        273 条 92+ 记录
assets/annual.js      2026 / 2025 / 2024 年度 90+ 记录
assets/vendor/        d3 / topojson / 10m 世界地图
assets/img/           163 张产品图（WebP）
```

## 主要来源

- https://www.whiskynotes.be/
- https://www.whiskynotes.be/whisky-reviews-by-distillery/
- https://www.whiskynotes.be/top-10/
- https://www.whiskynotes.be/links/
- https://www.whiskynotes.be/about-whiskynotes/
- https://www.whiskynotes.be/2017/whisky-news/sherry-casks-in-the-whisky-industry/
- https://www.whiskynotes.be/2025/whisky-news/best-wishes-best-whisky-of-2024/
- https://www.whiskynotes.be/2026/whisky-news/best-whisky-of-2025-overview/

## 声明

非官方项目，与 WhiskyNotes 无隶属关系。图片版权归 WhiskyNotes / 各品牌与零售商所有，仅用于识别。奖项只记录可核实的公开信息，未列出不等于未获奖。请理性饮酒。
