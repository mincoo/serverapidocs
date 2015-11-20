##消息内容

####1.基本信息
- 接口地址：{API_URL}/msg/getdata
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
	"data":{
		"mid":123,
		"type":1,
		"url":"",
		"title":"上午9点半在逸夫楼502上课",
		"content":"今天上午9点半，在逸夫楼502大教室上课，不要迟到。",
		"gname":"六年级英语5班",
		"uname":"张老师",
		"sender":"六年级英语5班",
		"stime":"2015-03-04 9:10",
		"status":2,
	}
}
```

|键      |类型  |说明  |
|--------|------|------|
|status  |int   |搜索结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|
|last    |int   |本页最后ID（用于分页start参数）|
|mid     |int   |消息ID|
|type    |int   |消息类型<br>1 文本<br>2 链接|
|url     |String|消息URL|
|title   |String|消息标题|
|content |String|消息内容|
|gname   |String|群组名|
|uname   |String|用户名|
|sender  |String|发送者（群组名或用户名）|
|stime   |String|发送时间|
|status  |int   |消息状态<br>1 未读<br>2 已读|
