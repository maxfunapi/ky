# 登录

用于商户登录，并获取访问其他接口使用的token，在调用其他接口时都必须先获取token

## URL
   {BASE_URL}/services/tp/oauth

## Method
   POST

## Headers
```
   content-type=application/json
```

## Request
<table data-tablesaw-sortable>
    <thead>
        <tr>
            <th data-tablesaw-sortable-col data-tablesaw-sortable-default-col>字段名称</th>
            <th data-tablesaw-sortable-col>类型</th>
            <th data-tablesaw-sortable-col>描述</th>
            <th data-tablesaw-sortable-col>是否必填</th>
        </tr>
		<tr>
            <td>username</td>
            <td>字符型</td>
            <td>商户登录名称</td>
            <td>是</td>
        </tr>
		<tr>
            <td>password</td>
            <td>字符型</td>
            <td>密码</td>
            <td>是</td>
        </tr>
		<tr>
            <td>source</td>
            <td>字符型</td>
            <td>登录请求来源，如“kuanyi”</td>
            <td>是</td>
        </tr>
    </thead>
<table>

{
	"username": "abc",
	"password": "1234567",
	"source":"kuanyi"
}

## Response
```
{
	"status": {
		"code": "200",
		"message": "success",
		"errors": [],
		"debug": {
			"build": "1.0",
			"serverName": "ethan-PC",
			"duration": 180
		}
	},
	"result": {
		"enterprise_name": "满乐测试",
		"access_token": "cc6d1a21-2bcc-462e-9e04-06b7352cae83",
		"tp_access_token": "0ce7891c-d2e8-4714-b8e4-0a9e4f65215b"
	}
}
```
