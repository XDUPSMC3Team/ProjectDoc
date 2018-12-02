# SPM Database Design

## buyer

- id int11
- username varchar
- password varchar
- realname varchar 
- phone varchar
- email varchar
- address varchar
- status tinyint
- create_time timestamp（数据库自行控制，下同）
- update_time timestamp（数据库自行控制，下同）

##seller 

- id
- shopname
- password
- realname
- phone
- email
- address
- status
- create_time
- update_time

## admin

- id
- username
- password
- email
- phone
- status
- create_time
- update_time

## category 类别

- id 
- parent_id 父分类id，默认0
- name 类别名

## product 商品主表（SPU）

- id
- category_id 类别id
- name 商品名
- pic 商品图片
- attribute_list 属性选项，例如：`{"memory":["4G", "8G"], "color":["red","black", "white"]}`
- description 商品描述
- create_time
- update_time

## product_specs 商品详情表（指定规格商品SKU）

- id
- product_id
- detail 详细属性，例如: `{"memory": "4G", "color": "red"}`
- stock 库存
- price 单价 decimal(8,2)
- create_time
- update_time

##attribute_key 商品属性key表

- id
- category_id
- attribute_key 属性key名称，例如：内存，颜色，尺码

##attribute_value 商品属性value表

- id
- attribute_id 属性key的id
- attribute_value

## shopcart购物车

- id
- buyer_id 用户id
- product_id 商品id
- amount 该商品数量
- price 该商品单价 decimal(8,2)
- create_time
- update_time

## order_master 订单主表

- id
- buyer_id
- receiver_name 收货人姓名
- receiver_address 收货地址
- money 总金额 decimal(8,2)
- status 订单状态（0已下单/1已发货/2已收获/3已评价/4退货中/5退货成功）
- pay_status 支付状态 （0未支付/1已支付）
- receive_time 收货时间
- create_time （在这里可作为下单时间使用）
- update_time

## order_detail 订单详情表

- id
- master_id
- product_id
- product_name
- amount 
- price
- create_time
- update_time
## product_collect 商品收藏表
- id
- buyer_id
- product_id
- create_time
- update_time

## shop_collect 店铺收藏表
- id
- buyer_id
- shop_id
- create_time
- update_time
