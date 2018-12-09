## 卖家注册
```
POST /seller/register
```

参数

```
{
    "realName":string
    "phone":string
    "email": string
    "password": string
    "address":(可选)string
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
## 卖家登录
```
POST /seller/login
```

参数

```
{
    "username": string,
    "password": string
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```

## 添加商品
```
POST /seller/product
```

参数

```
{
    categoryId:(int),    // 商品分类id
    shopId:(int)    // shopid
    name:"",    // 商品名称
    pic:"",    // 商品图片
    price: (double) // 商品价格
    description:"",   // 商品描述
    attributeList:"", // 属性选项
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
## 更新商品
```
POST /seller/product/{productId}
```

参数

```
{
    categoryId:0,    // 商品分类id
    shopId:0,
    name:"",    // 商品名称
    pic:"",    // 商品图片
    price:, //价格
    description:"",   // 商品描述
    attributeList:"", // 属性选项
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
```
说明：对于没有更改的字段一并传递过来
```

## 删除商品
```
Delete /seller/product/delete/{productId}
```
```
无
```
```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```

## 商家注册
```
POST /seller/register/shop
```

参数

```
{
    sellerId,"",    // 买家id
    shopName:"",
    shopDesc:"",    // 可选
    phone:"",   // 可选
    email:"", // 可选
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
## 商家详细信息更改
```
POST /shop/shopDetail/{shopId}
```

参数

```
{
    email:"",
    telephone:“”
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```
```
两个参数都为可选 ，如果为空，后端不做更改
```

# 查找所有的类别

```
GET /category/categories
```

参数

```

```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": [{
        "id":,
        "parentId":,
        "name":
    },]
}
```
# 增加类别

```
GET /category/add
```

参数

```
{
    "parentId":(int),
    "name":
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```

# 增加attributeKey

```
POST /seller/attributeKey
```

参数

```
{
    "categoryId":(int),
    "attributeKey":""   // 颜色 内存
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": ""
}
```

# 根据 categoryId 查找attributeKey

```
GET /seller/attributeKey/{categoryId}
```

参数

```
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data": {{
        "id":,
        "categoryId":,
        "attributeKey":
    }}
}
```

# 增加 一条 attributeValue

```
POST /seller/attributeValue
```

参数

```
{
    "attributeKeyId":(int),
    "attributeValue":""
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data":""
}
```

# 根据 attributeKey 查找 attributeValue

```
POST /seller/attributeValue/{attributeKey}
```

参数

```

```

返回

```
{
    "code": 0,
    "msg": "success",
    "data":{{
        "id":,
        "attributeKeyId":
        "attributeValue":
    }}
}
```
# 增加一条productSpecs
```
POST /seller/productSpecs
```

参数

```
{
    "productId":(int),
    "detail":"",
    "stock":(int),
    "price":(double)
}
```

返回

```
{
    "code": 0,
    "msg": "success",
    "data":""
}
```