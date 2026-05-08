# 新手上传代码到 GitHub 完整教程

> 本教程专为第一次使用 GitHub 的用户编写，跟着做就能成功。

---

## 第一步：安装必要工具

你需要安装两个免费工具。已经装好的可以跳过。

### 1.1 安装 Git（版本控制工具）

1. 打开浏览器，访问 https://git-scm.com/download/win
2. 下载会自动开始（下载一个 `.exe` 安装包）
3. 双击运行安装包，一路点击 **Next** 即可（全部保持默认选项）
4. 安装完成后，**重启 WorkBuddy** 或电脑

验证安装成功：在 WorkBuddy 里跟我说 "帮我检查 git 装好了没"

### 1.2 安装 GitHub CLI（命令行工具，比网页操作更快）

1. 打开浏览器，访问 https://cli.github.com/
2. 点击 **Windows** 下载安装包
3. 双击运行，一路 **Next**
4. 安装完成后，**重启 WorkBuddy**

验证安装成功：在 WorkBuddy 里跟我说 "帮我检查 GitHub CLI 装好了没"

---

## 第二步：注册 GitHub 账号

如果你已经有 GitHub 账号，直接跳到第三步。

1. 打开浏览器，访问 https://github.com
2. 点击右上角 **Sign up**
3. 输入邮箱 → 设置密码 → 设置用户名（建议用英文，比如 `zhangsan`）
4. 按提示完成验证（拼图验证码）
5. 去邮箱点击验证链接，完成注册
6. **重要**：记住你的用户名和密码！

---

## 第三步：登录 GitHub CLI

安装好工具后，让 WorkBuddy 帮你执行下面这条命令：

```bash
gh auth login
```

或者在 WorkBuddy 里跟我说：**"帮我登录 GitHub"**

执行后会弹出一个窗口或在命令行里让你选择：
- 选择 **GitHub.com**
- 选择 **Login with a web browser**
- 会给你一个验证码（比如 `ABCD-1234`）
- 按回车键，浏览器会自动打开 GitHub 授权页面
- 输入验证码，点击 **Authorize github**
- 回到 WorkBuddy，看到 `Logged in as xxx` 就是成功了

---

## 第四步：创建 GitHub 仓库

在 WorkBuddy 里跟我说：**"帮我在 GitHub 上创建一个 newbie-engager 仓库"**

WorkBuddy 会帮你执行类似这样的命令：

```bash
cd ~/Desktop/newbie-engager
git init
git add .
git commit -m "init: newbie-engager skill"
gh repo create newbie-engager --public --source=. --push
```

执行成功后，你会得到一个网址，比如：
`https://github.com/你的用户名/newbie-engager`

这就是你的代码仓库页面，任何人都能通过这个链接看到你的代码。

---

## 第五步：以后如何更新代码到 GitHub

当你修改了技能文件，想更新到 GitHub 上时，让 WorkBuddy 帮你执行下面三步：

### 5.1 修改了文件后，先"暂存"

```bash
cd ~/Desktop/newbie-engager
git add .
```

### 5.2 写一个提交说明

```bash
git commit -m "修改内容说明"
```

`"修改内容说明"` 要换成你实际改了什么，比如：
- `"fix: 修复财务场景话术"
- `"feat: 添加销售场景示例"
- `"docs: 更新边界说明"

### 5.3 推送到 GitHub

```bash
git push
```

完成！打开你的仓库页面就能看到最新内容了。

---

## 常见问题和命令速查表

| 你想做什么 | 命令 |
|-----------|------|
| 查看改了哪些文件 | `git status` |
| 查看修改内容 | `git diff` |
| 撤销某个文件的修改 | `git checkout -- 文件名` |
| 查看提交历史 | `git log --oneline` |
| 从 GitHub 拉取最新代码 | `git pull` |
| 查看当前登录的 GitHub 账号 | `gh auth status` |

---

## 需要 WorkBuddy 帮你做什么？

直接在聊天里跟我说：
- **"帮我检查 git 装好了没"** → 我会检查环境
- **"帮我登录 GitHub"** → 我会执行 `gh auth login`
- **"帮我把这个技能传到 GitHub"** → 我会创建仓库并上传
- **"帮我更新 GitHub 上的代码"** → 我会执行 add/commit/push

---

_本教程由 WorkBuddy 生成，遇到问题随时问我。_
