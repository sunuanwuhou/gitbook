### 表务管理→水量统计→大表总览表→口径分布接口

【GET/api/meter/operationsManagement/waterCount/meterDiameterDistribution】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

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
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| name | String   |口径名称|
| value | int   |口径分布值|

### 表务管理→水量统计→大表总览表→厂家分布接口

【GET/api/meter/operationsManagement/waterCount/factoryDistribution】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

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
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| name | String   |厂家名称|
| value | int   |厂家分布值|

### 表务管理→水量统计→大表总览表→使用年限接口

【GET/api/meter/operationsManagement/waterCount/usefullLife】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

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
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| name | String   |使用年限|
| value | int   |使用年限值|

### 表务管理→水量统计→大表总览表→表型分布接口

【GET/api/meter/operationsManagement/waterCount/meterModelDistribution】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

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
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| name | String   |表型名称|
| value | int   |表型分布值|

### 表务管理→水量统计→综合统计接口

【GET/api/meter/operationsManagement/waterCount/generalCount】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

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
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------: | :------: | :----: |
| meterBrand | String   |水表品牌|
| meterDiameter | String   |口径|
| outputMode | String   |输出方式|
| MeterTotal   | int   |表量小计|
| WaterTotal   | int   |水量小计|
| meterModel   | String   |表型|

### 表务管理→安装管理→安装表计总览接口

【GET/api/meter/operationsManagement/install/installOverview】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :--------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": {
        "year": [
            {
                "sort": "1月",
                "applyInstall": 300,
                "completeSceneSurvey": 100,
                "install": 100,
                "qualified": 100,
                "transformChargingSystem": 110
            },
            {
                "sort": "2月",
                "applyInstall": 200,
                "completeSceneSurvey": 70,
                "install": 40,
                "qualified": 50,
                "transformChargingSystem": 60
            }
        ],
        "month": [
            {
                "sort": "1号",
                "applyInstall": 100,
                "completeSceneSurvey": 11,
                "install": 20,
                "qualified": 30,
                "transformChargingSystem": 40
            },
            {
                "sort": "2号",
                "applyInstall": 100,
                "completeSceneSurvey": 10,
                "install": 60,
                "qualified": 80,
                "transformChargingSystem": 19
            },
            {
                "sort": "3号",
                "applyInstall": 100,
                "completeSceneSurvey": 10,
                "install": 60,
                "qualified": 70,
                "transformChargingSystem": 5
            }
        ]
    }
}
```
- 响应：

| 参数名称   | 二级子参数 | 参数类型 |  说明  |
| :---------: | :---------: | :------: | :----: |
| year |  | List |年份数据|
|  | sort | String   |横排名称|
|  | applyInstall | int   |申请安装数|
|  | completeSceneSurvey | int   |完成现场调查数|
|  | install | int   |安装数|
|  | qualified | int   |验收合格数|
|  | transformChargingSystem | int   |转收费系统数|
| month |  | List |月份数据|

### 表务管理→安装管理→安装申请→安装申请录入接口

【POST/api/meter/operationsManagement/install/installApplyEntry】

- 请求：

| 参数名称  | 二级子参数 |   参数类型  |  说明  | 是否必填 |
| :-------: | :-------: | :---------: | :----: |:--------:|
| applyNumber |  | String   |申请单号|    是    |
| createTime   |  | Timestamp   |创建时间|    是    |
| userName |  | String   |用户名|    是    |
| userNumber |  | String   |用户编号|    是    |
| userAddress |  | String   |用户所在地区|    是    |
| userPassport |  | String   |用户证件|    是    |
| userPassportNumber |  | String   |用户证件号码|    是    |
| userPhone |  | String   |用户联系电话|    是    |
| applyPerson |  | String   |申办人|    是    |
| applyPersonPassport |  | String   |申办人证件|    是    |
| applyPersonPassportNumber |  | String   |申办人证件号码|    是    |
| applyPersonPhone |  | String   |申办人联系电话|    是    |
| waterAddress |  | String   |用水地址|    是    |
| waterUnit |  | String   |用水单位|    是    |
| unitBusinessLicense |  | String   |单位营业执照|    是    |
| unitUserIDNnumber |  | String   |单位用户身份证|    是    |
| unitapplyPersonIDNnumber |  | String   |单位申办人身份证|    是    |
| table |  | List   |下面list|    是    |
|  | waterNature | String   |用水性质|    是    |
|  | waterPersonNumber | int   |用水人数|    是    |
|  | waterConsumption | double   |预估月用水量|    是    |
|  | applyMeterDiameter | String   |申请水表口径|    是    |

- JSON请求实例:

```json
{
	"applyNumber": "I-101",
	"createTime": 1523498001452,
	"userName": "用户1",
	"userNumber": "AX101",
	"userAddress": "XXX",
	"userPassport": "身份证",
	"userPassportNumber": "444XXX",
	"userPhone": "10086",
	"applyPerson": "申办人1",
	"applyPersonPassport": "身份证",
	"applyPersonPassportNumber": "44XXXX",
	"applyPersonPhone": "10000",
	"waterAddress": "XXX小区",
	"waterUnit": "XXX单位",
	"unitBusinessLicense": "IOS-1024",
	"unitUserIDNnumber": "44XXXXX",
	"unitapplyPersonIDNnumber": "4XXXXX",
	"table": [{
			"waterNature": "工业",
			"waterPersonNumber": 10,
			"waterConsumption": 20,
			"applyMeterDiameter": "DN100"

		},
		{
			"waterNature": "居民",
			"waterPersonNumber": 10,
			"waterConsumption": 20,
			"applyMeterDiameter": "DN80"
		}
	]
}

