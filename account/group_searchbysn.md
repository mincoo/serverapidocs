##根据班号搜索群组
根据班号查询用户信息。

####1.基本信息
- 接口地址：`{API_URL}/group/searchbysn` 
- 请求方式：POST


####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |--------   |
| uid       | 是        | 用户ID    |
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|
| sn        | 是        | 班级编号|

####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":{
		"gid":615,
		"uid":123,
		"name":"六年级英语5班",
		"uname":"张老师",
		"sn":2046,
		"province":"北京",
		"city":"北京市",
		" district":"海淀区",
		"school":"人大一中",
		"face":""
	}
}
```

|键      |类型  |说明  |
|--------|------|------|
|status  |int   |搜索结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|
|gid     |int   |群组ID|
|uid     |int   |创建者ID|
|name    |String|群组名称|
|uname   |String|创建者姓名|
|sn      |String|班号    |
|school  |String|学校名称|
|province|String|省份    |
|city    |String|市    |
|district|String|区    |
|face    |String|班级头像|
