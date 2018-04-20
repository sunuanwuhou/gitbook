# 【公共定义】服务端接口协议

## 公共请求参数

请求头：

| 参数名称 | 参数类型 | 是否必填 | 说明 |
| :--- | :--- | :--- | :--- |
| TW-AUTH-HEADER | String | 是 | 请求TOKEN信息 |

###  {#公共响应参数}

## 公共响应参数

响应参数：

| 参数名称 | 参数类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 状态码，0：成功 -1:失败 |
| data | Object | 响应数据 |
| msg | String | 信息 |

JSON实例：

```
{
    "code": -1,
    "msg": "用户名或密码错误",
    "data": null
}
```

### 

## 分页请求参数

| 参数名称 | 参数类型 | 是否必填 | 说明 |
| :--- | :--- | :--- | :--- |
| pageSize | String | 否 | 每页条数，默认20 |
| pageIndex | String | 否 | 页码，默认1 |

###  {#分页响应参数}

## 分页响应参数

| 参数名称 | 参数类型 | 说明 |
| :--- | :--- | :--- |
| data.datas | List | 返回具体数据对象数组 |
| data.total | int | 数据的总记录数 |
| data.totalPage | int | 总页数 |

## 常用数据格式

| 类型 | 格式 |
| :--- | :--- |
| 时间 | Timestamp\(毫秒\) |

## 获取TOKEN【POST  /api/auth/jwt/token】

请求参数：

| 参数名称 | 参数类型 | 是否必填 | 说明 |
| :--- | :--- | :--- | :--- |
| loginName | String | 是 | 登陆账号 |
| password | String | 是 | 密码 |

请求JSON示例：

```
{
    "loginName":"admin",
    "password":"8D969EEF6ECAD3C29A3A629280E686CF0C3F5D5A86AFF3CA12020C923ADC6C92"
}
```

响应JSON示例：

```
{
    "code": 0,
    "msg": "SUCC",
    "data": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsInVzZXJJZCI6IjEiLCJuYW1lIjoi57O757uf566h55CG5ZGYIiwiZXhwIjoxNTIwNDQ4NzIzfQ.6z1NcelIa3wdv6938mevHJHT6jbhWmZ-fl4keZr2vDs"
}
```

响应参数：

| 参数名称 | 参数类型 | 说明 |
| :--- | :--- | :--- |
| data | String | Token |