```

- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称 | 参数类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据 |
| msg | String | 信息 |

### 表务管理→安装管理→安装申请→安装申请查询接口

【POST/api/meter/operationsManagement/install/installApplyQuery】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------: | :---------: | :----: |:--------:|
| applyNumber | String   |申请单号|    否    |
| createTime   | Timestamp   |创建时间|    否    |
| userName | String   |用户名|    否    |
| userNumber | String   |用户编号|    否    |
| userAddress | String   |用户所在地区|    否    |
| userPassport | String   |用户证件|    否    |
| userPassportNumber | String   |用户证件号码|    否    |
| userPhone | String   |用户联系电话|    否    |
| applyPerson | String   |申办人|    否    |
| applyPersonPhone | String   |申办人联系电话|    否    |
| waterAddress | String   |用水地址|    否    |
| waterUnit | String   |用水单位|    否    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "applyNumber": "IOS-101",
            "createTime": 1523515257788,
            "userName": "用户1",
            "userNumber": "AX123",
            "userAddress": "深圳",
            "userPassport": "身份证",
            "userPassportNumber": "44xxxx",
            "userPhone": "10086",
            "applyPerson": "申办人1",
            "applyPersonPassport": "身份证",
            "applyPersonPassportNumber": "44xx",
            "applyPersonPhone": "10000",
            "waterAddress": "xxxx栋",
            "waterUnit": "xxx造纸厂",
            "unitBusinessLicense": "kk123",
            "unitUserIDNnumber": "44xxx",
            "unitapplyPersonIDNnumber": "66xxx",
            "table": [
                {
                    "waterNature": "工业",
                    "waterPersonNumber": 10,
                    "waterConsumption": 20,
                    "applyMeterDiameter": "DN100"
                },
                {
                    "waterNature": "居民",
                    "waterPersonNumber": 10,
                    "waterConsumption": 20,
                    "applyMeterDiameter": "DN80"
                }
            ]
        }
    ]
}
```

- 响应：

| 参数名称 | 二级子参数 | 参数类型 |  说明  |
| :--------: | :--------: | :------: | :----: |
| applyNumber |  | String   |申请单号|
| createTime   |  | Timestamp   |创建时间|
| userName |  | String   |用户名|
| userNumber |  | String   |用户编号|
| userAddress |  | String   |用户所在地区|
| userPassport |  | String   |用户证件|
| userPassportNumber |  | String   |用户证件号码|
| userPhone |  | String   |用户联系电话|
| applyPerson |  | String   |申办人|
| applyPersonPassport |  | String   |申办人证件|
| applyPersonPassportNumber |  | String   |申办人证件号码|
| applyPersonPhone |  | String   |申办人联系电话|
| waterAddress |  | String   |用水地址|
| waterUnit |  | String   |用水单位|
| unitBusinessLicense |  | String   |单位营业执照|
| unitUserIDNnumber |  | String   |单位用户身份证|
| unitapplyPersonIDNnumber |  | String   |单位申办人身份证|
| table |  | List   |下面list|
|  | waterNature | String   |用水性质|
|  | waterPersonNumber | int   |用水人数|
|  | waterConsumption | double   |预估月用水量|
|  | applyMeterDiameter | String   |申请水表口径|


### 表务管理→安装管理→领表安装→安装工单信息接口
【POST/api/meter/operationsManagement/install/installOrder】

- 请求：无


- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": {
        "installOrderNumber": "IOS-101",
        "applyNumber": "SO-102",
        "userNumber": "AX101",
        "userName": "用户1",
        "installAddress": "xxx",
        "sceneInstallOrder": "IO-101",
        "chooseMeter": [
            {
                "meterDiameter": "DN100",
                "type": "xxx类型",
                "factory": "拓安信",
                "accuracyLevel": "5"
            },
            {
                "meterDiameter": "DN80",
                "type": "xxx类型",
                "factory": "拓安信",
                "accuracyLevel": "4"
            },
            {
                "meterDiameter": "DN60",
                "type": "xxx类型",
                "factory": "拓安信",
                "accuracyLevel": "3"
            }
        ],
        "requestData": [
            {
                "dataName": "要求数据1",
                "dataValue": "要求数据内容1"
            },
            {
                "dataName": "要求数据2",
                "dataValue": "要求数据内容2"
            }
        ],
        "actualData": [
            {
                "dataName": "实况数据1",
                "dataValue": "实况数据内容1"
            },
            {
                "dataName": "实况数据2",
                "dataValue": "实况数据内容2"
            }
        ],
        "scenePicture": [
            "img/1.jpg",
            "img/2.jpg",
            "img/3.jpg",
            "img/4.jpg",
            "img/5.jpg"
        ]
    }
}
```

- 响应：

| 参数名称   | 二级子参数 | 参数类型 |  说明  |
| :--------: | :--------: | :------: | :----: |
| installOrderNumber |  | String   |安装工单号|
| applyNumber   |  | String   |申请单号|
| userNumber |  | String   |用户编号|
| userName |  | String   |用户名称|
| installAddress |  | String   |安装地址|
| sceneInstallOrder |  | String   |现场安装工单|
| chooseMeter |  | List   |选择仪表|
|  | meterDiameter | String   |口径|
|  | type | String   |类型|
|  | factory | String   |厂家|
|  | accuracyLevel | String   |精度等级|
| requestData |  | List   |要求数据|
|  | dataName |  |要求数据名称|
|  | dataValue |  |要求数据内容|
| actualData |  | List   |实况数据|
|  | dataName | String   |实况数据名称|
|  | dataValue | String   |实况数据内容|
| scenePicture |  | String[]   |现场环境|



### 表务管理→安装管理→领表安装→安装工单信息选择仪表接口
【POST/api/meter/operationsManagement/install/chooseMeter】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------: | :---------: | :----: |:--------:|
| installOrderNumbe | String |安装工单号| 是 |
| meterDiameter | String   |口径|    是    |
| type   | Timestamp   |类型|    是    |
| factory | String   |厂家|    是    |
| accuracyLevel | String   |精度等级|    是    |


- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称 | 参数类型 | 说明 |
| :---: | :---: | :---: |
| code | int | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据 |
| message | String | 信息 |

### 表务管理→安装管理→现场安装管理→安装审核接口
【GET/api/meter/operationsManagement/install/inStallApproval】

- 请求：无


- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": {
        "orderNumber": "IOS-101",
        "installAddress": "xxx安装地址",
        "sceneInstallOrder": "IS-101",
        "sceneSurvey": [
            {
                "dataName": "现场调查数据名称1",
                "dataValue": "现场调查数据内容1"
            },
            {
                "dataName": "现场调查数据名称2",
                "dataValue": "现场调查数据内容2"
            }
        ],
        "sceneSurveyPicture": [
            "img/1.jpg",
            "img/2.jpg",
            "img/3.jpg",
            "img/4.jpg",
            "img/5.jpg"
        ],
        "meterDiameter": "DN100",
        "type": "xx类型",
        "factory": "xx厂家",
        "accuracyLevel": "100",
        "deviceParameters": "设备参数",
        "confirmReview": [
            "img/1.jpg",
            "img/2.jpg",
            "img/3.jpg",
            "img/4.jpg",
            "img/5.jpg"
        ],
        "tmp": "暂定"
    }
}
```

