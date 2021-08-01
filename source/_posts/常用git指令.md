---
title: 常用Git指令
date: 2021-08-01 18:30:00
tags: Git
---
git init 将目录变成仓库
git add
git commit -m ""
git status
git diff <file>
git log --graph --pretty=oneline --abbrev-commit 或者 git log --graph --oneline
git reflog
git reset --hard commit_id(HEAD)
git checkout -- <file> 将缓存区回滚工作区
git reset <file> 将仓库回滚缓存区
git rm <file>
ssh key to authorize ur pc
git remote add origin <git address> 链接远程仓库
git push -u origin master 第一次push
git clone <git address>
git branch (-d <branch>)(-D <branch> for unmerged branch)
git branch <branch> 创建
git checkout <branch> = git switch <branch>
git checkout -b <branch> = git switch -c <branch> 创建并切换
git merge <branch>
manually merge if conflicts
git merge --no-ff -m "" <branch> :: branch history kept
git stash (list/pop/apply <stash>/drop)
git cherry-pick <commit> 套用特定commit
git remote (-v) 查看远程仓库
git branch --set-upstream-to=origin/dev dev 建立branch链接
git pull 抓branch
git rebase 使log变直，但修改了commits（用于对本地变基清理历史）
git tag (<version>) (<commit>)
git show <tag>
git tag -a <version> -m "" <commit>
git tag -d <version>
git push origin <version> (--tags 全部)
git push origin :refs/tags/<version> 远程删除
