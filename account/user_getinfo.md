## 获取用户信息

####1.基本信息
- 接口地址：{API_URL}/user/getinfo  
- 请求方式：POST


####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |--------   |
| uid       | 是        | 用户ID    |
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|


####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":｛
		"uid":123,
		"phone":"12345678901",
		"type":1,
		"name":"张三",
		"face":"",
		"token":"f88205a4eb1c15339158156380579dd1"
	｝
}
```

|键    |类型  |说明  |
|------|------|------|
|status|int   |获取结果<br>1 成功<br>0 失败|
|msg   |String|结果信息描述|
|uid   |int   |用户ID|
|phone |String|用户手机号|
|type  |int   |用户类型<br>1 教师（需要后台审核）<br>2 家长|
|name  |String|用户名|
|face  |String|用户头像（默认为空，按显示默认头像）|
|token |String|用户令牌（校验用户登录状态的有效性）|
