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

