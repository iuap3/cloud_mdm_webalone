# 云MDM文档编写流程与规范

## 编写流程

第一步：建立产品目录
          
根据产品名字 修改模板中相应内容，按规则给出书写方法。
         
第二步：创建 github仓库   (https://github.com/iuap3/)

把已经建立好的产品规范目前，上传到github仓库。

第三步：通知各角色编写文档

在github上编写文档。

第四步：收到提交后，合并，定时推送到网站。


## 编写方式

在线仓库地址--- https://github.com/iuap3/

当你想更新文档仓库里内容时，要走一个流程：

1、先 fork 别人的仓库，相当于拷贝一份，相信我，不会有人直接让你改修原仓库的；

2、clone 到本地编写MD文件，push到fork 的仓库；

3、fork 的仓库发起 pull request 给原仓库，让他看到你修改合并。

至此，整个 pull request 的过程就结束了。

编写就是MD标准格式，请参考线上其他文档。


## 编写规范

### 文案风格
 
1、一定多检查，确保没有错别字。
 
2、即使是流行语中的谐音错别字也不要使用，比如「墙裂」、「童鞋」等。
 
3、我们崇尚精练的文风。请在检查中把对表达意思没有明显作用的字、词、句删除，在不影响表达效果的前提下把文案长度减到最短。
 
4、记住，如果你写了一条文案觉得非常聪明非常好笑，很可能需要停下来想一下用户是否能理解。
 
### 目录要求
 
1、  文件命名规则：
 


```
* [目录名称](articles/产品英文名XXX/章节编号X-/目录英文名.md)
```



例如：



```
* [产品概述](articles/esb/1-/prod_intro.md)
```



articles文件夹，articles的下级产品英文名“esb”文件夹，产品英文名esb的下级“1-”文件夹，“1-”的下级prod_intro.md内容文件。

英文名必须全部小写。

其他章节依此方法设置即可。
 
2、  图片的存放位置：



```
* [目录名称](articles/产品英文名XXX/章节编号X-/图片images/图片英文名.jpg) 
```



例如：



```
* [产品概述](articles/esb/1-/images/tupian.jpg)
```




比如产品概述中的图片，本章中包含的所有图片请放置于articles/产品英文名esb /1-/images文件夹下，无此文件夹请依次建立。

 
3、  此目录必须在SUMMARY.md文件中。所有MD文件是UTF-8编码。

SUMMARY格式：



```
# 集成总线

* [集成总线](articles/esb/1-/)
   * [产品概述](articles/esb/1-/introduction.md)
   * [产品优势](articles/esb/1-/advantage.md)
   * [应用场景](articles/esb/1-/scenarios.md)
   * [基础架构](articles/esb/1-/infrastructure.md)
   * [产品历程](articles/esb/1-/course.md)
* [快速入门](articles/esb/2-/)
   * [场景一：如何快速更换导航栏](articles/esb/2-/scene1.md)
   * [场景二：如何开发widget](articles/esb/2-/scene2.md)
* [用户手册](articles/esb/3-/)
* [常见问题](articles/esb/4-/)
   * [如何开发widget](articles/esb/4-/question1.md)
```





4、  在上例中，[集成总线] 、[快速入门] 、[用户手册]和[常见问题]是一级目录，其余为二级目录。要求一级目录无内容，仅做目录。

例如：



```
* [集成总线](articles/esb/1-/)
```



比如一级目录“集成总线”后面不需要加MD文件（如introduction.md内容文件）。

二级目录必须缩进。

 
5、  必须严格按此格式写目录。

## Markdown简明语法

1、标题

类 Atx 形式是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶，例如：



```
# 这是 H1

## 这是 H2

###### 这是 H6
```
转换后：

# 这是 H1

## 这是 H2

###### 这是 H6


2、列表

1）无序列表可以用* ， + ， — 来创建，例如：


```
* 1
* 2
* 3
```

转换后：

* 1
* 2
* 3

2）有序列表只有如下这一种方式，注意，数字后面的点只能是英文的点：

1. 列表1
2. 列表2
3. 列表3

3、代码框

如果代码量比较少，只有单行的话，可以用单反引号包起来。

多行可以用右上角的“<>” Code功能。

4、表格

可以访问：http://pressbin.com/tools/excel_to_html_table/index.html

进行表格转换。

5、图片

可以使用右上角“Insert Image”功能。

6、题注居中

对于题注需要居中的情况，可以使用如下命令：



```
<p align="center">图1</p>
```

转换后：

<p align="center">图1</p>