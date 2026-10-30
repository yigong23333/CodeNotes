# 项目清单：Obsidian 方向

> 已核对过仓库地址，可直接点开。读一个就在 `notes/` 里写一篇。

## 一、中文资源总目录（先看这个）

- **PKM-er/awesome-obsidian-zh** —— https://github.com/PKM-er/awesome-obsidian-zh
  中文插件、主题、资源的分类清单，更新很勤（最近更新 2026-10）。找中文插件从这里进，比在 Obsidian 里一个个搜快得多。

## 二、必装级插件（用了就回不去）

| 插件 | 仓库 | 一句话 |
|---|---|---|
| Git | https://github.com/Vinzent03/obsidian-git | 把 vault 自动备份到 Git 仓库，**最适合我们现在的需求** |
| Dataview | https://github.com/blacksmithgu/obsidian-dataview | 把笔记当数据库查，写一行语句自动出表格 |
| Templater | https://github.com/SilentVoid13/Templater | 高级模板引擎，支持 JS 脚本，比自带模板强太多 |
| Tasks | https://github.com/obsidian-tasks-group/obsidian-tasks | 跨笔记汇总待办 |
| Kanban | https://github.com/mgmeyers/obsidian-kanban | Markdown 看板 |
| Excalidraw | https://github.com/zsviczian/obsidian-excalidraw-plugin | 手绘图 / 思维导图 |
| Advanced Tables | https://github.com/tgrosinger/advanced-tables-obsidian | 表格编辑增强 |
| Calendar | https://github.com/liamcain/obsidian-calendar-plugin | 日历打开每日笔记 |

建议顺序：**先 Git**（解决备份），**再 Templater**（我们沉淀库已经在用模板，能直接升级），**然后 Dataview**（沉淀库卡片多了以后，用它自动出索引表，比手工维护链接表强）。

## 三、学插件开发（想看懂代码怎么写的）

- **官方示例插件** obsidianmd/obsidian-sample-plugin —— https://github.com/obsidianmd/obsidian-sample-plugin
  这是官方给的模板，用 TypeScript 写的，演示了最基础的 API（加个按钮、加个命令、加个设置页）。代码量小，是入门第一站。
- **开发者文档（中文）** —— https://raistlind.github.io/obsidian-dev-docs-zh/zh/plugins/getting-started/build-a-plugin.html
  中文版，跟着做一遍就能把插件跑起来。
- 需要 Node.js 环境，`git clone` 后 `npm install` 再 `npm run dev`。

## 四、主题 / CSS

- PKM-er/Blue-Topaz_Obsidian-css —— https://github.com/PKM-er/Blue-Topaz_Obsidian-css（国产主题，中文排版友好）
- 主题本质是 CSS，想学可以直接看别人的 CSS 片段，比插件代码简单得多，适合当第一个"读懂"的目标。

## 五、下一步可以延伸的方向

- 无人机/低空：PX4、ArduPilot、Betaflight、MAVSDK（Python 控制无人机）
- 机械/CAD：FreeCAD（开源 CAD，支持 Python 二次开发）
- Python 实战：找带中文讲解的教程仓库

（这些等 Obsidian 这块读顺了再开新的清单文件。）
