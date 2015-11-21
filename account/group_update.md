##修改群组信息

####1.基本信息
- 接口地址：`{API_URL}/group/update` 
- 请求方式：POST


####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |--------   |
| uid       | 是        | 用户ID    |
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|
| gid       | 是        | 群组ID|
| name      | 否        | 群组名称|
| school    | 否        | 学校名称|
| province  | 否        | 省|
| city      | 否        | 市|
| district  | 否        | 区|
| longitude | 否        | 经度|
| latitude  | 否        | 纬度|
| face      | 否        | 班级头像|

####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":{
		"gid":615,
		"uid":123,
		"name":"六年级英语5班",
		"sn":2046,
		"school":"人大二中",
		"province":"北京",
		"city":"北京市",
		"district":"海淀区",
		"face":"",
		"createDt":"2015-01-01 18:00"
	}
}
```

|键      |类型  |说明  |
|--------|------|------|
|status  |int   |修改结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|
|gid     |int   |群组ID|
|uid     |int   |创建者ID|
|name    |String|群组名称|
|sn      |String|班号    |
|school  |String|学校名称|
|province|String|省份    |
|city    |String|市    |
|district|String|区    |
|face    |String|班级头像|
|created |String|创建时间|
