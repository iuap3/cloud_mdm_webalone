# 主数据权限

主数据权限主要由远程系统和主数据权限构成，用于设置业务系统对主数据的操作权限。

## 远程系统

点击【主数据权限】→【远程系统】，进入远程系统操作页面，此页面可进行远程系统的新增、修改和删除等操作。

![](/articles/cloudmdm/3-/images/image43.png)

<p align="center">图：远程系统</p>

* 新增远程系统

单击〖新增〗按钮，弹出下图所示窗口，填写内容后点击〖确定〗。

![](/articles/cloudmdm/3-/images/image44.png)

<p align="center">图：新增远程系统</p> 


* 修改远程系统

选择一条远程系统记录，单击〖修改〗按钮，弹出如下窗口，修改内容后，单击〖确定〗。

![](/articles/cloudmdm/3-/images/image45.png)

<p align="center">图：修改远程系统</p>


* 删除远程系统

选择远程系统，单击〖删除〗按钮。

* 分发服务接口说明

供二次开发使用，具体如下：



```
rest服务 
1.
http://ip:port/iuapmdm/cxf/mdmrs/center/com.yonyou.iuapmdm.centerService/insertMd
post请求参数
{
"systemCode":"远程系统编码",
"gdCode":"主数据编码",
"masterData":"主数据（json数组格式）"
}
header里面需要两个参数
mdmtoken远程系统的令牌  (7f092a4a-1aeb-4269-a593-d5d5ad24c8ce)
tenantid租户id  (tenant)
返回结果
{
"data":"返回的主数据(json)",
"success":"MDM与第三方系统交互成功与否",
"message":"结果描述信息"
}

2.
http://localhost:8082/iuapmdm/cxf/mdmrs/center/com.yonyou.iuapmdm.centerService/queryListMdByMdmCodes
post请求参数
{
"systemCode":"远程系统编码",
"gdCode":"主数据编码",
"codes":[主数据编码（数组格式]
}
header里面需要两个参数
mdmtoken远程系统的令牌  (7f092a4a-1aeb-4269-a593-d5d5ad24c8ce)
tenantid租户id  (tenant)
返回结果
{
"data":"返回的主数据(json)",
"success":"MDM与第三方系统交互成功与否",
"message":"结果描述信息"
}

3.
http://localhost:8082/iuapmdm/cxf/mdmrs/center/com.yonyou.iuapmdm.centerService/queryListMdByIds
post请求参数
{
"systemCode":"远程系统编码",
"gdCode":"主数据定义编码",
"codes":[id（数组格式）]
}
header里面需要两个参数
mdmtoken远程系统的令牌  (7f092a4a-1aeb-4269-a593-d5d5ad24c8ce)
tenantid租户id  (tenant)
返回结果
{
"data":"返回的主数据(json)",
"success":"MDM与第三方系统交互成功与否",
"message":"结果描述信息"
}

4.
物料服务
http://ip:port/iuapmdm/cxf/mdmrs/center/com.yonyou.iuapmdm.centerService/insertDynaMd
post请求参数
{
"systemCode":"远程系统编码",
"gdCode":"新的物料编码",
"masterData":"主数据（json数组格式）"
}
header里面需要两个参数
mdmtoken远程系统的令牌  (7f092a4a-1aeb-4269-a593-d5d5ad24c8ce)
tenantid租户id  (tenant)
返回结果
{
"data":"返回的主数据(json)",
"success":"MDM与第三方系统交互成功与否",
"message":"结果描述信息"
}

5.
http://localhost:8082/iuapmdm/cxf/mdmrs/center/com.yonyou.iuapmdm.centerService/queryDynaListMdByMdmCodes
post请求参数
{
"systemCode":"远程系统编码",
"gdCode":"新的物料编码",
"codes":[主数据编码（数组格式）]
}
header里面需要两个参数
mdmtoken远程系统的令牌  (7f092a4a-1aeb-4269-a593-d5d5ad24c8ce)
tenantid租户id  (tenant)
返回结果
{
"data":"返回的主数据(json)",
"success":"MDM与第三方系统交互成功与否",
"message":"结果描述信息"
}

6.
http://localhost:8082/iuapmdm/cxf/mdmrs/center/com.yonyou.iuapmdm.centerService/queryDynaListMdByIds
post请求参数
{
"systemCode":"远程系统编码",
"gdCode":"新的物料编码",
"codes":[id（数组格式]
}
header里面需要两个参数
mdmtoken远程系统的令牌  (7f092a4a-1aeb-4269-a593-d5d5ad24c8ce)
tenantid租户id  (tenant)
返回结果
{
"data":"返回的主数据(json)",
"success":"MDM与第三方系统交互成功与否",
"message":"结果描述信息"
}




分发服务 由业务系统实现，供主数据系统调用
入参 @XmlRootElement(name="distributePostDataVO")
{
"systemCode":"远程系统编码",
"mdType":"主数据定义编码或新的物料编码",
"action":"动作，distribute",
"masterData":"主数据（json数组格式）",
}
出参 @XmlRootElement(name="distributeRetVO")
{
"mdMappings":[{"mdmCode":"mdmcode", "entityCode":"实体编码", "busiDataId":"远程id", "errorMsg":"错误信息", "success":"成功标志，布尔型"}], //数组对象@XmlRootElement(name="mdMapingVO")
"success":"成功标志，布尔型",
"message":"返回信息",

}
```




## 主数据权限

点击【主数据权限】→【主数据权限】，进入主数据权限操作页面，此页面可进行主数据权限的新增、修改和删除等操作。基于主数据建模属性的操作权限包括：可读、可写、可订阅。数据权限配置过滤条件，用于装载和分发数据过滤。

![](/articles/cloudmdm/3-/images/image46.png)

<p align="center">图：主数据权限</p>


* 新增

选择左侧主数据，单击〖新增〗按钮新增权限，弹出新窗口，输入内容，单击〖确定〗。

![](/articles/cloudmdm/3-/images/image47.png)

<p align="center">图：新增主数据权限</p>
 
**主数据**：必输项；

**权限名称**：必输项；

**权限编码**：必输项，若先选择主数据，则会自动匹配到主数据的编码和名称；

**业务系统**：下拉选择；

**过滤条件**：根据条件判断哪些数据可以分发装载；

**条件编辑**：在新增权限的时候，根据实际业务场景设置条件，比如“名称”包含…，等于…或者不等于…。

![](/articles/cloudmdm/3-/images/image48.png)

 
<p align="center">图：条件编辑</p>


**主数据权限**：有可读、可写、可订阅的权限，通过复选框进行选择。如果选择“可读”，表示具有分发权限；选择“可写”，表示具有装载主数据权限；选择“可订阅”，表示具有自动分发权限，如果设置了业务系统对主数据的订阅权限，则维护主数据时，自动分发到业务系统。


* 修改

选择定义树的某个分类，单击〖修改〗，弹出新窗口，修改内容，单击〖确定〗。

![](/articles/cloudmdm/3-/images/image49.png)

<p align="center">图：修改主数据权限</p>


* 删除

选择一行记录，单击〖删除〗按钮，弹出确认窗口。
