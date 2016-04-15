## 本地代码库回滚
    
```
git reset --hard commit-id :回滚到commit-id，讲commit-id之后提交的commit都去除

git reset --hard HEAD~3：将最近3次的提交回滚
```
## 远程代码库回滚1

```
git reset --hard HEAD~1
git push --force
```

## 远程代码库回滚2

```
应用场景：自动部署系统发布后发现问题，需要回滚到某一个commit，再重新发布

原理：先将本地分支退回到某个commit，删除远程分支，再重新push本地分支

操作步骤：

1、git checkout the_branch

2、git pull

3、git branch the_branch_backup //备份一下这个分支当前的情况

4、git reset --hard the_commit_id //把the_branch本地回滚到the_commit_id

5、git push origin :the_branch //删除远程 the_branch

6、git push origin the_branch //用回滚后的本地分支重新建立远程分支

7、git push origin :the_branch_backup //如果前面都成功了，删除这个备份分支
```
