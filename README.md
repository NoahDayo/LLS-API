# LLS-API

### 请求地址:

>https://app.lovelivesupport.com/lls-api/getAll.php

>https://app.llsupport.cn/lls-api/getAll.php

### 调用方式：
	
	HTTP GET

### 接口描述：

	LLSupport提供的开放性数据接口
	本API服务站点为公益性质运营方式，如果使用请参照一下文档并注明数据来源LLSupport

	注: 本站采用全域https方式加密 对于加密协议等详细信息访问SSLLabs查询
	.cn 为中国大陆地区内访问专线，针对中国大陆有较强的访问速度
	.com 为国际专用线路，为非中国大陆地区内有极好的访问速度



### 请求参数:

|字段名称       |字段说明         |类型            |必填            |字段选项        |
| -------------|:--------------:|:--------------:|:--------------:|:------:|
|type|请求类型|string|必填|card / live / event / maps / pair_card / c_card / card_s|

* 当type为card时，请求卡片有关信息:

	|字段名称       |字段说明         |类型            |必填            |字段选项        |
	| -------------|:--------------|:--------------|:--------------|:------|
	|id|编号|string|必填|0 / {unit_number}|
	|page|分页选项|string|id=0时必填|all / {page}|
	|lang|数据语言 默认为日本语|string|可选|jp / en / cn / kr / tw|

	id=0&page=all 返回所有卡片基础信息<br>
	id=0&page=1 一页返回10条信息

	请求返回结果:
	```
	[
		{
			"unit_number":"1273", //卡号
			unit_type_id":"101",  //属性编号
			"name":"\u9ad8\u6d77\u5343\u6b4c", //卡片人员
			"eponym":"\u304a\u3044\u3067\u307e\u305b\u6d77\u306e\u5bb6\uff01", //卡名
			"normal_icon_asset":"assets\/image\/units\/u_normal_icon_41101003.png", //普通头像路径
			"rank_max_icon_asset":"assets\/image\/units\/u_rankup_icon_41101003.png", //觉醒头像路径
			"rarity":"4", //稀有度
			"attribute_id":"1" //颜色属性
		},
		{
			"unit_number":"1272",
			"unit_type_id":"105",
			"eponym":"\u30df\u30e9\u30af\u30eb\u30aa\u30fc\u30b7\u30e3\u30f3",
			"name":"\u6e21\u8fba\u66dc",
			"normal_icon_asset":"assets\/image\/units\/u_normal_icon_52105002.png",
			"rank_max_icon_asset":"assets\/image\/units\/u_rankup_icon_52105002.png",
			"rarity":"5",
			"attribute_id":"2"
		},
		....
	]

	```


