# SPM Database Design

## Buyer

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

##Seller 

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

## Admin

- id
- username
- password
- email
- phone
- status
- create_time
- update_time

## Category 类别

- id 
- parent_id 父分类id，默认0
- name 类别名

## Product 商品主表（SPU）

- id
- category_id 类别id
- name 商品名
- pic 商品图片
- attribute_list 属性选项
- description 商品描述
- create_time
- update_time

## Product_specs 商品详情表（指定规格商品SKU）

- id
- product_id
- detail 详细属性
- stock 库存
- price 单价 decimal(8,2)
- create_time
- update_time

## Shopcart购物车

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

