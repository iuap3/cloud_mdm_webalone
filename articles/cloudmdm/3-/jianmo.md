# 主数据建模

主要包括实体建模、主数据定义和主数据维护。可以把建模完成的实体发布到动态的主数据节点或者导出Excel模板。

## 实体建模

点击【主数据建模】→【实体建模】，进入实体建模页面，在该页面里，左边是实体的分类树，右边是对实体的新增、修改、删除和导出Excel模板等操作。

![](/articles/cloudmdm/3-/images/image4.png)

<p align="center">图：实体建模</p>
 

**分类树管理**

实体分类树是多级树结构。树根节点默认为“主数据分类”。

* 新增分类

单击实体分类树的根节点“主数据分类”，单击〖新增〗弹出窗口，选择“主数据分类”，填写内容（*表示必填项）后，单击〖确定〗。

![](/articles/cloudmdm/3-/images/image5.png)

<p align="center">图：新增分类</p> 

新增的主数据分类，会出现在分类树下。

* 新增实体

单击分类树的子节点，单击〖新增〗弹出窗口，选择“主数据”，填写内容（*表示必填项）后，单击〖确定〗。新增实体后，选择该实体，单击〖新增〗弹出窗口，选择“主表”，增加一个主表，如下图。

![](/articles/cloudmdm/3-/images/image6.png)

<p align="center">图：新增主数据</p>  

选择实体后，单击〖新增〗弹出窗口，选择“子表”，增加一个子表，如下图。

![](/articles/cloudmdm/3-/images/image7.png)

<p align="center">图：新增子表</p>   

实体属性的定义项包括：

1. 字段编码：唯一的英文编码标识别；

2. 字段名称：中文属性名称；

3. 类型：实体数据类型。包括：字符，整型，布尔，浮点型，日期，日期时间，参照，下拉，图片，文件，大文本，时间；

4. 长度：实体类型的数据宽度；

5. 是否必输项；

6. 是否唯一；

7. 查询条件：是否可查询。勾选后，将在主数据节点左侧显示查询框；

8. 默认值：设置此值后，在界面会自动出现。


* 显示分类

单击分类树下的某个主数据分类，在右边会出现该分类的信息。

![](/articles/cloudmdm/3-/images/image8.png)

<p align="center">图：显示分类</p>
 

* 显示实体

单击分类树下的某个实体，在右边会出现该实体的主子表信息。可以编辑或删除主子表信息。

![](/articles/cloudmdm/3-/images/image9.png)

<p align="center">图：显示主数据</p>

* 修改分类

单击分类树下的某个主数据分类，单击〖修改〗弹出窗口，填写内容（*表示必填项）后，单击〖确定〗。

![](/articles/cloudmdm/3-/images/image10.png)

<p align="center">图：修改分类</p>  

* 删除分类

单击分类树下的某个主数据分类，单击〖删除〗，弹出确认提示。

如果该分类下存在实体的定义，则不能删除该分类，弹出如下提示框：

![](/articles/cloudmdm/3-/images/image11.png)

<p align="center">图：删除分类</p>

**注：修改和删除实体与上述方法相同。**


* 导出Excel

单击定义树的某个分类下的某个实体，单击〖导出excel模板〗，生成Excel文件（文件名为实体的编码），包含该实体所包含的实体属性，保存到本地。

![](/articles/cloudmdm/3-/images/image12.png)

<p align="center">图：导出Excel</p>
 

## 主数据定义

单击【主数据建模】→【主数据定义】，进入如下界面，在此页面可进行主数据界面风格的选择、配置参照的编辑、配置下拉框和预览等操作。

![](/articles/cloudmdm/3-/images/image13.png)

<p align="center">图：主数据定义</p>
 

**界面风格**：有默认、树表和树卡三种风格。

树表：单击〖树表〗按钮，出现下图所示窗口，选择内容后，单击〖保存并发布〗或者〖反发布〗。

![](/articles/cloudmdm/3-/images/image14.png)

<p align="center">图：树表</p>


单击〖树卡〗按钮，出现下图所示窗口，选择内容后，单击〖保存并发布〗或者〖反发布〗。

![](/articles/cloudmdm/3-/images/image15.png)

<p align="center">图：树卡</p>
 

**配置参照**：选择一个主数据，单击〖配置参照〗按钮，出现下图所示页面，填写内容，点击〖保存〗。

![](/articles/cloudmdm/3-/images/image16.png)

<p align="center">图：配置参照</p>

**配置下拉框**：选择一个主数据，单击〖配置下拉框〗按钮，出现下图所示页面，填写内容，点击〖保存〗。

![](/articles/cloudmdm/3-/images/image17.png)

<p align="center">图：配置下拉框</p> 

**预览**：选择主数据，单击〖预览〗按钮，出现预览页面：

![](/articles/cloudmdm/3-/images/image18.png)

<p align="center">图：预览</p> 


## 主数据维护

单击【主数据建模】→【主数据维护】，进入如下界面，在此页面可进行主数据的新增、修改、下载、删除和高级查询等操作。

![](/articles/cloudmdm/3-/images/image19.png)

<p align="center">图：主数据维护</p> 

**新增**：选择主数据，单击〖新增〗按钮，填入相应内容，按〖确定〗。如下图所示：

![](/articles/cloudmdm/3-/images/image20.png)

<p align="center">图：新增主数据</p> 

**修改**：选择一条列表数据，单击〖修改〗按钮。修改完成后按〖确定〗。如下图所示：

![](/articles/cloudmdm/3-/images/image21.png)

<p align="center">图：修改主数据</p> 

**下载**：选择列表数据，单击〖下载〗，生成Excel文件，保存到本地。

**删除**：选择列表数据，单击〖删除〗进行删除。如下所示：

![](/articles/cloudmdm/3-/images/image22.png)

<p align="center">图：删除主数据</p> 

**高级查询**：单击〖高级查询〗，选择条件进行查询，可以重置条件设置。

![](/articles/cloudmdm/3-/images/image23.png)

<p align="center">图：高级查询</p>









 