- 响应：

| 参数名称 | 二级子参数 | 参数类型 |  说明  |
| :--------: | :--------: | :------: | :----: |
| orderNumber |  | String |工单号|
| Tmp |  | String |暂定|
| installAddress |  | String |安装地址|
| sceneInstallOrder |  | String |现场安装工单|
| sceneSurvey |  | List |现场调查数据|
|  | dataName | String |数据名称|
|  | dataValue | String |数据内容|
| sceneSurveyPicture |  | String[] |现场调查图片|
| meterDiameter |  | String |口径|
| type |  | String |类型|
| factory |  | String |厂家|
| accuracyLevel |  | String |精度等级|
| deviceParameters |  | String |设备参数|
| confirmReview |  | String[] |确认复核图片|

### 表务管理→安装管理→现场安装管理→安装审核确认接口
【POST/api/meter/operationsManagement/install/inStallApprovalConfirm】

- 请求

| 参数名称    | 参数类型 | 说明     | 是否必填 |
| ----------- | -------- | -------- | -------- |
| confirm     | int      | 是否通过 | 是       |
| orderNumber | String   | 工单号   | 是       |

- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称 | 参数类型 |          说明           |
| :------: | :------: | :---------------------: |
|   code   |   int    | 状态码，0：成功 -1:失败 |
|   data   |  Object  |        响应数据         |
| message  |  String  |          信息           |

### 表务管理→安装管理→现场安装管理→安装审核确认接口
【POST/api/meter/operationsManagement/install/inStallOrderTotal】

- 请求

| 参数名称  | 参数类型  |   说明   | 是否必填 |
| :-------: | :-------: | :------: | :------: |
| startTime | Timestamp | 开始时间 |    是    |
|  endTime  | Timestamp | 结束时间 |    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "organizationName": "xxx组织",
            "userNumber": "AX101",
            "userName": "用户1",
            "installAddress": "XXX安装地址",
            "installOrderNumber": "IOS-101",
            "isInstall": 1,
            "acceptanceState": "已验收",
            "isTransformCostSystem": 1,
            "isTransformOrder": 1,
            "orderNumber": "IOS-102",
            "total": 20
        },
        {
            "organizationName": "xxx组织1",
            "userNumber": "AX111",
            "userName": "用户2",
            "installAddress": "XXX安装地址1",
            "installOrderNumber": "IOS-111",
            "isInstall": 1,
            "acceptanceState": "已验收",
            "isTransformCostSystem": 1,
            "isTransformOrder": 1,
            "orderNumber": "IOS-112",
            "total": 30
        }
    ]
}
```

- 响应：

|       参数名称        | 参数类型 |       说明       |
| :-------------------: | :------: | :--------------: |
|   organizationName    |  String  |     组织名称     |
|         Total         |   int    |       小计       |
|      userNumber       |  String  |     用户编号     |
|       userName        |  String  |     用户名称     |
|    installAddress     |  String  |     安装地址     |
|  installOrderNumber   |  String  |    安装工单号    |
|       isInstall       |   int    |     是否安装     |
|    acceptanceState    |  String  |     验收状态     |
| isTransformCostSystem |   int    | 是否转入收费系统 |
|   isTransformOrder    |   int    |    是否转工单    |
|      orderNumber      |  String  |      工单号      |




### 表务管理→电池通信管理→电池通信总览→电池通信统计→电池维护总数接口
【GET/api/meter/operationsManagement/BatteryCommunication/batteryMaintenance】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------- | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "factoryName": "厂家1",
            "finished": 20,
            "unfinished": 30,
            "total": 50
        },
        {
            "factoryName": "厂家2",
            "finished": 30,
            "unfinished": 30,
            "total": 60
        },
        {
            "factoryName": "厂家3",
            "finished": 30,
            "unfinished": 50,
            "total": 80
        }
    ]
}
```
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------- | :------: | :----: |
| factoryName | String   |厂家名称|
| finished | int   |完成数|
| unfinished | int   |未完成数|
| total | int   |总数|


### 表务管理→电池通信管理→电池通信总览→电池通信统计→测量电池接口
【GET/api/meter/operationsManagement/BatteryCommunication/measureBattery】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------- | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "factoryName": "厂家1",
            "finished": 30,
            "unfinished": 30,
            "total": 60
        },
        {
            "factoryName": "厂家2",
            "finished": 40,
            "unfinished": 40,
            "total": 80
        },
        {
            "factoryName": "厂家3",
            "finished": 50,
            "unfinished": 50,
            "total": 100
        }
    ]
}
```
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------- | :------: | :----: |
| factoryName | String   |厂家名称|
| finished | int   |完成数|
| unfinished | int   |未完成数|
| total | int   |总数|


### 表务管理→电池通信管理→电池通信总览→电池通信统计→通讯电池接口
【GET/api/meter/operationsManagement/BatteryCommunication/communicationBattery】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------- | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "factoryName": "厂家1",
            "finished": 40,
            "unfinished": 30,
            "total": 70
        },
        {
            "factoryName": "厂家2",
            "finished": 40,
            "unfinished": 40,
            "total": 80
        },
        {
            "factoryName": "厂家3",
            "finished": 40,
            "unfinished": 50,
            "total": 90
        }
    ]
}
```
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------- | :------: | :----: |
| factoryName | String   |厂家名称|
| finished | int   |完成数|
| unfinished | int   |未完成数|
| total | int   |总数|


