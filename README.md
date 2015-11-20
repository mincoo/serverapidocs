该文档描述为移动端与业务系统数据交互接口，接口地址`{API_URL}`为  
>正式服务器：`http://ymxxapi.uxiaoxi.com`  
>测试服务器：`http://api-test.uxiaoxi.com`
  
数据校验方式按照参数列表（不包括sign）按字母排序连接参数，然后做md5加密。  
例如：`sign = md5("phone=12345678901&type=1")`  

第三方消息推送为极光推送（JPush55555）。  
群组推送tag值为`g+群组ID`（例如：`g615`），用户推送alias值为`u+用户ID`（例如：`u123`），  
推送内容extras格式为  
```
{  
	"mid":9,  
	"type":1,  
	"url":""  
}
```
