# 页面嵌入
```
	我们会提供一系列页面，让第三方商能方便的把这些页面嵌入到自己系统中，无缝衔接。
```
# 移动端
```
	测试环境:http://qa.maxfun.co/mobile?page={page}&token={token}&style={style}
	正式:https://tp.maxfun.co/mobile?page={page}&token={token}&style={style}
```
# PC端：
```
	测试环境:http://qa.maxfun.co/pc?page={page}&token={token}&style={style}
	正式:https://tp.maxfun.co/pc?page={page}&token={token}&style={style}
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
            <td>page</td>
            <td>数字型</td>
            <td>需要嵌入的页面，1表示数据魔方，2表示满乐智能</td>
            <td>是</td>
        </tr>
		<tr>
            <td>token</td>
            <td>字符型</td>
            <td>店铺身份标识，通过oauth接口获取</td>
            <td>是</td>
        </tr>
		<tr>
            <td>style</td>
            <td>数字型</td>
            <td>页面样式风格，默认为1 （现在暂时仅支持1，稍后会增加更多）</td>
            <td>否</td>
        </tr>
    </thead>
<table>

# Demo展示

* 移动端数据魔方https://tp.maxfun.co/mobile?style=1&page=1&token=123456

<img src="http://7xlef9.com1.z0.glb.clouddn.com/api/mobile.png"></img>
 
* PC端数据魔方 https://tp.maxfun.co/pc?style=1&page=1&token=123456
 
<img src="http://7xlef9.com1.z0.glb.clouddn.com/api/pc.png"></img>
