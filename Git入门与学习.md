

------


# 🧰 Git 和 GitHub 零基础入门教程

> 本教程适合从来没有用过 Git 和 GitHub 的朋友，一步步教你搭建开发环境、上传代码，并掌握最常用的命令。

---

## 🧠一、什么是 Git 和 GitHub？

| 名称    | 简要说明 |
|---------|----------|
| **Git** | 本地的版本控制工具，能记录文件修改历史，就像“时间机器” |
| **GitHub** | 一个远程代码托管平台，让你把 Git 项目上传到云端，并支持协作开发 |

---

## 🛠️ 二、安装 Git

### 1. 下载并安装 Git

- 打开官网：https://git-scm.com/
- 点击 **Download** 按钮，下载安装程序
- 一路点击“下一步”，保持默认设置即可

### 2. 验证安装

打开终端或命令行输入：

```bash
git --version
~~~

看到如下类似内容说明安装成功：
git version 2.xx.x
```

------

## 👤 三、注册 GitHub 账号

1. 打开 [https://github.com](https://github.com/)
2. 点击右上角 **Sign up**
3. 填写用户名、邮箱和密码，完成注册
4. 登录成功后可以访问你的主页：https://github.com/你的用户名

------

## 📁 四、本地创建第一个 Git 项目

### 1. 创建文件夹并进入

```bash
mkdir my-first-git
cd my-first-git
```

### 2. 初始化仓库

```bash
git init
```

### 3. 添加一个文件

```bash
echo "Hello, Git!" > readme.txt
```

### 4. 查看当前状态

```bash
git status
```

### 5. 添加到暂存区

```bash
git add readme.txt
```

### 6. 提交到仓库

```bash
git commit -m "第一次提交：添加了 readme.txt"
```

------

## ☁️ 五、将项目上传到 GitHub

### 1. 创建远程仓库

- 登录 GitHub
- 点击右上角 ➕ > **New repository**
- 仓库名填入：`my-first-git`
- 点击 “Create repository”

### 2. 将本地项目关联到 GitHub

```bash
git remote add origin https://github.com/你的用户名/my-first-git.git
git branch -M main
git push -u origin main
```

> ⚠️ 注意：第一次 push 可能需要登录 GitHub 账户或使用 Token，可以使用 GitHub Desktop 简化这个过程。

------

## 🔁 六、日常操作流程（记住这三步）

每次改完文件后，执行这三步即可：

```bash
git add .
git commit -m "你修改了什么"
git push
```

------

## 🖼️ 七、图形化工具推荐（不写命令也能用）

| 工具           | 官网                                                         | 简介                |
| -------------- | ------------------------------------------------------------ | ------------------- |
| GitHub Desktop | [https://desktop.github.com](https://desktop.github.com/)    | 官方图形客户端      |
| Sourcetree     | [https://www.sourcetreeapp.com](https://www.sourcetreeapp.com/) | 专业 Git 可视化工具 |

------

## 📚 八、可以继续学习的内容

- Git 分支（branch）和合并（merge）
- GitHub 的 Pull Request 协作流程
- 使用 `.gitignore` 忽略不必要的文件
- VS Code 中的 Git 集成操作

------

## ✅ 九、常用命令总结

```bash
git init              # 初始化仓库
git add .             # 添加所有更改
git commit -m "说明"  # 提交更改
git status            # 查看当前状态
git push              # 推送到 GitHub
git pull              # 拉取远程更新
```

------
