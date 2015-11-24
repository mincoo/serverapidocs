##消息推送状态切换

####1.基本信息
- 接口地址：`{API_URL}/msg/tagchange`
- 请求方式：POST

####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |-----------|
| uid       | 是        | 用户ID    |
| token     | 是        | 用户令牌  |
| sign      | 是        | 数据校验码|
| gid       | 是        | 群组ID    |
| status    | 是        | 消息推送的解除/恢复状态<br>0：请求恢复推送<br>1：请求解除推送 |

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
|status  |int   |状态切换结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|