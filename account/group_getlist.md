##获取用户的班级列表及详细信息
获取用户的班级列表，包括自己创建的和自己加入的。

####1.基本信息
- 接口地址：`{API_URL}/group/getlist` 
- 请求方式：POST


####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |--------   |
| uid       | 是        | 用户ID    |
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|
| start     | 是        | 开始ID（默认值0）    |

####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":{
		"size":10,
		"last":10,		
		"list":[
			{
				"gid":615,
				"uid":123,
				"name":"六年级英语5班"
				"sn":2046,
				"school":"人大一中",
				"province":"北京",
				"city":"北京市",
				" district":"海淀区",
				" tnum":"5",
				" snum":"50",
				" pnum":"80",
				"face":""
				"jpushflg":”0”
			},
			...
		]
	}
}
```

|键    |类型  |说明  |
|--------|------|------|
|status  |int   |获取结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|
|last    |int   |本页最后ID（用于分页start参数）|
|size    |int   |列表大小|
|gid     |int   |群组ID|
|uid     |int   |创建者ID|
|name    |String|群组名称|
|sn      |String|班号    |
|school  |String|学校名称|
|province|String|省份    |
|city    |String|市    |
|district|String|区    |
|tnum    |int   |老师数|
|snum    |int   |学生数|
|pnum    |int   |家长数|
|jpushflg|int   |消息推送flg<br>0：推送<br>1：不推送|
|face    |String|班级头像|
