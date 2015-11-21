##版本信息

####1.基本信息
- 接口地址：`{API_URL}/version`
- 请求方式：POST

####2.参数信息  

| 参数名    | 必填      | 说明      |
| -------   |:-------:  |-----------|
| ostype    | 是        | 系统类型<br>1:android<br>2:ios  |
| sign      | 是        | 数据校验码|

####3.报文响应

```
{
	"status":1,
	"msg":"success",
	"data":{
		"version":1.0.0,
		"name":易名校信1.0.0,
		"url":"http://xxxx/xxxx",
		"ostype":1,
		"date":"2015-03-27 11:38"
	}
}
```

|键      |类型  |说明  |
|--------|------|------|
|status  |int   |获取结果<br>1 成功<br>0 失败|
|msg     |String|结果信息描述|
|version |String|当前版本号|
|name    |String|App名称|
|URL     |String|App下载地址|
|Ostype  |int   |系统类型<br>1:android<br>2:ios|
|date    |String|更新时间|