### 表务管理→电池通信管理→电池通信总览→单表电池通信接口
【GET/api/meter/operationsManagement/BatteryCommunication/singleMeterCommunication】

请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------- | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
	"code": 0,
	"message": "SUCC",
	"data": [{
		"time": 1523341096949,
		"eventType": "入库",
		"describe": "测试",
		"workOrderNumber": "I-OS1234"
	}]
}
```
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------- | :------: | :----: |
| time | Timestamp   |时间|
| eventType | String   |事件类型|
| describe | String   |描述|
| workOrderNumber | String   |工单号|


### 表务管理→电池通信管理→SIM卡管理→SIM卡统计接口
【GET/api/meter/operationsManagement/BatteryCommunication/simTotal】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------- | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": {
        "year": [
            {
                "sort": "一月",
                "warehouseTotal": 300,
                "intoTotal": 100,
                "requisitionTotal": 100,
                "balance": 100
            },
            {
                "sort": "二月",
                "warehouseTotal": 200,
                "intoTotal": 70,
                "requisitionTotal": 40,
                "balance": 50
            }
        ],
        "month": [
            {
                "sort": "一号",
                "warehouseTotal": 200,
                "intoTotal": 70,
                "requisitionTotal": 40,
                "balance": 50
            },
            {
                "sort": "二号",
                "warehouseTotal": 200,
                "intoTotal": 70,
                "requisitionTotal": 40,
                "balance": 50
            },
            {
                "sort": "三号",
                "warehouseTotal": 200,
                "intoTotal": 70,
                "requisitionTotal": 40,
                "balance": 50
            }
        ]
    }
}
```
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------- | :------: | :----: |
| sort | String   |横排名称|
| warehouseTotal | int   |库存总数|
| intoTotal | int   |入库数|
| requisitionTotal | int   |领用数|
| balance | int   |结余|


### 表务管理→电池通信管理→SIM卡管理→SIM卡明细接口
【GET/api/meter/operationsManagement/BatteryCommunication/simDetails】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------- | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "supplier": "拓安信",
            "openingTime": 1523504596185,
            "setMeal": "xxx套餐"
        }
    ]
}
```
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------- | :------: | :----: |
| supplier | String   |供应商|
| openingTime | Timestamp   |开通时间|
| setMeal | String   |套餐|


### 表务管理→电池通信管理→SIM卡管理→SIM卡入库接口
【GET/api/meter/operationsManagement/BatteryCommunication/simInto】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------- | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "intoBatch": "I-OS1234",
            "chinaMobile": 10,
            "chinaUnicom": 5,
            "chinaTelecom": 5,
            "total": 20
        }
    ]
}
```
- 响应：

| 参数名称   | 参数类型 |  说明  |
| :--------- | :------: | :----: |
| intoBatch | String   |入库批次|
| chinaMobile | Timestamp   |中国移动数量|
| chinaUnicom | String   |中国联通|
| chinaTelecom | String   |中国电信|
| total | String   |总数量|


### 表务管理→电池通信管理→SIM卡管理→SIM卡入库新增接口
【POST/api/meter/operationsManagement/BatteryCommunication/simIntoApply】

- 请求：

|    参数名称     | 二级子参数  | 参数类型  |      说明      | 是否必填 |
| :-------------: | :---------: | :-------: | :------------: | :------: |
| intoOrderNumber |             |  String   |    入库单号    |    是    |
|   orderNumber   |             |  String   |     工单号     |    是    |
|    intoTime     |             | Timestamp |    入库时间    |    是    |
|   intoPerson    |             |  String   |     入库人     |    是    |
|    SIMNumber    |             |    int    |   本批卡数量   |    是    |
|      type       |             |  String   |      类型      |    是    |
|    infoTotal    |             |  String   |  可用信息总数  |    是    |
|    operator     |             |  String   |     运营商     |    是    |
|   usefullTime   |             |    int    | 预计可使用时间 |    是    |
|     simInfo     |             |   List    |    SIM信息     |    是    |
|                 | NumberStart |  String   |    号段开始    |    是    |
|                 |  NumberEnd  |  String   |    号段结束    |    是    |
|                 |  SIMtotal   |    int    |    张数小计    |    是    |

- JSON请求参数实例：

