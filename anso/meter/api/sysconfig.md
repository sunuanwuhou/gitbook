# 【系统设置】


###  增加用户接口

【POST /api/auth/user/save】


- 请求：

| 参数名称           | 参数类型   | 说明       | 是否必填 |
| :------------- | :----- | :------- | :--- |
| name           | String | 账户名称     | 是    |
| loginname      | String | 登录名称     | 是    |
| password       | String | 登录密码     | 是    |
| sex            | String | 性别       | 是    |
| deptid         | String | 部门ID     | 是    |
| remark         | String | 备注       | 是    |
| isAnalyst      | String | 是否分析员    | 是    |
| isEnable       | String | 是否启用     | 是    |
| roleIdList     | int [] | 角色数组集合   | 是    |
| dataRoleIdList | int [] | 数据角色数组集合 | 是    |

- 请求JSON实例：

```json
{
	"name":"测试1",
	"loginname":"qiumeng",
	"password":"123456",
	"sex":"男",
	"deptid":"481",
	"remark":"邱猛",
	"isAnalyst":true,
	"isEnable":true,
	"roleIdList":[
			"1",
			"2",
			"3"
		],
	"dataRoleIdList":[
        	"1",
        	"2"
     ]
	
}

```

- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": 0
}
```

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | int    | 返回生产用户id       |



###  删除用户接口

【DELETE /api/auth/user/delete/${id}】

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |


- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

###  修改用户接口

【PUT /api/auth/user/edit/${id}】

- 请求：

| 参数名称           | 参数类型   | 说明       | 是否必填 |
| :------------- | :----- | :------- | :--- |
| name           | String | 账户名称     | 是    |
| loginname      | String | 登录名称     | 是    |
| password       | String | 登录密码     | 是    |
| sex            | String | 性别       | 是    |
| deptid         | String | 部门ID     | 是    |
| remark         | String | 备注       | 是    |
| isAnalyst      | String | 是否分析员    | 是    |
| isEnable       | String | 是否启用     | 是    |
| roleIdList     | int [] | 角色数组集合   | 是    |
| dataRoleIdList | int [] | 数据角色数组集合 | 是    |

- 请求JSON实例：

```json
{
	"name": "测试2",
	"loginname": "qiumeng",
	"password": "123456",
	"sex": "男",
	"deptid": "481",
	"remark": "邱猛",
	"isAnalyst": true,
	"isEnable": true,
	"roleIdList": [
		"3",
		"4"
	],
	"dataRoleIdList": [
		"1",
		"2"
	]

}

```
- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |





###  查询用户接口

【GET /api/auth/user/userList】

- 响应JSON实例：
```json
{
	"code": 0,
	"message": "SUCC",
	"data": {
		"loginname": "qiumeng2",
		"name": "测试修改",
		"deptid": 4812,
		"isAnalyst": false,
		"roleInfoList": [{
				"id": 3,
				"name": "跟单员",
				"remark": "跟单员",
				"enable": true
			},
			{
				"id": 4,
				"name": "送货员",
				"remark": "送货员",
				"enable": true
			}
		],
		"dataroleInfoList": [{
				"id": 1,
				"name": "dataRole1",
				"remark": "dataRole1",
				"enable": true
			},
			{
				"id": 3,
				"name": "dataRole3",
				"remark": "dataRole3",
				"enable": true
			}
		]
	}
}
```


- 响应：

| 参数名称             | 子参数名称  | 参数类型    | 说明                  |
| :--------------- | :----- | :------ | :------------------ |
| loginname        |        | int     | 用户登录名               |
| name             |        | String  | 用户名                 |
| deptid           |        | int     | 部门ID                |
| isAnalyst        |        | boolean | 是否分析员 true：是 其他： 不是 |
| roleInfoList     |        | List    | 角色信息                |
|                  | id     | int     | 角色信息                |
|                  | name   | String  | 角色名称                |
|                  | remark | String  | 角色描述                |
|                  | enable | boolean | 是否启用 true：是 其他： 不是  |
| dataroleInfoList |        | List    | 数据角色信息              |
|                  | id     | int     | 数据角色信息              |
|                  | name   | String  | 数据角色名称              |
|                  | remark | String  | 数据角色描述              |
|                  | enable | boolean | 是否启用 true：是 其他： 不是  |

###  修改用户账户密码

【PUT /api/auth/user/update/${id}】

- 请求：

| 参数名称      | 参数类型   | 说明   | 是否必填 |
| :-------- | :----- | :--- | :--- |
| loginname | String | 登录名称 | 是    |
| password  | String | 登录密码 | 是    |


- 请求JSON实例：

```json
{
	"loginname":"qiumeng",
	"password":"123456"
}

