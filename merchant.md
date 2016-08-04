# 创建商户接口
```
	该接口用于创建商户接口
```
## URL
```	
   {BASE_URL}/services/tp/merchant
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
		"merchant_id": "10087",
		"merchant_name": "麻辣烫",
		"password":"123456",
		"login_name":"alipptest2",
		"merchant_group_id":246
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
            <td>merchant_id</td>
            <td>字符型</td>
            <td>商户ID</td>
            <td>是</td>
        </tr>
		<tr>
            <td>merchant_name</td>
            <td>字符型</td>
            <td>商户名称</td>
            <td>是</td>
        </tr>
	<tr>
            <td>password</td>
            <td>字符型</td>
            <td>密码</td>
            <td>是</td>
        </tr>
		<tr>
            <td>login_name</td>
            <td>字符型</td>
            <td>登录名</td>
            <td>是</td>
        </tr>
		<tr>
            <td>contact_number</td>
            <td>字符型</td>
            <td>联系电话</td>
            <td>否</td>
        </tr>
		<tr>
            <td>merchant_group_id</td>
            <td>字符型</td>
            <td>merchant_group_id为空即新建一个新group</td>
            <td>否</td>
        </tr>
		<tr>
            <td>create_time</td>
            <td>字符型</td>
            <td>商户创建时间 格式为yyyy-MM-dd HH:mm:ss</td>
            <td>否</td>
        </tr>
        	<tr>
            <td>merchant_address</td>
            <td>字符型</td>
            <td>地址</td>
            <td>否</td>
        </tr>
	<tr>
            <td>merchant_city</td>
            <td>字符型</td>
            <td>城市</td>
            <td>否</td>
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
	"result":"success"
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
            <td>字符型</td>
            <td>状态描述or success</td>
        </tr>
    </thead>
<table>
