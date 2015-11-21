##信息阅读状态

####1.基本信息
- 接口地址：`{API_URL}/msg/readstate`
- 请求方式：POST

####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |-----------|
| uid       | 是        | 用户ID    |
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|
| mid       | 是        | 消息ID    |

####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":[
		{
			"uid":123,
			"type":1,
			"name":"张三",
			"face":"",
			"readTime":"2015-03-04 9:10",
			"status":1
		},
		...
	]
}
```

|键      |类型  |说明  |
|--------|------|------|
|status  |int   |获取结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|
|uid     |int   |用户id|
|type    |int   |用户类型<br>1 老师<br>2 家长|
|name    |String|用户名称|
|face    |String|用户头像|
|readTime|String|阅读时间|
|status  |int   |阅读状态<br>1 未读<br>2 已读|