```json
{
	"intoOrderNumber": "IO-101",
	"orderNumber": "IO-101",
	"intoTime": 14232323232,
	"intoPerson": "入库人1",
	"SIMNumber": 12,
	"type": "xxx",
	"infoTotal": "xxx",
	"operator": "xxx运营商",
	"usefullTime": 30,
	"simInfo": [{
			"NumberStart": "123",
			"NumberEnd": "789",
			"SIMtotal": 123
		},
		{
			"NumberStart": "123",
			"NumberEnd": "789",
			"SIMtotal": 123
		}
	]
}
```

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": null
}
```

- 响应：

| 参数名称 | 参数类型 |          说明           |
| :------: | :------: | :---------------------: |
|   code   |   int    | 状态码，0：成功 -1:失败 |
|   data   |  Object  |        响应数据         |
|   msg    |  String  |          信息           |

### 表务管理→电池通信管理→通讯维护管理接口

【GET/api/meter/operationsManagement/BatteryCommunication/communicationMaintain】

- 请求：

| 参数名称  |   参数类型  |  说明  | 是否必填 |
| :-------: | :---------: | :----: |:--------:|
| startTime | Timestamp   |开始时间|    是    |
| endTime   | Timestamp   |结束时间|    是    |

- JSON实例：

```json
{
    "code": 0,
    "message": "SUCC",
    "data": {
        "year": {
            "communicationRatioList": [
                {
                    "sort": "1月",
                    "level1": 1,
                    "level2": 2,
                    "level3": 3,
                    "level4": 4
                },
                {
                    "sort": "2月",
                    "level1": 2,
                    "level2": 3,
                    "level3": 4,
                    "level4": 5
                },
                {
                    "sort": "3月",
                    "level1": 3,
                    "level2": 5,
                    "level3": 6,
                    "level4": 7
                },
                {
                    "sort": "4月",
                    "level1": 8,
                    "level2": 7,
                    "level3": 6,
                    "level4": 3
                }
            ],
            "signalRatioList": [
                {
                    "sort": "1月",
                    "level1": 1,
                    "level2": 2,
                    "level3": 3
                },
                {
                    "sort": "2月",
                    "level1": 2,
                    "level2": 3,
                    "level3": 4
                },
                {
                    "sort": "3月",
                    "level1": 3,
                    "level2": 5,
                    "level3": 6
                },
                {
                    "sort": "4月",
                    "level1": 8,
                    "level2": 7,
                    "level3": 6
                }
            ]
        },
        "month": {
            "communicationRatioList": [
                {
                    "sort": "1号",
                    "level1": 1,
                    "level2": 2,
                    "level3": 3,
                    "level4": 4
                },
                {
                    "sort": "2号",
                    "level1": 2,
                    "level2": 3,
                    "level3": 4,
                    "level4": 5
                },
                {
                    "sort": "3号",
                    "level1": 3,
                    "level2": 5,
                    "level3": 6,
                    "level4": 7
                },
                {
                    "sort": "4号",
                    "level1": 8,
                    "level2": 7,
                    "level3": 6,
                    "level4": 3
                }
            ],
            "signalRatioList": [
                {
                    "sort": "1号",
                    "level1": 1,
                    "level2": 2,
                    "level3": 3
                },
                {
                    "sort": "2号",
                    "level1": 2,
                    "level2": 3,
                    "level3": 4
                },
                {
                    "sort": "3号",
                    "level1": 3,
                    "level2": 5,
                    "level3": 6
                },
                {
                    "sort": "4号",
                    "level1": 8,
                    "level2": 7,
                    "level3": 6
                }
            ]
        }
    }
}
```

响应：

| 参数名称 |       二级子参数       | 三级子参数 | 参数类型 |     说明     |
| :------: | :--------------------: | :--------: | :------: | :----------: |
|   year   |                        |            |   List   |   年份数据   |
|          | communicationRatioList |            |   List   | 通讯占比数据 |
|          |                        |    sort    |  String  |   月份名称   |
|          |                        |   level1   |   int    |    1级值     |
|          |                        |   level2   |   int    |    2级值     |
|          |                        |   level3   |   int    |    3级值     |
|          |                        |   level4   |   int    |    4级值     |
|          |    signalRatioList     |    sort    |  String  |   日期名称   |
|          |                        |   level1   |   int    |    1级值     |
|          |                        |   level2   |   int    |    2级值     |
|          |                        |   level3   |   int    |    3级值     |
|  month   |                        |            |          |   月份数据   |






###  表务管理→校验管理→首检管理→首检信息录入接口

【POST  multipart/form-data   /api/meter/operationsManagement/check/tblCheckfirst 】
- 请求：

| 参数名称                   | 参数类型   | 是否必填          | 说明   |
| :--------------------- | :----- | :------------ | :--- |
| workNumber             | String | 工单号           | 是    |
| instrumentNumber       | String | 仪表编号          | 是    |
| checkAccuracy          | String | 精度等级          | 是    |
| verificationUnit       | String | 检验单位          | 是    |
| checkDate              | String | 检验时间          | 是    |
| checkResult            | String | 检验结果 0通过,1不通过 | 是    |
| checkCertificateNumber | String | 证书编号          | 是    |
| q1                     | String | 最小流量          | 是    |
| q1Note                 | String | Q1备注          | 是    |
| q2                     | String | 分解流量          | 是    |
| q2Note                 | String | Q2备注          | 是    |
| q3                     | String | Q3            | 是    |
| q3Note                 | String | Q3备注          | 是    |
| q4                     | String | Q4            | 是    |
| q4Note                 | String | Q4备注          | 是    |
| file                   | File   | 附件            | 是    |


- JSON实例：

```json

{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |

### 表务管理→校验管理→首检管理→首检结果明细接口

【GET /api/meter/operationsManagement/check/tbCheckFirstDetail】

- 请求：

| 参数名称      | 参数类型   | 是否必填 | 说明   |
| :-------- | :----- | :--- | :--- |
| startTime | String | 开始时间 | 是    |
| endTime   | String | 结束时间 | 是    |

- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "meterDiameter": 32,
      "singleCount": 50,
      "instrumentNumber": "12",
      "checkAccuracy": "12",
      "range": "2222222222",
      "checkResult": "12",
      "q1": 12,
      "q1Note": "12.0",
      "q2": 22,
      "q2Note": "22.0",
      "q3": 33,
      "q3Note": "33.0",
      "q4": 44,
      "q4Note": "44.0",
      "validDate": "2018-62-80",
      "checkDate": "12",
      "verificationUnit": "222北京天诶",
      "workNumber": "123156562221215"
    },
    {
      "meterDiameter": 3,
      "singleCount": 50,
      "instrumentNumber": "1",
      "checkAccuracy": "1",
      "range": "222222",
      "checkResult": "1",
      "q1": 1,
      "q1Note": "1.0",
      "q2": 2,
      "q2Note": "2.0",
      "q3": 3,
      "q3Note": "3.0",
      "q4": 4,
      "q4Note": "4.0",
      "validDate": "2018-6-80",
      "checkDate": "1",
      "verificationUnit": "北京天诶",
      "workNumber": "123156561215"
    }
  ]
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


