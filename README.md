# LLS-API

## 请求地址:

>https://app.lovelivesupport.com/lls-api/getAll.php

>https://app.llsupport.cn/lls-api/getAll.php

### 调用方式：HTTP GET

### 接口描述：

接口描述详情:

### 请求参数:

|字段名称       |字段说明         |类型            |必填            |字段选项        |
| -------------|:--------------:|:--------------:|:--------------:|:------:|
|type|请求类型|string|Y|card / live / event / maps / pair_card / c_card / card_s|

* 当type为card时，请求卡片有关信息:

	|字段名称       |字段说明         |类型            |必填            |字段选项        |
	| -------------|:--------------:|:--------------:|:--------------:|:------:|
	|id|编号|string|Y|0 / {unit_number}|
	|page|id=0时，page必填|string|Y|all / {page}|


###  请求返回结果:

```

```


