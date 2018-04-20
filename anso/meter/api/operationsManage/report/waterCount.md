### 表务管理→水量统计→综合统计接口【GET/operationsManagement/waterCount/generalCount】

请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 | 
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

JSON实例：

```json
{
	"code": 0,
	"message": "SUCC",
	"data": [{
		"meterBrand": "拓安信",
		"meterDiameter": "DN50",
		"outputMode": "GPRS远传",
		"meterTotal": 15,
		"waterTotal": 3453,
		"meterModel": "测试"
	}]
}
```
响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| meterBrand | String   |水表品牌|
| meterDiameter | String   |口径|
| outputMode | String   |输出方式|
| MeterTotal   | int   |表量小计|
| WaterTotal   | int   |水量小计|
| meterModel   | String   |表型|


### 表务管理→水量统计→大表总览表→口径分布接口【GET/operationsManagement/waterCount/meterDiameterDistribution】

请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 | 
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

JSON实例：

```json
{
	"code": 0,
	"message": "SUCC",
	"data": [{
		"name": "DN50",
		"value": 69363
	}, {
		"name": "DN80",
		"value": 97657
	}, {
		"name": "DN100",
		"value": 47490
	}]
}
```
响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| name | String   |口径名称|
| value | int   |口径分布值|

### 表务管理→水量统计→大表总览表→厂家分布接口【GET/operationsManagement/waterCount/factoryDistribution】

请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 | 
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

JSON实例：

```json
{
	"code": 0,
	"message": "SUCC",
	"data": [{
		"name": "拓安信",
		"value": 69363
	}, {
		"name": "西门子",
		"value": 47490
	}]
}
```
响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| name | String   |厂家名称|
| value | int   |厂家分布值|

### 表务管理→水量统计→大表总览表→使用年限接口【GET/operationsManagement/waterCount/usefullLife】

请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 | 
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

JSON实例：

```json
{
	"code": 0,
	"message": "SUCC",
	"data": [{
		"name": "一年",
		"value": 69363
	}, {
		"name": "两年",
		"value": 47490
	}, {
		"name": "三年",
		"value": 27490
	}, {
		"name": "六年",
		"value": 11490
	}]
}
```
响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| name | String   |使用年限|
| value | int   |使用年限值|

### 表务管理→水量统计→大表总览表→表型分布接口【GET/operationsManagement/waterCount/meterModelDistribution】

请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 | 
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

JSON实例：

```json
{
	"code": 0,
	"message": "SUCC",
	"data": [{
		"name": "远程系列",
		"value": 69363
	}, {
		"name": "485系列",
		"value": 47490
	}, {
		"name": "xxx系列",
		"value": 95656
	}]
}
```
响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| name | String   |表型名称|
| value | int   |表型分布值|