| 参数名称             | 参数类型   | 是否必填          |
| :--------------- | :----- | :------------ |
| meterDiameter    | String | 口径            |
| singleCount      | int    | 本次送检数         |
| instrumentNumber | String | 仪表编号          |
| checkAccuracy    | String | 精度等级          |
| range            | String | 量程范围          |
| checkResult      | String | 检验结果 0通过,1不通过 |
| q1               | String | 最小流量          |
| q1Note           | String | Q1备注          |
| q2               | String | 分解流量          |
| q2Note           | String | Q2备注          |
| q3               | String | Q3            |
| q3Note           | String | Q3备注          |
| q4               | String | Q4            |
| q4Note           | String | Q4备注          |
| validDate        | String | 有效期           |
| checkDate        | String | 检验日期          |
| verificationUnit | String | 检验单位          |
| workNumber       | String | 送检工单号         |



###  表务管理→校验管理→周期性检定→周检录入接口

【POST  multipart/form-data   /api/meter/operationsManagement/check/tblCheck 】

- 请求：

| 参数名称                   | 参数类型   | 是否必填          | 说明   |
| :--------------------- | :----- | :------------ | :--- |
| workNumber             | String | 工单号           | 是    |
| instrumentNumber       | String | 仪表编号          | 是    |
| checkAccuracy          | String | 现精度等级         | 是    |
| originalCheckAccuracy  | String | 原精度等级         | 是    |
| verificationUnit       | String | 检验单位          | 是    |
| checkDate              | String | 检验时间          | 是    |
| checkResult            | String | 检验结果 0通过,1不通过 | 是    |
| checkCertificateNumber | String | 证书编号          | 是    |
| q1                     | String | 最小流量          | 是    |
| q1Note                 | String | Q1备注          | 是    |
| q2                     | String | 分解流量          | 是    |
| q2Note                 | String | Q2备注          | 是    |
| q3                     | String | Q3            | 是    |
| q3Note                 | String | Q3备注          | 是    |
| q4                     | String | Q4            | 是    |
| q4Note                 | String | Q4备注          | 是    |
| file                   | File   | 附件            | 是    |


- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |



###  表务管理→校验管理→周期性检定→周检录入接口→根据送检工单号获取相关信息

【GET /api/meter/operationsManagement/check/getWorkOrder】

- 请求：

| 参数名称       | 参数类型   | 是否必填  | 说明   |
| :--------- | :----- | :---- | :--- |
| planNumber | String | 送检工单号 | 是    |

- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "tableAddress": "table",
      "userId": "2018041314362762",
      "userName": "测试201804131436276",
      "installAddress": "东莞市",
      "usedDate": "2018-04-13 14:36:27",
      "waterUsage": "500",
      "ifCheck": "是"
    }
  ]
}
```
- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


###  表务管理→校验管理→周期性检定→周检结果明细接口

【GET /api/meter/operationsManagement/check/tbCheckDetail】

- 请求：

| 参数名称      | 参数类型   | 是否必填 | 说明   |
| :-------- | :----- | :--- | :--- |
| startTime | String | 开始时间 | 是    |
| endTime   | String | 结束时间 | 是    |

- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "meterDiameter": 32,
      "singleCount": 50,
      "instrumentNumber": "12",
      "checkAccuracy": "12",
      "range": "2222222222",
      "checkResult": "12",
      "q1": 12,
      "q1Note": "12.0",
      "q2": 22,
      "q2Note": "22.0",
      "q3": 33,
      "q3Note": "33.0",
      "q4": 44,
      "q4Note": "44.0",
      "validDate": "2018-62-80",
      "checkDate": "12",
      "verificationUnit": "222北京天诶",
      "workNumber": "123156562221215"
    },
    {
      "meterDiameter": 3,
      "singleCount": 50,
      "instrumentNumber": "1",
      "checkAccuracy": "1",
      "range": "222222",
      "checkResult": "1",
      "q1": 1,
      "q1Note": "1.0",
      "q2": 2,
      "q2Note": "2.0",
      "q3": 3,
      "q3Note": "3.0",
      "q4": 4,
      "q4Note": "4.0",
      "validDate": "2018-6-80",
      "checkDate": "1",
      "verificationUnit": "北京天诶",
      "workNumber": "123156561215"
    }
  ]
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


| 参数名称                  | 参数类型   | 是否必填          |
| :-------------------- | :----- | :------------ |
| meterDiameter         | String | 口径            |
| singleCount           | int    | 本次送检数         |
| instrumentNumber      | String | 仪表编号          |
| checkAccuracy         | String | 精度等级          |
| originalCheckAccuracy | String | 原精度等级         |
| range                 | String | 量程范围          |
| checkResult           | String | 检验结果 0通过,1不通过 |
| q1                    | String | 最小流量          |
| q1Note                | String | Q1备注          |
| q2                    | String | 分解流量          |
| q2Note                | String | Q2备注          |
| q3                    | String | Q3            |
| q3Note                | String | Q3备注          |
| q4                    | String | Q4            |
| q4Note                | String | Q4备注          |
| validDate             | String | 有效期           |
| checkDate             | String | 检验日期          |
| verificationUnit      | String | 检验单位          |
| workNumber            | String | 周计划号          |

###  表务管理→校验管理→周期性检定→到期需周检表明细

【GET /api/meter/operationsManagement/check/tbCheckPlan】

- 请求：

| 参数名称       | 参数类型   | 是否必填   | 说明   |
| :--------- | :----- | :----- | :--- |
| expiryDate | String | 快要到期天数 | 是    |

- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "tableAddress": "table",
      "userId": "2018041314420416",
      "userName": "测试201804131442043",
      "installAddress": "东莞市",
      "usedDate": "2018-04-13 14:42:04",
      "waterUsage": "500",
      "ifCheck": "是"
    }
  ]
}

```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


