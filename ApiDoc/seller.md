## 买家登录
```
POST /seller/login
```

参数

```
email string
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
<<<<<<< HEAD
    pic:"",    // 商品图片
=======
    pic:"",    // 商品图片
>>>>>>> c02394742945ec72b4078c63d0b5fb03f18a5d30
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
        "id":,
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