# Git Bash 速查：复制粘贴 / 卡住怎么办 / 中文乱码

> 适用：Windows 上的 Git Bash（默认终端是 mintty）。
> 配置日期：2026-10-30，本机已写好 `~/.minttyrc` 和 `~/.inputrc`。

---

## 一、为什么 Ctrl+V 在 Git Bash 里没用

Git Bash 不是 Windows 的 CMD/PowerShell，它是一个**终端模拟器（mintty）**。
终端里的 Ctrl+C 是"中断当前进程"的信号（不是复制），所以 Ctrl+V 也不会是粘贴。
这是设计如此，不是坏了。

---

## 二、四种粘贴办法（按好用程度排）

| 方式 | 操作 | 说明 |
|---|---|---|
| **右键粘贴** ★推荐 | 在窗口里点右键 → Paste | mintty 最稳的方式，永远有效 |
| **Ctrl+Shift+V** | 键盘 | 已通过 `~/.minttyrc` 开启（新开窗口生效） |
| **Shift+Insert** | 键盘 | 终端通用快捷键，不用配置 |
| 中键粘贴 | 按鼠标滚轮键 | Linux 习惯，Windows 上少用 |

**复制**：鼠标选中文字即自动复制（不用按 Ctrl+C）；或 Ctrl+Shift+C。

> 配置文件位置：`C:\Users\yigong\.minttyrc`
> 手动开启路径：Git Bash 标题栏右键 → Options → Keyboard → 勾 "Ctrl+Shift+letter shortcuts"

---

## 三、多行命令粘贴时被"逐行执行"

表现：粘一段多行命令，结果第一行就跑了，后面几行报错。

原因：粘贴时每行末尾的换行被当成"回车"，一行一行提交。

解决（已配置）：`~/.inputrc` 里写了 `set enable-bracketed-paste on`，
开启**括号粘贴模式**后，多行内容会被当成一个整体，只在你按回车时执行。

临时补救办法：

- 一次只粘一行，粘完按回车；
- 或者先粘到记事本里合并成一行，用 `&&` 或 `;` 连接；
- 或者粘完后**先看清楚再按回车**（终端会先显示出来等你确认）。

---

## 四、最常踩的坑：以为"卡住了"，其实是进了编辑器

Git 有两个地方会自动打开 **Vim 编辑器**，新手 100% 会卡在这里：

### 1. `git commit` 不带 `-m`

```
git commit
```
会直接打开 Vim 让你写提交说明。此时**按什么都没反应、也退不出去**。

正确操作：

```
i            ← 进入编辑模式（左下角出现 -- INSERT --）
（粘贴或手写提交说明）
Esc          ← 退出编辑模式
:wq          ← 冒号 + wq，回车，保存并退出
```

**不想用 Vim，就永远别裸敲 git commit，改成：**

```
git commit -m "这里写提交说明"
```

一行搞定，不进编辑器。

### 2. `git log` 或 `git diff` 结果翻页

会进入 less 分页器，底部显示 `:`。

```
q            ← 退出
空格         ← 下一页
```

### 3. 命令输了一半想取消

```
Ctrl + C     ← 放弃当前行，重新回到提示符
```

---

## 五、粘贴代码时的其他坑

1. **行尾多余空格 / 缩进丢失**：先在编辑器里写好，别直接在终端里拼。
2. **中文粘贴变乱码**：已设 `Charset=UTF-8`，基本不会；万一出现，在窗口标题栏右键 → Options → Text → Locale 选 `zh_CN`、Character set 选 `UTF-8`。
3. **粘贴带 `$` 或 `>` 的多行示例**：那些是提示符，不是命令的一部分，只粘命令本身。
4. **粘贴 GitHub 上的 clone 命令**：一行，直接右键 Paste 最稳。

---

## 六、实在不想折腾的话

直接用 **Windows Terminal**（微软商店免费装）：

- 默认就是 Ctrl+Shift+V 粘贴，跟其他软件一致；
- 可以在里面开 Git Bash、PowerShell、CMD 多个标签页；
- 中文显示比 mintty 好。

或者用 **GitHub Desktop**（图形界面，完全不碰命令行也能 clone/看历史）。

---

## 七、现阶段真正用得上的命令

```bash
git clone <仓库地址>      # 把项目下载到本地（粘地址后右键 Paste）
cd <目录名>               # 进入项目
git status                # 看当前状态
git log --oneline         # 看提交历史（q 退出）
git diff                  # 看改了什么（q 退出）
git pull                  # 拉最新代码
```

就这些。commit / push 等你建了 GitHub 账号再说。
