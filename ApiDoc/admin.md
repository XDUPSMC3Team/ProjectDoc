## admin注册
```
POST /admin/register
```

参数

```
email string
username string
password string
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": "Welcome, xxx"
}
```
字段解释

```
xxx: xxxxxx
```

## admin登录
```
POST /buyer/login
```

参数

```
username string
password string
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
字段解释

```
xxx: xxxxxx
```

## 查看新申请的店铺
```
GET /admin/personal/appliedShops
```

参数

```
无参数
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": { [ // Shop实体数组 ] }
}
```
字段解释

```
xxx: xxxxxx
```

## 通过申请
```
POST /admin/personal/approve
```

参数

```
shopId integer
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
字段解释

```
xxx: xxxxxx
```

## 拒绝申请
```
POST /admin/personal/reject
```

参数

```
shopId integer
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
字段解释

```
xxx: xxxxxx
```
## 搜索店铺
```
GET /admin/personal/search
```

参数

```
shopId integer
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": { // Shop实体 }
}
```
字段解释

```
xxx: xxxxxx
```

## 关闭店铺
```
POST /admin/personal/close
```

参数

```
shopId integer
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
字段解释

```
xxx: xxxxxx
```

