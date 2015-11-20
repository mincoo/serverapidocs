##班级成员列表及详细信息（老师）
返回班级全部的老师信息。

####1.基本信息
- 接口地址：{API_URL}/group/tuserlist 
- 请求方式：POST


####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |--------   |
| uid       | 是        | 用户ID    |
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|
| gid       | 是        | 群组ID    |

####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":{
		"size":10,
		"list":[
			{
				"tid":126,
				"tname":"张三",
				"tface":"",
				"phone":"15210253368",
				"ssize":10,
				"slist":[
					{
						"sid":321,
						"sname":"张四",
						"sface":""
					},
					...
				]
			},
			...
		]
	}
}
```

|键      |类型  |说明  |
|--------|------|------|
|status  |int   |搜索结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|
|size    |int   |列表大小（老师）|
|tid     |int   |用户ID（老师）  |
|tname   |String|名称（老师）    |
|tface   |String|用户头像（老师）|
|phone   |String|用户手机（老师）|
|ssize   |int   |关注的学生列表大小|
|sid     |int   |关注的学生ID    |
|sname   |String|关注的学生名称    |
|sface   |String|关注的学生用户头像|
