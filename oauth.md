# 登录
```
	用于商户登录，并获取访问其他接口使用的token，在调用其他接口时都必须先获取token
```
## URL
```	
   {BASE_URL}/services/tp/oauth
```
## Method
```	
   POST
```
## Headers
```
   content-type=application/json
```

## Request
```
	{
		"username": "abc",
		"password": "1234567",
		"source":"kuanyi"
	}
```
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
<table data-tablesaw-sortable>
    <thead>
        <tr>
            <th data-tablesaw-sortable-col data-tablesaw-sortable-default-col>字段名称</th>
            <th data-tablesaw-sortable-col>类型</th>
            <th data-tablesaw-sortable-col>描述</th>
        </tr>
		<tr>
            <td>status</td>
            <td></td>
            <td>请求返回的状态，所以得返回值都会有这个字段。如果有错误，code将是非200</td>
        </tr>
		<tr>
            <td>code</td>
            <td>数字型</td>
            <td>Code为200表示成功，其他为错误</td>
        </tr>
		<tr>
            <td>result</td>
            <td></td>
            <td>返回的实际内容</td>
        </tr>
		<tr>
            <td>enterprise_name</td>
            <td>字符型</td>
            <td>商户的名称</td>
        </tr>
		<tr>
            <td>access_token</td>
            <td>字符型</td>
            <td>登录的token，该token在所有的非登录接口中都要使用，作为身份认证</td>
        </tr>
		<tr>
            <td>tp_access_token</td>
            <td>字符型</td>
            <td>嵌入页面使用的token</td>
        </tr>
    </thead>
<table>
