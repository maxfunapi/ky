# 创建用户（电话号码）
```
	该接口用于创建用户
```
## URL
```	
   {BASE_URL}/services/tp/customer
```
## Method
```	
   POST
```
## Headers
```
   content-type=application/json
   authorization=bearer {access_token}
```

## Request
```
	{
		"phone_number": "13512345678",
		"name": "测试",
		"birthday": "1990-11-06",
		"gender" : "male",
		"email" :"zhangsan@maxfun.co"
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
            <td>phone_number</td>
            <td>字符型</td>
            <td>手机号码</td>
            <td>是</td>
        </tr>
		<tr>
            <td>password</td>
            <td>字符型</td>
            <td>密码</td>
            <td>是</td>
        </tr>
		<tr>
            <td>name</td>
            <td>字符型</td>
            <td>用户昵称</td>
            <td>否</td>
        </tr>
		<tr>
            <td>birthday</td>
            <td>字符型</td>
            <td>生日，格式:2016-01-01</td>
            <td>否</td>
        </tr>
		<tr>
            <td>gender</td>
            <td>字符型</td>
            <td>性别, 只能填male或者female</td>
            <td>否</td>
        </tr>
		<tr>
            <td>email </td>
            <td>字符型</td>
            <td>邮箱</td>
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
	"result": 134206
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
            <td>返回新创建的用户的ID，调用方应该保存该ID以便以后的数据对比时使用</td>
        </tr>
	
    </thead>
<table>