| 参数名称           | 参数类型   | 是否必填  |
| :------------- | :----- | :---- |
| tableAddress   | String | 表地址   |
| userId         | String | 用户编号  |
| userName       | String | 用户名称  |
| installAddress | String | 安装地址  |
| usedDate       | String | 已使用日期 |
| waterUsage     | String | 已计量水量 |
| ifCheck        | String | 是否周检  |



###  表务管理→校验管理→周期性检定→周检计划清单

【GET /api/meter/operationsManagement/check/tbCheckPlanList】

- 请求：

| 参数名称       | 参数类型   | 是否必填   | 说明   |
| :--------- | :----- | :----- | :--- |
| expiryDate | String | 快要到期天数 | 是    |


- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "planNumber": "2018041314425408",
      "planName": "测试14",
      "tableCounts": 54524,
      "planDate": "2018-04-13 14:42:54",
      "planner": "测试人201804131442549"
    }
  ]
}

```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


| 参数名称        | 参数类型   | 是否必填 |
| :---------- | :----- | :--- |
| planNumber  | String | 计划编号 |
| planName    | String | 计划名称 |
| tableCounts | String | 周检表数 |
| planDate    | String | 计划日期 |
| planner     | String | 计划人  |



###  表务管理→校验管理→周期性检定→周检计划清单→获取周检计划清单详细信息

【GET /api/meter/operationsManagement/check/tbCheckPlanDetail】

- 请求：

| 参数名称       | 参数类型   | 是否必填 | 说明   |
| :--------- | :----- | :--- | :--- |
| planNumber | String | 计划编号 | 是    |

- JSON实例：

```json
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "tableAddress": "table",
      "userId": "2018041314434268",
      "userName": "测试201804131443426",
      "installAddress": "东莞市",
      "usedDate": "2018-04-13 14:43:42",
      "waterUsage": "500",
      "ifCheck": "是"
    }
  ]
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |

| 参数名称           | 参数类型   | 是否必填  |
| :------------- | :----- | :---- |
| tableAddress   | String | 表地址   |
| userId         | String | 用户编号  |
| userName       | String | 用户名称  |
| installAddress | String | 安装地址  |
| usedDate       | String | 已使用日期 |
| waterUsage     | String | 已计量水量 |




###  表务管理→表极出入库管理→入库管理→入库操作

【POST     /api/meter/operationsManagement/tableStorage/storageOperation 】
- 请求：

| 参数名称                  | 参数类型   | 是否必填     | 说明   |
| :-------------------- | :----- | :------- | :--- |
| meterDiameter         | String | 口径       | 是    |
| specification         | String | 规格型号     | 是    |
| factory               | String | 厂家       | 是    |
| productBrand          | String | 产品品牌     | 是    |
| outputType            | String | 输出类型     | 是    |
| powerType             | String | 供电方式     | 是    |
| accuracy              | String | 精度       | 是    |
| tableAddress          | String | 表地址      | 是    |
| instrumentNumber      | String | 仪表编号     | 是    |
| factoryDate           | String | 出厂日期     | 是    |
| nameplateAccuracy     | String | 铭牌精度     | 是    |
| certificateNumber     | String | 出厂检验证书编号 | 是    |
| intoOrderNumber       | String | 入库单号     | 是    |
| ifCheck               | String | 是否必须检验   | 是    |
| intoPerson            | String | 入库人      | 是    |
| storageLocation       | String | 存放位置     | 是    |
| state                 | String | 状态       | 是    |
| useCode               | String | 使用编码     | 是    |
| barCode               | String | 条形码      | 是    |
| verificationUnit      | String | 校验单位     | 是    |
| incomingDate          | String | 入库日期     | 是    |
| activationDate        | String | 可启用日期    | 是    |
| installationSituation | String | SIM卡安装情况 | 是    |

- JSON实例：

```

{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |

### 表务管理→表极出入库管理→入库管理→入库统计

【GET /api/meter/operationsManagement/tableStorage/storageOperationCount】

- 请求：

| 参数名称      | 参数类型   | 是否必填 | 说明   |
| :-------- | :----- | :--- | :--- |
| startTime | String | 开始时间 | 是    |
| endTime   | String | 结束时间 | 是    |

- JSON实例：

```
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "meterDiameter": 100,
      "meterModel": "fkshgi",
      "output": "45",
      "factory": "中国制作",
      "serialNumber": "25",
      "factoryDate": "2018-04-16 11:05:09",
      "checkAccuracy": "3",
      "deviceID": "dfsf22",
      "orderNumber": "245434"
    },
    {
      "meterDiameter": 100,
      "meterModel": "fkshgi",
      "output": "45",
      "factory": "中国制作",
      "serialNumber": "25",
      "factoryDate": "2018-04-16 11:05:09",
      "checkAccuracy": "3",
      "deviceID": "dfsf22",
      "orderNumber": "245434"
    }
  ]
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


| 参数名称          | 参数类型   | 是否必填   |
| :------------ | :----- | :----- |
| meterDiameter | int    | 口径     |
| meterModel    | String | 表型     |
| output        | String | 输出     |
| factory       | String | 厂家     |
| serialNumber  | String | 仪表出厂编号 |
| factoryDate   | String | 出厂日期   |
| checkAccuracy | String | 精度等级   |
| deviceID      | String | 出厂设备编号 |
| orderNumber   | String | 入库工单号  |




###  表务管理→表极出入库管理→入库管理→入库操作

【POST     /api/meter/operationsManagement/tableStorage/storageOperation 】
- 请求：

