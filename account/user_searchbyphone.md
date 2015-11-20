## 根据手机号搜索用户

####1.基本信息
- 接口地址：{API_URL}/user/searchbyphone  
- 请求方式：POST


####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |--------   |
| uid       | 是        | 用户ID    |
| phone     | 是        | 用户手机号|
| type      | 是        | 用户类型<br>1 教师<br>2 家长|
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|

####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":｛
		"uid":123,
		"type":1,
		"name":"张三",
		"face":"",
	｝
}
```

|键    |类型  |说明  |
|------|------|------|
|status|int   |搜索结果<br>1 成功<br>0 失败|
|msg   |String|结果信息描述|
|uid   |int   |用户ID|
|type  |int   |用户类型<br>1 教师（需要后台审核）<br>2 家长|
|name  |String|用户名|
|face  |String|用户头像（默认为空，按显示默认头像）|
