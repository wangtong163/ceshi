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