| 参数名称                  | 参数类型   | 是否必填     | 说明   |
| :-------------------- | :----- | :------- | :--- |
| meterDiameter         | String | 口径       | 是    |
| specification         | String | 规格型号     | 是    |
| factory               | String | 厂家       | 是    |
| productBrand          | String | 产品品牌     | 是    |
| outputType            | String | 输出类型     | 是    |
| powerType             | String | 供电方式     | 是    |
| accuracy              | String | 精度       | 是    |
| tableAddress          | String | 表地址      | 是    |
| instrumentNumber      | String | 仪表编号     | 是    |
| factoryDate           | String | 出厂日期     | 是    |
| nameplateAccuracy     | String | 铭牌精度     | 是    |
| certificateNumber     | String | 出厂检验证书编号 | 是    |
| intoOrderNumber       | String | 入库单号     | 是    |
| ifCheck               | String | 是否必须检验   | 是    |
| intoPerson            | String | 入库人      | 是    |
| storageLocation       | String | 存放位置     | 是    |
| state                 | String | 状态       | 是    |
| useCode               | String | 使用编码     | 是    |
| barCode               | String | 条形码      | 是    |
| verificationUnit      | String | 校验单位     | 是    |
| incomingDate          | String | 入库日期     | 是    |
| activationDate        | String | 可启用日期    | 是    |
| installationSituation | String | SIM卡安装情况 | 是    |

- JSON实例：

```

{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |

### 表务管理→表极出入库管理→入库管理→入库统计

【GET /api/meter/operationsManagement/tableStorage/storageOperationCount】

- 请求：

| 参数名称      | 参数类型   | 是否必填 | 说明   |
| :-------- | :----- | :--- | :--- |
| startTime | String | 开始时间 | 是    |
| endTime   | String | 结束时间 | 是    |

- JSON实例：

```
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "meterDiameter": 100,
      "meterModel": "fkshgi",
      "output": "45",
      "factory": "中国制作",
      "serialNumber": "25",
      "factoryDate": "2018-04-16 11:05:09",
      "checkAccuracy": "3",
      "deviceID": "dfsf22",
      "orderNumber": "245434"
    },
    {
      "meterDiameter": 100,
      "meterModel": "fkshgi",
      "output": "45",
      "factory": "中国制作",
      "serialNumber": "25",
      "factoryDate": "2018-04-16 11:05:09",
      "checkAccuracy": "3",
      "deviceID": "dfsf22",
      "orderNumber": "245434"
    }
  ]
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


| 参数名称          | 参数类型   | 是否必填   |
| :------------ | :----- | :----- |
| meterDiameter | int    | 口径     |
| meterModel    | String | 表型     |
| output        | String | 输出     |
| factory       | String | 厂家     |
| serialNumber  | String | 仪表出厂编号 |
| factoryDate   | String | 出厂日期   |
| checkAccuracy | String | 精度等级   |
| deviceID      | String | 出厂设备编号 |
| orderNumber   | String | 入库工单号  |

###  表务管理→表极出入库管理→出库管理→选表领用→根据口径获取表

【GET /api/meter/operationsManagement/tableStorage/pickingTableDiameter】

- 请求：

| 参数名称          | 参数类型   | 是否必填 | 说明   |
| :------------ | :----- | :--- | :--- |
| meterDiameter | String | 口径   | 是    |

- JSON实例

```json
{
  "code": 0,
  "message": "SUCC",
  "data": {
    "data": [
      {
        "meterDiameter": "201804161646497",
        "type": "2",
        "output": "2018-04-16 16:46:49",
        "factory": "make in china",
        "number": "2018041616464980"
      },
      {
        "meterDiameter": "201804161646495",
        "type": "2",
        "output": "2018-04-16 16:46:49",
        "factory": "make in china",
        "number": "2018041616464920"
      }
    ]
  }
}
```


- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


| 参数名称          | 参数类型   | 说明   |
| :------------ | :----- | :--- |
| meterDiameter | String | 口径   |
| type          | String | 类型   |
| output        | String | 输出   |
| factory       | String | 厂家   |
| number        | String | 表计编号 |


###  表务管理→表极出入库管理→出库管理→选表领用→根据SIM获取表


【GET /api/meter/operationsManagement/tableStorage/pickingTableSim】

- 请求：

| 参数名称   | 参数类型   | 是否必填  | 说明   |
| :----- | :----- | :---- | :--- |
| simPid | String | SIM卡号 | 是    |

- JSON实例

```json
{
  "code": 0,
  "message": "SUCC",
  "data": {
    "data": [
      {
        "operator": "sfsda",
        "type": "2",
        "output": "2018-04-16 16:50:38",
        "simPid": "201804161650386"
      },
      {
        "operator": "sfsda",
        "type": "2",
        "output": "2018-04-16 16:50:38",
        "simPid": "201804161650384"
      }
    ]
  }
}
```


- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |


| 参数名称     | 参数类型   | 说明    |
| :------- | :----- | :---- |
| operator | String | 运营商   |
| type     | String | 类型    |
| output   | String | 输出    |
| simPid   | String | SIM卡号 |




###  表务管理→表极出入库管理→出库管理→选表领用


【POST   /api/meter/operationsManagement/tableStorage/savePickingTable】

- 请求：

| 参数名称            | 参数类型   | 是否必填  | 说明   |
| :-------------- | :----- | :---- | :--- |
| meterDiameter   | String | 口径    | 是    |
| type            | String | 类型    | 是    |
| factory         | String | 厂家    | 是    |
| intoInfo        | String | 入库信息  | 是    |
| simPid          | String | SIM卡号 | 是    |
| simType         | String | 卡类型   | 是    |
| consumUnit      | String | 领用单位  | 是    |
| applicant       | String | 领用人   | 是    |
| useUnit         | String | 使用单位  | 是    |
| installPosition | String | 预计安装位置  | 是    |

```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |

###  表务管理→表极出入库管理→出库管理→领用统计

【GET /api/meter/operationsManagement/tableStorage/getPickingTableCount】

- 请求：

| 参数名称      | 参数类型   | 是否必填 | 说明   |
| :-------- | :----- | :--- | :--- |
| startTime | String | 开始时间 | 是    |
| endTime   | String | 结束时间 | 是    |

```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}

```

- 响应：

| 参数名称 | 参数类型   | 说明             |
| :--- | :----- | :------------- |
| code | int    | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据           |
| msg  | String | 信息             |








