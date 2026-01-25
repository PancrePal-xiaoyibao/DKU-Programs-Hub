# GitHub Pull Request 提交流程

本文档介绍了如何从克隆仓库开始，到创建新的分支、提交代码、更改 commit、推送分支到远程仓库，以及如何在合并后删除无用分支的整个过程。

## 1. 克隆仓库

首先，将远程仓库克隆到本地。
```bash
git clone https://github.com/your-username/repository-name.git
```
- **说明**：
  - `git clone` 命令用于从远程仓库复制整个项目到本地目录。
  - `https://github.com/your-username/repository-name.git` 是仓库的 URL，请根据实际仓库地址进行修改。

## 2. 切换到项目目录

进入刚刚克隆的仓库目录。
```bash
cd repository-name
```
- **说明**：
  - `cd repository-name` 命令将当前工作目录切换到仓库目录，后续的所有 Git 操作都会在该目录下进行。

## 3. 创建并切换到新的特性分支

创建一个新的分支，并立即切换到该分支。
```bash
git checkout -b feature-branch-name
```
- **说明**：
  - `git checkout -b feature-branch-name` 命令创建名为 `feature-branch-name` 的新分支，并切换到该分支进行开发。
  - 建议将 `feature-branch-name` 修改为描述具体功能的分支名称，如 `fix-login-bug`、`add-user-profile` 等。

## 4. 添加需要提交的更改

将你修改的文件添加到暂存区。
```bash
git add .
```
- **说明**：
  - `git add .` 命令将当前目录下所有更改的文件添加到暂存区。
  - 你也可以指定具体的文件名称，如 `git add index.html` 或 `git add src/app.js`，以选择性提交更改。

## 5. 创建提交记录

创建一次提交记录，描述你所做的更改。
```bash
git config --global user.email "github注册邮箱"
git config --global user.name "github用户名"
git commit -m "描述你的更改，例如：Fix bug in login feature"
```
- **说明**：
  - `git commit -m "..."` 命令将暂存区中的更改提交到本地仓库，其中 `-m` 参数后面跟的是提交描述。
  - 提交信息要简洁明了，描述清楚本次提交的目的。

## 6. 推送分支到远程仓库

将创建的新分支推送到远程仓库。
```bash
git push origin feature-branch-name
```
- **说明**：
  - `git push origin feature-branch-name` 命令将本地 `feature-branch-name` 分支推送到远程仓库的对应分支。
  - 推送完成后，你就可以在 GitHub 上创建一个 Pull Request 来请求将你的更改合并到主分支。

## 7. 代码修改后的操作

如果在提交后发现还需要修改代码，可以继续编辑并覆盖之前的提交：

1. 修改代码后，再次添加改动。
   ```bash
   git add .
   ```
   - **说明**：将新的更改添加到暂存区。

2. 修改已有提交的信息，并将暂存区的改动加入到上一次提交中。
   ```bash
   git commit --amend -m "更新后的描述"
   ```
   - **说明**：
     - `--amend` 选项会修改上一次提交，包括合并新的改动并更新提交信息。
     - 请确保只有在尚未与他人共享该分支时使用 `--amend`，因为它会重写提交记录。

3. 强制推送修改后的提交到远程仓库。
   ```bash
   git push origin feature-branch-name --force
   ```
   - **说明**：
     - `--force` 的作用是强制覆盖远程分支上的提交记录，使得远程分支与本地提交保持同步。
     - 注意：强制推送会覆盖远程仓库的历史记录，请与团队成员确认再操作。

## 8. 合并 Pull Request 后删除分支（可选）

Pull Request（PR）被合并后，可以删除本地和远程上的分支，以保持仓库的清洁。

1. 删除本地分支：
   ```bash
   git branch -d feature-branch-name
   ```
   - **说明**：
     - `git branch -d feature-branch-name` 命令用于删除本地的 `feature-branch-name` 分支。
     - `-d` 选项会在分支已被合并后安全删除分支。

2. 删除远程分支：
   ```bash
   git push origin --delete feature-branch-name
   ```
   - **说明**：
     - `git push origin --delete feature-branch-name` 命令用于删除远程仓库中的 `feature-branch-name` 分支。
