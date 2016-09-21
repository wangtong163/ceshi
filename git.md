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
###基础
>初始化新仓库
```ruby
git init
```
>从现有仓库中克隆
```ruby 
git clone git:#项目仓库
```
>暂存制定文件
```ruby
git add 文件名
#如果文件名为 .  或者添加--all 则暂存所有文件
git add .
git add --all
```
>检查当前文件状态
```ruby 
git status
#位于分支 bj-1
#
#初始提交
#
#未跟踪的文件:
#  （使用 "git add <文件>..." 以包含要提交的内容）
#
#	git.md
#
#提交为空，但是存在尚未跟踪的文件（使用 "git add" 建立跟踪）
#现在文件已经暂存起来，下次提交直接提交到仓库
```
>忽略某些文件
>因为一些文件不需要纳入Git 的管理，也不希望它们总出现在未跟踪文件列表。通常都是些自动生成的文件，比如日志文件，或者编译过程中创建的临时文件等。
```ruby
cat .gitignore
*.[oa]
*~
#第一行告诉 Git 忽略所有以 .o 或 .a 结尾的文件。一般这类对象文件和存档文件都是编译过程中出现的，我们用不着跟踪它们的版本。第二行告诉 Git 忽略所有以波浪符（~）结尾的文件，许多文本编辑软件（比如 Emacs）都用这样的文件名保存副本。此外，你可能还需要忽略 log，tmp 或者 pid 目录，以及自动生成的文档等等。要养成一开始就设置好 .gitignore 文件的习惯，以免将来误提交这类无用的文件。
#文件 .gitignore 的格式规范如下：

#1.所有空行或者以注释符号 ＃ 开头的行都会被 Git 忽略。
#2.可以使用标准的 glob 模式匹配。
#3.匹配模式最后跟反斜杠（/）说明要忽略的是目录。
#4.要忽略指定模式以外的文件或目录，可以在模式前加上惊叹号（!）取反。
```
>要查看尚未暂存的文件更新了哪些部分，不加参数直接输入 git diff：
```ruby
git diff
diff --git a/git.md b/git.md
index f0a6a09..d41eea2 100644
--- a/git.md
+++ b/git.md
@@ -19,4 +19,53 @@ git config --global merge.tool vimdiff
 ```ruby
 git config --list
 ```
+###基础
+>初始化新仓库
+```ruby
+git init
+```
+>从现有仓库中克隆
```
>此命令比较的是工作目录中当前文件和暂存区域快照之间的差异，也就是修改之后还没有暂存起来的变化内容。

>若要看已经暂存起来的文件和上次提交时的快照之间的差异，可以用 git diff --cached
```ruby
git diff --cached
diff --git a/git.md b/git.md
index f0a6a09..d41eea2 100644
--- a/git.md
+++ b/git.md
@@ -19,4 +19,53 @@ git config --global merge.tool vimdiff
 ```ruby
 git config --list
 ```
+###基础
+>初始化新仓库
+```ruby
+git init
+```
+>从现有仓库中克隆
```
>提交更新
```ruby
git commit
#如果加参数-m 则直接写入更新说明 
git commit -m '更新说明'
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
冲突冲突冲突
啊啊啊vdadsfe

