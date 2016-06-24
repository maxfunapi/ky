# 使用优惠券
```
	该接口用于核销优惠券
```
## URL
```	
   {BASE_URL}/services/tp/use_coupon
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
		"coupon_no": "ezyCgOsRtnMZ"
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
            <td>coupon_no</td>
            <td>字符型</td>
            <td>优惠券唯一标示</td>
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
	"result": true
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
            <td>布尔型</td>
            <td>true为成功，false为失败或该优惠券已经被使用</td>
        </tr>
    </thead>
<table>
