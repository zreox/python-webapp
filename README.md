Python webapp 
=============

# 停止使用
由于前期对 git 理解不够，有以下几点失误，以后需要注意。

## 未添加 .gitignore 文件
在添加 .gitignore 文件之前已提交过的项目无法过滤，为避免这种情况，需要在项目初始就创建好 .gitignore 文件，然后再去 push。这种情况并非无解，暂时不说。

## 多个分支长期并存
合适的做法是：
- 开发前先 pull 远程仓库
- 在此基础上新建 new_branch，在这个 branch 上进行开发
- 开发完成后 checkout 至 master，使用 no-ff 模式进行 merge
- 进行 tag，add，commit，push 等后续操作
- `git branch -d new-branch`，删除开发时的分支

## tag 应在 master 分支上进行操作
进行 tag 操作之前，先 checkout 至 master 分支。tag 操作可以作为 push 前的最后一步。

# 项目迁移
该项目在 [webapp-python](https://github.com/zreox/webapp-python) 重启
