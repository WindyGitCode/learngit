# 📖 Git 常用指令速查表（初学者版）

## 🔹 仓库操作
```bash
git init              # 在当前文件夹初始化一个新的本地仓库
git clone <url>       # 克隆远程仓库到本地
```

---

## 🔹 查看状态和历史
```bash
git status            # 查看当前状态（改了哪些文件，有没有提交）
git log               # 查看提交历史
git log --oneline     # 简洁模式显示提交历史
git diff              # 查看未暂存的修改
git diff --staged     # 查看已暂存的修改
```

---

## 🔹 添加和提交
```bash
git add <file>        # 把文件加入暂存区
git add .             # 把所有修改过的文件加入暂存区
git commit -m "说明"  # 提交代码，并附带说明
```

---

## 🔹 分支操作
```bash
git branch            # 查看所有分支
git branch <name>     # 创建新分支
git checkout <name>   # 切换到分支（旧写法）
git switch <name>     # 切换到分支（推荐新写法）
git switch -c <name>  # 创建并切换到新分支
git merge <branch>    # 合并分支
```

---

## 🔹 远程操作
```bash
git remote -v         # 查看远程仓库地址
git pull              # 拉取远程最新代码并合并
git push              # 推送代码到远程仓库
git push -u origin <branch>  # 推送并设置默认上游分支
```

---

## 🔹 撤销/回滚（谨慎使用❗）
```bash
git restore <file>        # 撤销对某个文件的修改（还原到最近一次提交）
git reset --hard <commit> # 回到某个历史提交（会丢失之后的修改）
git revert <commit>       # 撤销某次提交（保留历史记录，推荐）
```

---

## 🔹 常用组合场景

### 1. 第一次提交代码
```bash
git init
git add .
git commit -m "first commit"
git remote add origin <url>
git push -u origin main
```

### 2. 日常提交更新
```bash
git status
git add .
git commit -m "更新说明"
git pull   # 先拉取，避免冲突
git push
```
