# 【权限】权限模块

## 

## 获取用户权限信息【GET  /api/auth/user/info】

响应JSON示例：

```
{
    "code": 0,
    "msg": "SUCC",
    "data": {
        "loginname": "admin",
        "name": "系统管理员",
        "isAnalyst": null,
        "permissionInfos": [
            {
                "id": 1,
                "name": "运营管理",
                "type": "MENU",
                "permissionValue": "r:operationManage",
                "parentId": 0,
                "treeId": 0,
                "pageId": 0
            },
            {
                "id": 2,
                "name": "大用户表管理",
                "type": "MENU",
                "permissionValue": "r:o:largeCusManage",
                "parentId": 1,
                "treeId": 0,
                "pageId": 0
            }
         ]
     }
}
```

响应参数：

| 参数名称 | 子参数名称 | 参数类型 | 说明 |
| :--- | :--- | :--- | :--- |
| loginname |  | String | 用户登录名 |
| name |  | String | 用户名 |
| isAnalyst |  | String | 是否分析员 1：是   其他： 不是 |
| permissionInfos |  | Array | 权限信息 |
|  | id | int | 权限ID |
|  | name | String | 权限名称 |
|  | type | String | 权限类型 MENU:菜单    MODULE：模块    BUTTON:按钮 |
|  | permissionValue | String | 权限值 |
|  | parentId | int | 父ID |
|  | treeId | int | 树ID（预留） |
|  | pageId | int | 页面ID（预留） |









