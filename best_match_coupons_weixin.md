# 计算优惠券最佳方案（微信openid方式）
```
	该接口用于计算用户消费后使用已有优惠券的最佳方案，暂时只能使用一张优惠券
```
## URL
```	
   {BASE_URL}/services/tp/best_match_coupons_weixin
```
## Method
```	
   GET
```
## Headers
```
   authorization=bearer {access_token}
```

## Request
```
	 {BASE_URL}/services/tp/best_match_coupons_weixin?open_id=openid&purchase_amount=100
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
            <td>open_id</td>
            <td>字符型</td>
            <td>用户微信的openid</td>
            <td>是</td>
        </tr>
		<tr>
            <td>purchase_amount</td>
            <td>浮点型</td>
            <td>用户消费金额</td>
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
       "coupon_list": [
            {
                "rule": "满100元可使用",
                "coupon_no": "8fjtjW3hJvwE",
                "coupon_name": "折扣券",
                "coupon_amt": 5,
                "expiration_time_str": "2016-03-05 18:00:47",
                "min_buy_price": 100,
                "coupon_id": 246,
                "coupon_type": 1
            }
        ],
        "after_amount": 60,
        "before_amount": 120
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
            <td>实际返回内容</td>
        </tr>
		<tr>
            <td>coupon_list</td>
            <td>数组型</td>
            <td>用户可用优惠券记录的数组</td>
        </tr>
		<tr>
            <td>rule</td>
            <td>字符型</td>
            <td>优惠券规则</td>
        </tr>
		<tr>
            <td>coupon_no</td>
            <td>字符型</td>
            <td>优惠券唯一标示</td>
        </tr>
		<tr>
            <td>coupon_name</td>
            <td>字符型</td>
            <td>优惠券名称</td>
        </tr>
		<tr>
            <td>coupon_amt</td>
            <td>数字型</td>
            <td>该券减免的金额，如果是现金券则为减多少元，如果为折扣券则为多少折（8折则为8）</td>
        </tr>
		<tr>
            <td>expiration_time_str</td>
            <td>字符型</td>
            <td>过期时间</td>
        </tr>
		<tr>
            <td>min_buy_price</td>
            <td>数字型</td>
            <td>优惠券的使用限制，消费多少元可用，0为无限制</td>
        </tr>
		<tr>
            <td>coupon_id</td>
            <td>数字型</td>
            <td>优惠券的ID</td>
        </tr>
		<tr>
            <td>coupon_type</td>
            <td>数字型</td>
            <td>优惠券类型，0为现金券，1为折扣券，2为特殊券</td>
        </tr>
		<tr>
            <td>after_amount</td>
            <td>数字型</td>
            <td>使用优惠券后的金额</td>
        </tr>
		<tr>
            <td>before_amount</td>
            <td>数字型</td>
            <td>使用优惠券前的金额</td>
        </tr>
    </thead>
<table>
