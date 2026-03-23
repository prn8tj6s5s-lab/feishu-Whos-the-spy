# 🚀 上传到 GitHub 的完整指南

## 📋 准备工作

**仓库信息：**
- **GitHub 用户名**: prn8tj6s5s-lab
- **仓库名称**: feishu-Whos-the-spy
- **仓库类型**: 公开（Public）
- **仓库链接**: https://github.com/prn8tj6s5s-lab/feishu-Whos-the-spy

---

## 方式 A：使用 Git 命令行（推荐）

### 步骤 1：创建 GitHub 仓库

1. 访问 https://github.com/new
2. 填写以下信息：
   - **Repository name**: `feishu-Whos-the-spy`
   - **Description**: 飞书群聊谁是卧底游戏 Skill - 支持多局连续游戏、智能词语去重、标准话术模板
   - **Public**: ✅ 选中（公开仓库）
   - **Initialize this repository with a README**: ❌ 不选中（我们已经有 README.md 了）
3. 点击 **Create repository**

### 步骤 2：初始化本地仓库

```bash
# 进入技能目录
cd /home/gem/workspace/agent/skills/feishu-game-Whos-the-spy

# 初始化 git 仓库
git init

# 添加所有文件
git add .

# 提交
git commit -m "Initial commit: 谁是卧底游戏 Skill v1.7.0

- 完整的游戏逻辑和状态管理
- 15 个标准话术模板
- 词语参考库（100+ 组合）
- 词语历史记录（1000 局不重复）
- 场/局概念和 1 小时间隔判断
- 飞书群聊集成"
```

### 步骤 3：关联远程仓库

```bash
# 添加远程仓库（替换为你的实际仓库链接）
git remote add origin https://github.com/prn8tj6s5s-lab/feishu-Whos-the-spy.git

# 验证
git remote -v
```

### 步骤 4：推送到 GitHub

```bash
# 推送到 main 分支
git branch -M main
git push -u origin main
```

如果提示需要认证，使用以下方式之一：

**方式 1：使用 Personal Access Token（推荐）**
```bash
# 在 GitHub 设置中生成 Token：
# Settings → Developer settings → Personal access tokens → Generate new token
# 勾选 repo 权限
# 然后推送时使用：
git push https://<你的用户名>:<Token>@github.com/prn8tj6s5s-lab/feishu-Whos-the-spy.git main
```

**方式 2：使用 SSH（如果你配置了 SSH key）**
```bash
# 改用 SSH 链接
git remote set-url origin git@github.com:prn8tj6s5s-lab/feishu-Whos-the-spy.git
git push -u origin main
```

---

## 方式 B：使用 GitHub Desktop（图形界面）

### 步骤 1：下载并安装

访问 https://desktop.github.com/ 下载并安装 GitHub Desktop

### 步骤 2：添加本地仓库

1. 打开 GitHub Desktop
2. 点击 **File** → **Add Local Repository**
3. 选择文件夹：`/home/gem/workspace/agent/skills/feishu-game-Whos-the-spy`
4. 如果提示"This directory does not appear to be a Git repository"，点击 **Create a repository**

### 步骤 3：发布到 GitHub

1. 点击右上角 **Publish repository**
2. 填写信息：
   - **Name**: `feishu-Whos-the-spy`
   - **Description**: 飞书群聊谁是卧底游戏 Skill
   - ✅ **Keep this code private**: 不选中（公开仓库）
3. 点击 **Publish Repository**

---

## 方式 C：使用网页上传（最简单，适合首次）

### 步骤 1：创建仓库

1. 访问 https://github.com/new
2. 填写：
   - **Repository name**: `feishu-Whos-the-spy`
   - **Description**: 飞书群聊谁是卧底游戏 Skill
   - ✅ **Public**
   - ❌ 不初始化 README
3. 点击 **Create repository**

### 步骤 2：上传文件

1. 点击 **uploading an existing file** 链接
2. 将以下文件拖拽到上传区域：
   - SKILL.md
   - GAME_SCRIPTS.md
   - WORD_BANK.md
   - WORD_HISTORY.json
   - README.md
   - LICENSE
   - .gitignore
3. 填写提交信息：`Initial commit: 谁是卧底游戏 Skill v1.7.0`
4. 点击 **Commit changes**

---

## ✅ 验证上传成功

### 检查仓库

访问：https://github.com/prn8tj6s5s-lab/feishu-Whos-the-spy

应该看到：
- ✅ 所有 7 个文件
- ✅ README.md 正确显示
- ✅ 文件树完整

### 测试安装命令

```bash
# 在别人电脑上测试安装
npx skills add https://github.com/prn8tj6s5s-lab/feishu-Whos-the-spy
```

---

## 📊 安装说明（分享给别人）

### 安装命令

```bash
# 方式 1：直接安装
npx skills add https://github.com/prn8tj6s5s-lab/feishu-Whos-the-spy

# 方式 2：从 Skillhub 安装
SKILLS_API_URL=https://skills.volces.com/v1 npx -y skills add https://github.com/prn8tj6s5s-lab/feishu-Whos-the-spy -a openclaw -y --copy
```

### 分享文案

```
🎮 谁是卧底游戏 Skill 发布啦！

在飞书群聊中主持经典的"谁是卧底"游戏
✨ 多局连续游戏，无需重复配置
✨ 智能词语去重，1000 局不重复
✨ 15 个标准话术，体验一致性
✨ 场/局概念，1 小时间隔判断

安装命令：
npx skills add https://github.com/prn8tj6s5s-lab/feishu-Whos-the-spy

仓库地址：
https://github.com/prn8tj6s5s-lab/feishu-Whos-the-spy
```

---

## 🔧 后续更新

### 发布新版本

```bash
# 修改文件后
git add .
git commit -m "v1.8.0: 新增 XXX 功能"
git tag v1.8.0
git push origin main --tags
```

### 更新 README 中的版本号

在以下文件中更新版本号：
- README.md（徽章和更新日志）
- SKILL.md（YAML frontmatter）

---

## ❓ 常见问题

### Q: 推送时提示认证失败？
A: 使用 Personal Access Token 代替密码。在 GitHub Settings → Developer settings → Personal access tokens 生成。

### Q: 仓库名称可以改吗？
A: 可以，在 GitHub 仓库 Settings 中修改。但修改后安装链接也会变化。

### Q: 可以转为私有仓库吗？
A: 可以，在 Settings → Danger Zone → Change visibility 中修改。但别人就无法安装了。

### Q: 如何删除仓库重新创建？
A: Settings → Danger Zone → Delete this repository。然后重新创建即可。

---

**🚀 祝你上传顺利！** 🦞
