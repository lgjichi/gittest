# Git 常用命令列表

## 基础配置
```bash
git config --global user.name "你的名字"    # 设置用户名
git config --global user.email "你的邮箱"   # 设置邮箱
git config --list                          # 查看配置信息
```

## 仓库操作
```bash
git init                       # 初始化一个新的Git仓库
git clone <url>                # 克隆远程仓库
git remote add origin <url>    # 添加远程仓库
git remote -v                  # 查看远程仓库信息
```

## 基本工作流
```bash
git status                     # 查看工作区状态
git add <file>                 # 添加文件到暂存区
git add .                      # 添加所有更改到暂存区
git commit -m "提交信息"        # 提交更改
git pull                       # 拉取远程更改并合并
git push origin <branch>       # 推送到远程分支
```

## 分支操作
```bash
git branch                     # 查看本地分支
git branch -r                  # 查看远程分支
git branch -a                  # 查看所有分支
git branch <name>              # 创建新分支
git checkout <branch>          # 切换分支
git checkout -b <branch>       # 创建并切换到新分支
git merge <branch>             # 合并指定分支到当前分支
git branch -d <branch>         # 删除分支
```

## 日志与差异
```bash
git log                        # 查看提交历史
git log --oneline              # 查看简洁的提交历史
git diff                       # 查看未暂存的更改
git diff --staged              # 查看已暂存的更改
git show <commit>              # 查看某次提交的详细信息
```

## 撤销与重置
```bash
git checkout -- <file>         # 丢弃工作区的修改
git reset HEAD <file>          # 撤销暂存区的修改
git reset --hard HEAD^         # 回退到上一个版本
git reset --hard <commit>      # 回退到指定版本
git revert <commit>            # 创建一个新提交来撤销指定提交
```

## 暂存操作
```bash
git stash                      # 暂存当前修改
git stash list                 # 查看暂存列表
git stash pop                  # 恢复最近的一次暂存
git stash apply                # 应用暂存但不删除暂存记录
git stash drop                 # 删除暂存记录
```

## 标签操作
```bash
git tag                        # 查看所有标签
git tag <name>                 # 创建标签
git tag -a <name> -m "消息"    # 创建带注释的标签
git push origin <tagname>      # 推送标签到远程
```

## 高级操作
```bash
git rebase <branch>            # 变基操作
git cherry-pick <commit>       # 挑选某个提交合并到当前分支
git blame <file>               # 查看文件的每一行是谁修改的
git reflog                     # 查看所有操作记录
```