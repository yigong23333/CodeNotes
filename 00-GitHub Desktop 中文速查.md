# GitHub Desktop 中文速查（界面全对照）

> 本机 GitHub Desktop 3.6.8，界面是英文，但日常用的就这几个词。
> 按位置记，不用背英文。

---

## 一、顶部三大区（打开软件第一眼）

```
┌──────────────────────────────────────────────────────┐
│  File   Edit   View   Repository   Branch   Help      │  ← 菜单栏
│ [Current repository ▾] [Current branch ▾] [Fetch origin] │
└──────────────────────────────────────────────────────┘
```

| 英文 | 意思 | 干嘛用 |
|---|---|---|
| **Current repository** | 当前仓库 | 点开切换/添加仓库（Add → Add existing repository 选本地文件夹） |
| **Current branch** | 当前分支 | 日常用 main，不用管 |
| **Fetch origin** | 抓取远程 | 相当于「检查云端有没有新东西」，点一下没坏处 |

---

## 二、日常记录笔记：只需三个动作

以「写完一篇源码笔记」为例：

1. **左边栏 Changes（更改）**——你改过/新增的文件全列在这里。
   黄色点 = 改过，绿色加号 = 新文件。
2. **左下角写说明**：第一行 Summary（必填，一句话说明这次改了什么，**可以用中文**），
   第二行 Description（可选，不填也行）。
3. **点蓝色大按钮 `Commit to main`**——提交到本地。按钮上会显示有几个文件待提交。

提交完左上角会出现：

4. **`Push origin`**——推到 GitHub。有数字（如 `Push origin 1`）说明还有内容没推上去，点一下就同步了。**看到 Push origin 就点它，养成习惯**。

> 一句话总结：**Changes 里看改了什么 → 左下角写一句中文说明 → Commit to main → Push origin**。

---

## 三、克隆别人的项目

菜单 **File → Clone repository**（文件 → 克隆仓库），三个标签：

| 标签 | 用途 |
|---|---|
| GitHub.com | 列出你账号下的仓库（拉自己的） |
| **URL** | 粘贴别人的仓库地址（常用！） |
| 本地 | 已克隆过的 |

选 URL → 粘贴 `https://github.com/用户名/仓库名` → 下面 **Local path** 改成
`D:\Repos\仓库名` → 点 **Clone**。完事后项目就在 D:\Repos 里了。

---

## 四、其他常见英文对照（出现时查这里）

| 英文 | 意思 |
|---|---|
| History | 历史（每次提交记录，点开能看每次改了什么） |
| Pull origin | 拉取云端更新到本地（云端有新内容时出现） |
| Stashed changes | 暂存的改动（新手不用管） |
| Untracked files | 新增的、还没被 Git 管理的文件 |
| Discard changes | 丢弃改动（**慎点**，改的东西就没了） |
| Fetch origin | 从云端检查更新（不改动本地） |
| Publish repository | 发布仓库（把本地新仓库传到 GitHub，私有仓库要勾 Keep this code private） |
| Create a new repository | 新建仓库 |
| Branch → Create branch | 新建分支（读源码想大改时再用，日常不碰） |
| Repository → Show in Explorer | 在文件管理器打开这个仓库 |
| Update from origin / Pull | 更新本地代码 |

---

## 五、日常节奏（背下来就够）

```
写笔记 → 左下角写中文说明 → Commit to main → Push origin
读项目 → File → Clone repository → URL → D:\Repos → Clone
```

其他按钮暂时一律不用碰。Discard changes 那个是删除改动，别乱点。

---

## 六、关于汉化

GitHub Desktop 官方没有中文。社区有汉化包（如 lgw88/CN-GitHub-Desktop，支持 3.6.10），
需要：先把 GitHub Desktop 升级到对应版本，再跑汉化脚本。2026-10-30 当晚网络不稳没装成，
想要中文界面时找管家说一声再装。**注意：软件每次自动升级后汉化可能失效，要重跑一次。**

---

## 七、Git 常用概念中英对照（读文章会遇到）

| 英文 | 中文 |
|---|---|
| repository / repo | 仓库 |
| commit | 提交（一次存档） |
| push | 推送（上传到 GitHub） |
| pull / fetch | 拉取 / 抓取（从 GitHub 下载） |
| clone | 克隆（完整复制一个项目） |
| branch | 分支 |
| merge | 合并 |
| conflict | 冲突（两边改了同一处） |
| remote / origin | 远程 / 默认远程名 |
| stage | 暂存（把改动放进待提交清单） |