```
- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |



###  增加角色接口

【POST /api/auth/role/save】


- 请求：

| 参数名称     | 参数类型   | 说明   | 是否必填 |
| :------- | :----- | :--- | :--- |
| name     | String | 角色名称 | 是    |
| remark   | String | 角色备注 | 是    |
| isEnable | String | 是否启用 | 是    |

- 请求JSON实例：

```json
{
	"name":"质检员",
	"remark":"支连媛",
	"isEnable":true
}

```

- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": 1
}
```

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | int    | 返回角色id         |



###  删除角色接口

【DELETE /api/auth/role/delete/${id}】

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |


- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

###  修改角色接口

【PUT /api/auth/user/${id}】

- 请求：

| 参数名称     | 参数类型   | 说明   | 是否必填 |
| :------- | :----- | :--- | :--- |
| name     | String | 角色名称 | 是    |
| remark   | String | 角色备注 | 是    |
| isEnable | String | 是否启用 | 是    |

- 请求JSON实例：

```json
{
	"name":"质检员",
	"remark":"sfaf",
	"isEnable":true
}

```
- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |



###  查询所有角色接口

【GET /api/auth/role/roleList】

- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": [
    {
      "id": 1,
      "name": "超级管理员",
      "remark": "超级管理员",
      "isEnable": true,
      "createTime": 1524046724000,
      "updateTime": null
    },
    {
      "id": 2,
      "name": "管理员",
      "remark": "管理员",
      "isEnable": true,
      "createTime": 1524046748000,
      "updateTime": null
    },
    {
      "id": 3,
      "name": "跟单员",
      "remark": "跟单员",
      "isEnable": true,
      "createTime": 1524046750000,
      "updateTime": null
    },
    {
      "id": 4,
      "name": "送货员",
      "remark": "送货员",
      "isEnable": true,
      "createTime": 1524046753000,
      "updateTime": null
    },
    {
      "id": 11,
      "name": "质检员",
      "remark": "质检员1",
      "isEnable": true,
      "createTime": 1524036851000,
      "updateTime": 1524037049000
    }
  ]
}
```

- 响应：

| 参数名称       | 参数类型      | 说明                 |
| :--------- | :-------- | :----------------- |
| name       | String    | 角色名称               |
| remark     | String    |                    |
| isEnable   | boolean   | 是否启用。true代表启用，其他不是 |
| createTime | TIMESTAMP | 创建时间               |
| updateTime | TIMESTAMP | 修改时间               |

###  查询单个角色接口

【GET /api/auth/role/${id}】

- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": {
    "id": 11,
    "name": "质检员",
    "remark": "质检员1",
    "isEnable": true,
    "createTime": 1524036851000,
    "updateTime": 1524037049000
  }
}
```


- 响应：

| 参数名称       | 参数类型      | 说明                 |
| :--------- | :-------- | :----------------- |
| name       | String    | 角色名称               |
| remark     | String    |                    |
| isEnable   | boolean   | 是否启用。true代表启用，其他不是 |
| createTime | TIMESTAMP | 创建时间               |
| updateTime | TIMESTAMP | 修改时间               |

###  查询角色所拥有的权限

【GET /api/auth/permission/getPermissList/${id}】

- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": {
    "name": "超级管理员",
    "remark": "超级管理员",
    "isEnable": true,
    "rolePermissionInfoList": [
      {
        "name": "1",
        "icon": "1",
        "type": "MENU",
        "uri": "1",
        "method": "1",
        "permissionValue": "1",
        "parentId": 0,
        "treeId": 0,
        "pageId": 0,
        "orderNum": 999,
        "isEnable": true,
        "remark": "1"
      },
      {
        "name": "1",
        "icon": "1",
        "type": "MENU",
        "uri": "1",
        "method": "1",
        "permissionValue": "1",
        "parentId": 0,
        "treeId": 0,
        "pageId": 0,
        "orderNum": 999,
        "isEnable": true,
        "remark": "1"
      },
      {
        "name": "1",
        "icon": "1",
        "type": "MENU",
        "uri": "1",
        "method": "1",
        "permissionValue": "1",
        "parentId": 0,
        "treeId": 0,
        "pageId": 0,
        "orderNum": 999,
        "isEnable": true,
        "remark": "1"
      },
      {
        "name": "1",
        "icon": "1",
        "type": "MENU",
        "uri": "1",
        "method": "1",
        "permissionValue": "1",
        "parentId": 0,
        "treeId": 0,
        "pageId": 0,
        "orderNum": 999,
        "isEnable": true,
        "remark": "1"
      }
    ]
  }
}
```


- 响应：

| 参数名称                   | 子参数名称            | 参数类型      | 说明                              |
| :--------------------- | :--------------- | :-------- | :------------------------------ |
| name                   |                  | String    | 用户名                             |
| remark                 |                  | int       |                                 |
| isEnable               |                  | boolean   | 是否分析员 true：是 其他： 不是             |
| rolePermissionInfoList |                  | List      | 角色信息                            |
|                        | name             | String    | 权限名称                            |
|                        | icon             | String    | 图标                              |
|                        | type             | String    | 权限类型，菜单MENU  模块MOUDLE  按钮BUTTON |
|                        | uri              | String    | 访问地址                            |
|                        | method           | String    | 访问方法                            |
|                        | permission_value | String    | 权限值                             |
|                        | parent_id        | int       | 父级权限ID                          |
|                        | tree_id          | int       | 权限对应树ID                         |
|                        | page_id          | int       | 权限对应页面资源ID                      |
|                        | order_num        | int       | 排序                              |
|                        | is_enable        | boolean   | 是否启用。true代表启用，其他不是              |
|                        | remark           | String    | 备注                              |
|                        | create_time      | TIMESTAMP | 创建时间                            |
|                        | update_time      | TIMESTAMP | 修改时间                            |




###  修改角色权限

【POST /api/auth/permission/rolePer/edit/${id}】

- 请求

| 参数名称           | 参数类型   | 说明   |
| :------------- | :----- | :--- |
| permissionList | int [] | 权限id |

- 请求json实例：
```json
{
	"permissionList":
		[
			"4","5"
			]
	
}
```

- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```


- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |





###  增加数据角色接口

【POST /api/auth/dataRole/save】


- 请求：

| 参数名称     | 参数类型   | 说明     | 是否必填 |
| :------- | :----- | :----- | :--- |
| name     | String | 数据角色名称 | 是    |
| remark   | String | 数据角色备注 | 是    |
| isEnable | String | 是否启用   | 是    |

- 请求JSON实例：

```json
{
	"name":"dataRole1",
	"remark":"dataRole1",
	"isEnable":true
}

```

- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": 1
}
```

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | int    | 返回数据角色id       |

###  删除数据角色接口

【DELETE /api/auth/dataRole/delete/${id}】

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |


- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

###  修改数据角色接口

【PUT /api/auth/dataRole/edit/${id}】

- 请求：

| 参数名称     | 参数类型   | 说明   | 是否必填 |
| :------- | :----- | :--- | :--- |
| name     | String | 角色名称 | 是    |
| remark   | String | 角色备注 | 是    |
| isEnable | String | 是否启用 | 是    |

- 请求JSON实例：

```json
{
	"name":"dataRole1",
	"remark":"dataRole1",
	"isEnable":true
}

