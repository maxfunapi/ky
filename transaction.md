# 消费（电话号码）
```
	该接口用于客户消费或者加积分时使用
```
## URL
```	
   {BASE_URL}/services/tp/transaction
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
		"phone_number": "17665992093",
		"open_id": "xxxxxxxxxxxxxxxxxxxxxxxx",
		"points": 1,
		"message_flag": false,
		 "reward_points":10,
		 "price":36.0,
		"wm_platform":"百度外卖",
		 "product_list": [{
			"product_id": 1,
			"product_name": "鱼香茄子",
			"amount": 1,
			"unit_price": 12.0
		 },{
			"product_id": 2,
			"product_name": "肉末麻婆豆腐",
			"amount": 2,
			"unit_price": 12.0
		 }],
		  "coupon_no_list":["obdI5eLX360p","T3BpfbRNoPje"]
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
            <td>如果传入的电话号码不存在，后台会以该电话号码创建一个新的会员账号</td>
            <td>是</td>
        </tr>
		<tr>
            <td>points</td>
            <td>字符型</td>
            <td></td>
            <td>是</td>
        </tr>
		<tr>
            <td>message_flag</td>
            <td>字符型</td>
            <td>当为true，积分成功后会给该用户推送一条积分通知信息；false则不会</td>
            <td>是</td>
        </tr>
		<tr>
            <td>reward_points</td>
            <td>数字型</td>
            <td>使用积分抵扣金额</td>
            <td>否</td>
        </tr>
		<tr>
            <td>price</td>
            <td>数字型</td>
            <td>订单总金额</td>
            <td>否</td>
        </tr>
		<tr>
            <td>open_id</td>
            <td>字符型</td>
            <td>微信公众号openid</td>
            <td>否</td>
        </tr>
		<tr>
            <td>wm_platform</td>
            <td>字符型</td>
            <td>外卖平台名称， 百度外卖、美团外卖...，请保持各外卖平台名称统一。</td>
            <td>否</td>
        </tr>
		<tr>
            <td>product_list</td>
            <td>数组</td>
            <td>购买菜品明细列表</td>
            <td>是</td>
        </tr>
		<tr>
            <td>coupon_no_list</td>
            <td>数组</td>
            <td>优惠券编号列表</td>
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
			"duration": 20332
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
            <td>数字型</td>
            <td>返回新创建的记录的的ID，调用方应该保存该ID以便以后的数据对比时使用</td>
        </tr>
    </thead>
<table>
