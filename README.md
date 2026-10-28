# 集大成者

一个材料系学生的个人档案总台。五个入口，一套视觉：纸色底、宋体标题、发丝线分格。

## 页面

| 文件 | 板块 | 现在有什么 |
| --- | --- | --- |
| `index.html` | 总台 | 五个模块的入口、四个统计数字、近七天打卡格 |
| `writing.html` | 我的创作 | 写作台（标题 / 类型 / 正文），保存、改稿、删除 |
| `photography.html` | 我的摄影 | 上传照片（自动压到长边 1600），相册、删除 |
| `study.html` | 本科学习 | 四个学习站入口（汉语 / 现代材料 / 量子统计 / 经济专题）、本学期课表、三个待建分区 |
| `literature.html` | 学海无涯 | PDF 上传 → AI 生成中文阅读报告（概述 / 引用 / 原理 / 借鉴 / 理论 / 词汇表），手动添加、编辑、筛选 |
| `discipline.html` | 日常网站 | 五项打卡、近七天表格、本周完成度与连续天数 |

## 数据存在哪

所有内容（文稿、照片、文献、打卡）保存在**浏览器本地** `localStorage`，键名 `jdc.writings` / `jdc.photos` / `jdc.papers` / `jdc.vocab` / `jdc.habits`。

- 换设备、换浏览器、清缓存，数据都不会跟过去。
- 照片压缩后存本地，容量上限约 5 MB，放十几张就到顶。
- AI 接口的 Key 存在本机（`jdc.ai.key`），不会上传。
- 想跨设备同步，下一步要接后端或把内容存进仓库（可以再商量）。

## 学习站

| 站点 | 地址 | 内容 |
| --- | --- | --- |
| 汉语 | https://kinghihido.github.io/hanyu-xuexi/ | 古代汉语、现代汉语课堂讲义 |
| 现代材料 | https://kinghihido.github.io/materials-analysis-learning-site/ | 现代材料分析与原理，19 篇讲稿、522 页图文 |
| 量子统计 | https://kinghihido.github.io/quantum-mechanics-notes/ | 材料中的量子与统计，50 个知识点 |
| 经济专题 | https://kinghihido.github.io/china-economy-study-website/ | 中国经济专题（北大 NSD），六讲整理 |

## 还没做的

- 课程笔记、实验与作业、复习清单三块目前只有结构，规则待定。
- 照片的相册分组、创作的长文导出，都还没做。
- 文献报告的 Markdown 渲染、词汇表导出为 Anki 卡片，可以考虑加。

## AI 阅读报告

「学海无涯」页面支持上传 PDF，自动提取文字并调用 AI 生成中文阅读报告。报告包含七个维度：概述、原文引用、原理总结、可借鉴之处、相关理论、通用词汇、专业词汇。

### 配置方法

1. 打开 https://kinghihido.github.io/jidacheng/literature.html
2. 点右上角「AI 设置」
3. 填入 API Key 和接口地址

推荐用 **GitHub Models**（免费）：

| 设置项 | 推荐值 |
| --- | --- |
| 接口地址 | `https://models.inference.ai.azure.com/chat/completions` |
| API Key | GitHub Personal Access Token（Settings → Developer settings → Personal access tokens → Fine-grained tokens） |
| 模型名 | `gpt-4o-mini` |

也可以用 OpenAI、DeepSeek 等任何兼容 OpenAI 格式的接口。

### 技能定义

阅读报告的分析框架定义在 `skills/paper-reader/SKILL.md`，也可以单独在 Qoder 里调用此技能分析论文。

## 本地预览

直接双击 `index.html` 即可（页面互相用相对路径跳转）。改完提交推送，GitHub Pages 会自动更新。

## 素材说明

`assets/photos/weiminghu.jpg` 是占位用的示例照片（未名湖·博雅塔），正式使用时换成自己拍的。
