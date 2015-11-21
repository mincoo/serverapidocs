##班级成员列表及详细信息（学生）
返回班级全部的学生信息。

####1.基本信息
- 接口地址：`{API_URL}/group/suserlist` 
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
				"sid":126,
				"sname":"张三",
				"sface":""
				"num":"2015445"
				"psize":10,
				"plist":[
					{
						"pid":321,
						"pname":"张四",
						"pface":""
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
|size    |int   |列表大小（学生）|
|sid     |int   |用户ID（学生）  |
|sname   |String|名称（学生）    |
|sface   |String|用户头像（学生）|
|num     |String|学生学号        |
|psize   |int   |学生的家长列表大小|
|pid     |int   |学生的家长ID    |
|pname   |String|学生的家长名称  |
|pface   |String|学生的家长头像  |
