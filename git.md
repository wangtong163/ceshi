#git学习笔记

###安装

```ruby
apt-get install git
```
###配置
>首次安装之后，必须配置用户信息
```ruby
git config --global user.name "wangtong"
git config --global user.email 936217172@qq.com
##默认文本编辑器
git config --global core.editor vim
##差异分析工具
git config --global merge.tool vimdiff
```
>查看配置信息
```ruby
git config --list
```


>移动文件
```ruby
git mv file_from file_to#要在 Git 中对文件改名，可以这么做
```
>查看提交历史
```ruby
git log
git log -p #显示每次提交的差异
git log --stat #仅显示简要的增改行数统计
```
>从远程仓库抓取数据
```ruby
git fetch [remote-name]#只抓取更新的数据
```
>推送数据到远程仓库
```ruby
git push origin master
```
>查看远程仓库信息
```ruby
git remote show origin
```
>远程仓库的删除和重命名
```ruby
git remote rename name1 name2 #修改远程仓库名
git remote rm paul #删除远程仓库
```
>列显已有的标签
```ruby
git tag
```
>新建标签
```ruby
git tag -a v0.1 -m '测试标签'
```
###分支
>新建并且切换到分之
```ruby
git checkout -b bj-1 #相当于执行两条命令

git branch bj-1 #新建分支
git checkout bj-1 #切换分支
```
>删除分之
```ruby
git branch -d bj-1
```
>合并分支
```ruby
git checkout master #切换到master分之
git merge bj-1 #合并分支
```
>遇到冲突时的分支合并
