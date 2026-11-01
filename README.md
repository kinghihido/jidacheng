# 集大成者

一个材料系学生的个人档案总台。**轻量集合点：本站不装内容，只做入口。** 纸色底、宋体标题、发丝线分格。

> 2026-10-31 起，最有分量的内容先后独立成站，总台只保留指向它们的外链。
> 现在十二个活动站各自一个仓库、各自迭代，总台不再背着它们的体积；另有 2 个废站（层林尽染重复站、燕园）已归档下线。
>
> 首页排成 **6 + 3 + 2 + 3**：
> - 一排：六个学习站（汉语 / 现代材料 / 材料科学基础 / 量子统计 / 经济专题 / 基础物理实验）
> - 二排：三个并列内容站 —— 层林尽染（朱砂红）/ 学海无涯（苍蓝）/ 雾里楼台（雾绿）
> - 三排：日常打卡、摄影
> - 四排：三个积累站 —— 诗词积累 / 计算机小知识 / 英语学习

## 页面

| 文件 | 板块 | 现在有什么 |
| --- | --- | --- |
| `index.html` | 总台 | 学习站入口（6 个）、三个内容站入口、日常打卡（可直接勾选）与摄影两块、三个积累站入口、**别处**模块（文献连接器 / 全部仓库）、近七天统计 |
| `study.html` | 本科学习 | 六个学习站入口、本学期课表（10 门）、三个待建分区 |
| `photography.html` | 我的摄影 | 上传照片（自动压到长边 1600），相册、删除 |
| `discipline.html` | 日常网站 | 三餐打卡、臂力棒计数、睡眠记录、任务清单 |
| `writing.html` | 创作（迁移页） | 原写作页已迁至独立站「雾里楼台」，此页自动跳转；本机如有旧稿可先导出 |

## 首页结构

```
一排 · 课业   →  六个学习站
二排 · 自留地 →  层林尽染 / 学海无涯 / 雾里楼台   （红 / 蓝 / 绿）
三排 · 日常   →  日常打卡（可直接勾选）/ 我的摄影
```

三排都是 1px 发丝线分格的栅格，靠列数（4 / 3 / 2）区分层级。第二排每张卡顶部有一条 3px 的标识色，就是那一站的主色。

## 站点目录

学习站：

| 站点 | 地址 | 内容 |
| --- | --- | --- |
| 汉语 | https://kinghihido.github.io/hanyu-xuexi/ | 古代汉语、现代汉语课堂讲义 |
| 现代材料 | https://kinghihido.github.io/materials-analysis-learning-site/ | 现代材料分析与原理，19 篇讲稿、522 页图文 |
| 材料科学基础 | https://kinghihido.github.io/materials-science-foundations/ | 415 页课件逐页放映，附 50 题章节自测 |
| 量子统计 | https://kinghihido.github.io/quantum-mechanics-notes/ | 材料中的量子与统计，50 个知识点 |
| 经济专题 | https://kinghihido.github.io/china-economy-study-website/ | 中国经济专题（北大 NSD），七讲整理 |
| 基础物理实验 | https://kinghihido.github.io/physlab-thu-night/ | 周四晚班课程站点：安排、地点、须知、资料 |

内容站（中排三个并列）：

| 站点 | 主色 | 地址 | 内容 |
| --- | --- | --- | --- |
| 层林尽染 | 朱砂红 | https://kinghihido.github.io/wuli-loutai/ | 技术流：AI 工具链、范德华材料转移、前端工程化 |
| 学海无涯 | 苍蓝 | https://kinghihido.github.io/paper-reading/ | 文献精读报告 22 篇、词汇 282 条 |
| 雾里楼台 | 雾绿 | https://kinghihido.github.io/wuliloutai-writing/ | 文集：日记 / 随感 / 长文 |

下排（积累站）：

| 站点 | 主色 | 地址 | 内容 |
| --- | --- | --- | --- |
| 诗词积累 | 紫 | https://kinghihido.github.io/daily-poem/ | 每日一诗 · 抄录与批注 |
| 计算机小知识 | 绿 | https://kinghihido.github.io/cs-weekly/ | 每周一条 · 原理与拾遗 |
| 英语学习 | 棕 | https://kinghihido.github.io/english-daily/ | 每日精读 · 词汇与长难句 |

其他：

| 站点 | 地址 | 内容 |
| --- | --- | --- |
| 文献连接器 | https://github.com/kinghihido/Zotero_Connector | Zotero × WorkBuddy |
| 全部仓库 | https://github.com/kinghihido | GitHub 主页 |

## 视觉

- 一套变量在 `assets/style.css` 的 `:root`：纸色 `--paper`、墨三级 `--ink/-2/-3`、主色 `--accent`、朱砂 `--seal`。所有页面共用，**不要再在页面里写 `<style>` 或私有调色板**。
- `--ink-3` 取 `#5e6563`（在纸色上对比度约 4.9:1，之前的 `#767d79` 只有 3.6:1，不达 AA）。
- 站点标统一为：64×64 视窗、圆角 12、浅色调底 + 单字符/符号、0.5px 发丝描边。新增站点照这个规格做，先去子站看过 DNA，别凭空配色。

## 数据存在哪

照片、打卡、任务存在**浏览器本地** `localStorage`，键名 `jdc.photos` / `jdc.meals`（三餐与睡眠）/ `jdc.tasks`（任务）/ `jdc.fitness`（臂力棒）。

文稿与文献分别由雾里楼台、学海无涯自己管，键前缀分别是 `wuli.` 类与 `lit.`。

- 换设备、换浏览器、清缓存，数据都不会跟过去。
- 照片压缩后存本地，容量上限约 5 MB，放十几张就到顶。
- AI 接口的 Key 存在本机（`jdc.ai.key`），不会上传。
- 两个自转站与本站同在 `kinghihido.github.io` 域下，**localStorage 同源互通**。学海无涯首次进入时会读一次旧键 `jdc.papers` / `jdc.vocab` 做迁移，并把篇数同步回本站首页。

### 一个旧的假统计

首页原本读 `jdc.lit` 来显示「待读 / 在读 / 已读」，而文献页写的是 `jdc.papers` —— 全站没有任何地方往 `jdc.lit` 写过，所以那三个数**常年恒为 0**。现在首页改成直接取学海无涯的 `papers-index.json`（两站同在一个域名下，没有跨域问题），显示真实篇数。

## 还没做的

- 课程笔记、实验与作业、复习清单三块目前只有结构，规则待定。
- 照片的相册分组还没做。
- 稳定后可考虑给六个学习站和雾里楼台做真正的 favicon / OG 图。
- AI 生成阅读报告：之前 README 描述过「上传 PDF → 调 AI 生成七维度报告」，但 `literature.html` 里其实从没实现过这段，只有列表和词汇展示。这个功能的所有笔记已随模块迁到学海无涯，骨架留在那边待实现，分析框架在它的 `skills/paper-reader/SKILL.md`。

## 本地预览

直接双击 `index.html` 即可（页面互相用相对路径跳转）。改完提交推送，GitHub Pages 会自动更新。

## 素材说明

`assets/photos/weiminghu.jpg` 是占位用的示例照片（未名湖·博雅塔），正式使用时换成自己拍的。