```
- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |



###  查询所有数据角色接口

【GET /api/auth/dataRole/dataRoleList】

- 响应JSON实例：
```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "id": 1,
            "name": "dataRole1",
            "remark": "dataRole1",
            "isEnable": true,
            "createTime": 1524074754000,
            "updateTime": null
        },
        {
            "id": 2,
            "name": "dataRole2",
            "remark": "dataRole2",
            "isEnable": true,
            "createTime": 1524074735000,
            "updateTime": null
        },
        {
            "id": 3,
            "name": "dataRole3",
            "remark": "dataRole3",
            "isEnable": true,
            "createTime": 1524133528000,
            "updateTime": null
        }
    ]
}
```

- 响应：

| 参数名称       | 参数类型      | 说明                 |
| :--------- | :-------- | :----------------- |
| id         | int       | 数据角色id             |
| name       | String    | 数据角色名称             |
| remark     | String    | 数据角色描述             |
| isEnable   | boolean   | 是否启用。true代表启用，其他不是 |
| createTime | TIMESTAMP | 创建时间               |
| updateTime | TIMESTAMP | 修改时间               |

###  查询单个数据角色接口

【GET /api/auth/dataRole/getRoleById/${id}】

- 响应JSON实例：
```json
{
    "code": 0,
    "message": "SUCC",
    "data": {
        "id": 1,
        "name": "dataRole1",
        "remark": "dataRole1",
        "isEnable": true,
        "createTime": 1524074754000,
        "updateTime": null
    }
}
```


- 响应：

| 参数名称       | 参数类型      | 说明                 |
| :--------- | :-------- | :----------------- |
| name       | String    | 数据角色名称             |
| remark     | String    | 数据角色描述             |
| isEnable   | boolean   | 是否启用。true代表启用，其他不是 |
| createTime | TIMESTAMP | 创建时间               |
| updateTime | TIMESTAMP | 修改时间               |

### 获取部门树接口

【GET /api/auth/dept/getDeptTree】

- 响应JSON实例：


```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "id": 23,
            "deptId": "001",
            "label": "拓安信",
            "children": [
                {
                    "id": 24,
                    "deptId": "001001",
                    "label": "开发部",
                    "children": [
                        {
                            "id": 26,
                            "deptId": "001001001",
                            "label": "前端组",
                            "children": [
                                {
                                    "id": 27,
                                    "deptId": "001001001001",
                                    "label": "JS",
                                    "children": []
                                },
                                {
                                    "id": 28,
                                    "deptId": "001001001002",
                                    "label": "CSS",
                                    "children": []
                                },
                                {
                                    "id": 43,
                                    "deptId": "001001001002",
                                    "label": "JQuery",
                                    "children": []
                                }
                            ]
                        },
                        {
                            "id": 29,
                            "deptId": "001001002",
                            "label": "后端组",
                            "children": [
                                {
                                    "id": 30,
                                    "deptId": "001001002001",
                                    "label": "Java",
                                    "children": [
                                        {
                                            "id": 31,
                                            "deptId": "001001002001001",
                                            "label": "接口",
                                            "children": []
                                        }
                                    ]
                                },
                                {
                                    "id": 32,
                                    "deptId": "001001002002",
                                    "label": "C#",
                                    "children": []
                                }
                            ]
                        }
                    ]
                },
                {
                    "id": 25,
                    "deptId": "001002",
                    "label": "销售部",
                    "children": [
                        {
                            "id": 33,
                            "deptId": "001002001",
                            "label": "售后",
                            "children": []
                        },
                        {
                            "id": 34,
                            "deptId": "001002002",
                            "label": "售前",
                            "children": []
                        }
                    ]
                }
            ]
        },
        {
            "id": 35,
            "deptId": "002",
            "label": "前海达信",
            "children": [
                {
                    "id": 36,
                    "deptId": "002001",
                    "label": "开发部",
                    "children": []
                },
                {
                    "id": 37,
                    "deptId": "002002",
                    "label": "行政部",
                    "children": []
                },
                {
                    "id": 38,
                    "deptId": "002003",
                    "label": "人事部",
                    "children": []
                }
            ]
        }
    ]
}
```



- 响应：


| 参数名称     | 参数类型   | 说明   |
| -------- | ------ | ---- |
| id       | int    | 主键Id |
| deptId   | String | 部门Id |
| label    | String | 名称   |
| children | List   | 子节点  |

###  获取部门列表接口

【GET /api/auth/dept/getDeptList】

- 响应JSON实例：
```json
{
    "code": 0,
    "message": "SUCC",
    "data": [
        {
            "id": 23,
            "groupId": null,
            "deptId": "001",
            "level": "1",
            "name": "拓安信",
            "aliasName": "拓安信",
            "orderNum": 0,
            "createTime": null,
            "updateTime": null,
            "createUserId": 0,
            "enabled": 1,
            "deleteFlag": 0
        },
        {
            "id": 24,
            "groupId": null,
            "deptId": "001001",
            "level": "2",
            "name": "开发部",
            "aliasName": "开发部",
            "orderNum": 0,
            "createTime": null,
            "updateTime": null,
            "createUserId": 0,
            "enabled": 1,
            "deleteFlag": 0
        }
    ]
}
```


- 响应：

| 参数名称         | 参数类型      | 说明                    |
| :----------- | :-------- | :-------------------- |
| id           | int       | 主键Id                  |
| groupId      | int       | 预留字段                  |
| deptId       | String    | 部门Id                  |
| level        | String    | 等级                    |
| name         | String    | 部门名称                  |
| aliasName    | String    | 部门别名                  |
| orderNum     | int       | 排序                    |
| createTime   | TIMESTAMP | 创建时间                  |
| updateTime   | TIMESTAMP | 修改时间                  |
| createUserId | int       | 创建人Id                 |
| enabled      | Byte      | 是否启用‘1‘代表启动 ’0‘代表未启动  |
| deleteFlag   | Byte      | 是否删除 ‘1‘代表删除 ’0‘代表未删除 |


###  获取单个部门信息接口

【GET /api/auth/dept/getDeptById/${id}】

- 响应JSON实例：
```json
{
    "code": 0,
    "message": "SUCC",
    "data": {
        "id": 23,
        "groupId": null,
        "deptId": "001",
        "level": "1",
        "name": "拓安信",
        "aliasName": "拓安信",
        "orderNum": 0,
        "createTime": null,
        "updateTime": null,
        "createUserId": 0,
        "enabled": 1,
        "deleteFlag": 0
    }
}
```


- 响应：

| 参数名称         | 参数类型      | 说明                    |
| :----------- | :-------- | :-------------------- |
| id           | int       | 主键Id                  |
| groupId      | int       | 预留字段                  |
| deptId       | String    | 部门Id                  |
| level        | String    | 等级                    |
| name         | String    | 部门名称                  |
| aliasName    | String    | 部门别名                  |
| orderNum     | int       | 排序                    |
| createTime   | TIMESTAMP | 创建时间                  |
| updateTime   | TIMESTAMP | 修改时间                  |
| createUserId | int       | 创建人Id                 |
| enabled      | Byte      | 是否启用‘1‘代表启动 ’0‘代表未启动  |
| deleteFlag   | Byte      | 是否删除 ‘1‘代表删除 ’0‘代表未删除 |

###  添加部门接口

【POST /api/auth/dept/saveDept】

- 请求：

| 参数名称         | 参数类型   | 说明                    | 是否必填 |
| :----------- | :----- | :-------------------- | :--- |
| parentDeptId | String | 父级部门ID                | 是    |
| name         | String | 部门名称                  | 是    |
| aliasName    | String | 部门别名                  | 是    |
| createUserId | int    | 创建人ID                 | 是    |
| orderNum     | int    | 排序                    | 是    |
| enabled      | Byte   | 是否启用‘1‘代表启动 ’0‘代表未启动  | 是    |
| deleteFlag   | Byte   | 是否删除 ‘1‘代表删除 ’0‘代表未删除 | 否    |

- 请求JSON实例：

```json
{
	"parentDeptId":"001001002",
	"name":"PHP",
	"aliasName":"PHP",
	"createUserId":8,
	"orderNum":0,
  	"enabled":1
}
```

- 响应JSON实例：
```json
{
    "code": 0,
    "message": "SUCC",
    "data": 45
}
```


- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |

###  删除部门接口

【DELETE /api/auth/dept/deleteDept/${id}】

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |


- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

###  修改部门接口

【PUT /api/auth/dept/edit/${id}】

- 请求：

| 参数名称      | 参数类型   | 说明   | 是否必填 |
| :-------- | :----- | :--- | :--- |
| name      | String | 角色名称 | 是    |
| aliasName | String | 角色别名 | 是    |
| enabled   | Byte   | 是否启用 | 是    |

- 请求JSON实例：

```json
{
	"name":"dataRole1",
	"remark":"dataRole1",
	"enabled":1
}

```
- 响应JSON实例：
```json
{
  "code": 0,
  "message": "SUCC",
  "data": null
}
```

- 响应：

| 参数名称    | 参数类型   | 说明             |
| :------ | :----- | :------------- |
| code    | int    | 状态码，0：成功 -1:失败 |
| message | String | 信息             |
| data    | object | 响应数据           |
