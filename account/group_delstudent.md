##删除成员（学生）
创建者将学生踢出班级。

####1.基本信息
- 接口地址：`{API_URL}/group/delstudent` 
- 请求方式：POST


####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |-----------|
| uid       | 是        | 用户ID    |
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|
| gid       | 是        | 群组ID    |
| nid       | 是        | 删除的学生ID  |

####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":
}
```

|键      |类型  |说明  |
|--------|------|------|
|status  |int   |删除结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|
