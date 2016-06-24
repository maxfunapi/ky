# 满乐卡-接口文档 @ ky 
<html>
  <table>
    <tr>
      <td>版本</td>
      <td>操纵人</td>
      <td>描述</td>
      <td>操作时间</td>
    </tr>
    <tr>
      <td>1.0</td>
      <td>Ethan</td>
      <td>创建文档</td>
      <td>2015-12-17</td>
    </tr>
    <tr>
      <td>2.0</td>
      <td>Ethan</td>
      <td>加入微信openId支持，加入积分优惠券的在线核销</td>
      <td>2016-02-26</td>
    </tr>
    <tr>
      <td>2.1</td>
      <td>Ethan</td>
      <td>增加通过(手机号码/微信)获取用户当前积分</td>
      <td>2016-03-14</td>
    </tr>
    <tr>
      <td>2.2</td>
      <td>Ethan</td>
      <td>增加取消消费接口</td>
      <td>2016-03-16</td>
    </tr>
    <tr>
      <td>2.3</td>
      <td>Kevin</td>
      <td>增加创建商户接口</td>
      <td>2016-05-11</td>
    </tr>
    <tr>
      <td>2.4</td>
      <td>Kevin</td>
      <td>修改登录获取token接口，增加返回嵌入页面使用的token</td>
      <td>2016-05-11</td>
    </tr>
    <tr>
      <td>2.5</td>
      <td>Ethan</td>
      <td>加了生成环境url，和demo的链接</td>
      <td>2016-05-18</td>
    </tr>
    <tr>
      <td>2.6</td>
      <td>Kevin</td>
      <td>消费接口增加wm_platform字段</td>
      <td>2016-06-23</td>
    </tr>
  </table>
</html>

### API访问URL
   
  * 测试环境： https://demo.maxfun.co/
  * 正式环境： http://api.maxfun.co/

###  Header token格式
  * Authorization: bearer {access_token}
  * 关于身份认证：登录接口会返回一个access token，在调用其他接口时必须把token放在header里面，不传token会报错。
  
### 接口说明
  * [登录获取token](https://github.com/maxfunapi/ky/blob/master/oauth.md)
  * [消费（电话号码](https://github.com/maxfunapi/ky/blob/master/get_access_token.md)
  * [消费（微信ID）](https://github.com/maxfunapi/ky/blob/master/syn_transaction.md)
  * [创建用户（电话号码）](https://github.com/maxfunapi/ky/blob/master/import_history.md)
  * [创建用户（微信）](https://github.com/maxfunapi/ky/blob/master/page_embed.md)
  * [获取最合适的优惠券（电话号码）](https://github.com/maxfunapi/ky/blob/master/calculate_data.md)
  * [获取最合适的优惠券（微信ID）](https://github.com/maxfunapi/ky/blob/master/calculate_data.md)
  * [使用优惠券](https://github.com/maxfunapi/ky/blob/master/calculate_data.md)
  * [获取用户当前积分（电话号码）](https://github.com/maxfunapi/ky/blob/master/calculate_data.md)
  * [获取用户当前积分（微信）](https://github.com/maxfunapi/ky/blob/master/calculate_data.md)
  * [取消消费接口](https://github.com/maxfunapi/ky/blob/master/calculate_data.md)
  * [创建商户接口](https://github.com/maxfunapi/ky/blob/master/calculate_data.md)
  * [页面嵌入](https://github.com/maxfunapi/ky/blob/master/calculate_data.md)


