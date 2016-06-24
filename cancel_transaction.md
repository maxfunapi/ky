# 取消消费接口
```
	该接口用于取消消费接口
```
## URL
```	
   {BASE_URL}/services/tp/cancel_transaction
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
		"transaction_id":205276
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
            <td>transaction_id</td>
            <td>数字型</td>
            <td>消费记录ID</td>
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
        "status": "success",
        "msg": "success"
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
            <td>返回内容</td>
        </tr>
		<tr>
            <td>status</td>
            <td>字符型</td>
            <td>状态描述error success</td>
        </tr>
		<tr>
            <td>msg</td>
            <td>字符型</td>
            <td>消息描述</td>
        </tr>
    </thead>
<table>
