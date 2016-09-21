#macdown 学习笔记
**快捷键**
`ctrl+/`帮助，查看更多语法帮助
`*斜体内容*` 如：*斜体*
`**粗体**` 如：**粗体**
`#放大字体，#符号越多，字体越小`如：
###放大
`[链接]·(要连接到的地方)`[链接](www.baidu.com)注，所有内容都可以用HTML标签代替
脚注`[^demo]`,下方用同样的内容定位[^demo]。不过必须加冒号。
**代码块**
```python
在```python (代码内容) ```  里面放代码块
如：
var a = 'nohao';
content.log(a);
class test{
}
if(true){
}
function abc(){
	
}
```
###表格
`|字段1|字段2|字段3|
|:---(左对齐)|-(右对齐)--:|:-(居中对齐)-:|
|值1|值2|值3|`
如：
|name|age|sex|
|:---|--:|:-:|
|张三|18|男|
|李四|22|女|
###流程图
```flow
st=>start: 开始
e=>end
op=>operation: 过程1
op1=>operation: 过程2
cond=>condition: yes ro no?
st->op->op1->cond
cond(yes)->e
cond(no)->op1
```
`流程 start 开始， end 结束， operation 过程，condition 判断分支，`
###复选框
- [x]选项1
- [ ]选项2
- [ ]选项3
`- [ ]未选中 - [x]选中 中间有空格`
>**注意**引用的文字`>`开头
###列表
1. 有序列表
2. 2
3. 3
4. 4
- 无序列表
- 2
- 3
- 4
###

aaa


[^demo]:脚注内容