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

	id={unit_number} 返回一张卡的详细信息

	请求返回结果:
	```
	[{
		"assets_base_url":"https:\/\/card.lovelivesupport.com",
		"card_info":{
			"unit_id":"1287", //内部编号
			"unit_number":"1273", //卡号
			"unit_type_id":"101", //卡片类型编号
			"eponym":"\u304a\u3044\u3067\u307e\u305b\u6d77\u306e\u5bb6\uff01", //卡名
			"name":"\u9ad8\u6d77\u5343\u6b4c", //卡片角色名
			"normal_card_id":"5047", //普通卡片号
			"rank_max_card_id":"5048", //觉醒卡片号
			"normal_icon_asset":"assets\/image\/units\/u_normal_icon_41101003.png", //普通头像路径
			"rank_max_icon_asset":"assets\/image\/units\/u_rankup_icon_41101003.png", //觉醒头像路径
			"normal_unit_navi_asset_id":"2356",	//普通无框编号
			"rank_max_unit_navi_asset_id":"2357", //觉醒无框编号
			"rarity":"4", //稀有度
			"attribute_id":"1",	//颜色属性
			"default_unit_skill_id":"731", //默认技能编号
			"skill_asset_voice_id":"6958", //默认技能发动音编号
			"default_leader_skill_id":"64", //默认C位技能编号
			"before_love_max":"500", //普通满绊
			"after_love_max":"1000", //觉醒满绊
			"before_level_max":"80", //普通等级
			"after_level_max":"100", //觉醒等级
			"default_removable_skill_capacity":"4", //普通宝石槽
			"max_removable_skill_capacity":"8", //举行宝石槽
			"disable_rank_up":"0", //是否可升级
			"unit_level_up_pattern_id":"25", 
			"hp_max":"6", //最大生命值
			"smile_max":"5340", //最大Smile值
			"pure_max":"4500", //最大Pure值
			"cool_max":"4070", //最大Cool值
			"rank_up_cost":"45000", //觉醒消耗
			"exchange_point_rank_up_cost":"450000", //劝退获得
			"release_tag":null,
			"_encryption_release_id":null
		},
		"card_type":{
			"name":"\u9ad8\u6d77\u5343\u6b4c", //卡片角色名
			"background_color":"ffcdb7", //角色背景色
			"age":"2", //角色年龄
			"birthday":"8\u67081\u65e5", //角色生日
			"school":"\u6d66\u306e\u661f\u5973\u5b66\u9662", //角色所属学院
			"hobby":"\u30bd\u30d5\u30c8\u30dc\u30fc\u30eb\u30fb\u30ab\u30e9\u30aa\u30b1", //角色兴趣
			"blood_type":"\uff22\u578b", //角色血腥
			"height":"157", //角色身高
			"three_size":"\uff2282\uff3759\uff2883", //角色三围
			"cv":"\u4f0a\u6ce2\u674f\u6a39" //角色声优
		},
		"default_skill":{
			"name":"\u304a\u3044\u3067\u307e\u305b\u6d77\u306e\u5bb6\uff01", //默认技能名
			"unit_skill_id":"731"
		},
		"default_skill_des":{
			"description":"\u30ea\u30ba\u30e0\u30a2\u30a4\u30b3\u30f328\u500b\u3054\u3068\u306b75%\u306e\u78ba\u7387\u3067\u5224\u5b9a\u304c9\u79d2\u5f37\u5316\u3055\u308c\u308b" //默认技能表述
		},
		"center_skill":{
			"name":"\u30b9\u30de\u30a4\u30eb\u30d7\u30ea\u30f3\u30bb\u30b9", //C位技能名
			"description":"\u30b9\u30de\u30a4\u30ebP\u304c9%UP\u3059\u308b", //C位技能描述
			"unit_leader_skill_id":"64"
		},
		"card_nor_navi":{
			"unit_navi_asset":"assets\/image\/units\/u_normal_navi_41101003.png" //普通立绘路径
		},
		"card_max_navi":{
			"unit_navi_asset":"assets\/image\/units\/u_rankup_navi_41101003.png" //觉醒立绘路径
		},
		"card_base_nor":{
			"flash_asset":"assets\/image\/units\/b_normal_41101003.png" //普通无框图路径
		},
		"card_base_max":{
			"flash_asset":"assets\/image\/units\/b_rankup_41101003.png" //觉醒无框图路径
		},
		"card_frame_position":{ //卡片定位
			"nor":{
				"unit_navi_asset_id":"2356", 
				"navi_layer_order":"0",
				"navi_rotation":"0",
				"navi_move_x":"-180",
				"navi_move_y":"-142",
				"navi_size_ratio":"0.9"
			},
			"max":{
				"unit_navi_asset_id":"2357",
				"navi_layer_order":"0",
				"navi_rotation":"0",
				"navi_move_x":"-180",
				"navi_move_y":"-142",
				"navi_size_ratio":"0.9"
			}
		},
		"chack_db":{ //检测其他语言是否含有相同卡片
			"jp":{"unit_id":"1287","unit_number":"1273","name":"\u9ad8\u6d77\u5343\u6b4c","eponym":"\u304a\u3044\u3067\u307e\u305b\u6d77\u306e\u5bb6\uff01"},
			"cn":false,
			"en":false,
			"kr":false,
			"tw":false
		}
	}]

	```


