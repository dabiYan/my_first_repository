太棒了！你已经掌握了 Git 的基础操作，下面我们继续学习：

------

## ✅ 一、修改文件并提交（更新版本）

### ✍️ 假设你已经有一个 Git 仓库，并修改了某个文件，比如 `readme.txt`：

你可以使用 VS Code、记事本、Sublime 等编辑器对文件进行修改。

然后在命令行中按以下步骤操作：

```bash
git status                    # 查看有哪些文件修改了
git add .                     # 添加所有修改（也可以单独 add 某个文件）
git commit -m "更新了 readme 内容"  # 提交修改并写上说明
```

> 💡 建议写清楚每次修改的内容，方便日后回溯。

------

## 🧾 二、查看提交历史记录（版本历史）

你可以使用以下命令：

### 1. **基本查看历史版本**

```bash
git log
```

输出示例：

```
commit 91e1b2aa7a1c3b5e5cb9a0dbd437bafcb89a74f6
Author: yan dabi <example@email.com>
Date:   Tue Jun 18 14:32:12 2024 +0800

    更新了 readme 内容

commit b72f6d3ccaa43cfe47c8cd522e4c93046cc25e1a
Author: yan dabi <example@email.com>
Date:   Tue Jun 17 22:14:11 2024 +0800

    第一次提交：添加 readme.txt
```

------

### 2. **一行一条记录（简洁模式）**

```bash
git log --oneline
```

输出示例：

```
91e1b2a 更新了 readme 内容
b72f6d3 第一次提交：添加 readme.txt
```

------

### 3. **查看具体某次提交内容**

```bash
git show 提交ID
```

示例：

```bash
git show 91e1b2a
```

你会看到本次提交改了哪些文件、每一行增加或删除了什么。

------

## 🕰️ 三、版本回退（可选）

如果你提交后发现问题，也可以回到上一个版本：

```bash
git checkout 提交ID
```

例如：

```bash
git checkout b72f6d3
```

> ⚠️ 注意：你这样会进入“游离状态（detached HEAD）”，一般用于查看，不建议直接在这时修改文件。

------

## 🛟 四、回到当前主分支

如果你用 `checkout` 进入了历史版本，可以这样回到主分支：

```bash
git switch main
```

或：

```bash
git checkout main
```

------

## 📌 总结流程图（推荐背下来）

```text
修改文件 → git status → git add . → git commit -m "说明" → git push（可选）
           ↓
     git log / git show 查看历史
```

------

如果你喜欢图形化查看历史，也可以使用：

- `gitk`（在终端中输入）
- VS Code 左边栏的 Git 图标
- GitHub 上的 “Commits” 页面查看远程记录

------

