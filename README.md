## 用户管理

### 买家

+ 注册、登录

+ 查询所有商品
+ 查询单个商品
+ 对具体商品进行更新（加入购物车）



### 卖家

+ 登录、注册

+ 添加商品种类

+ 商品CRUD

	





### 超级管理员

+ 登录、注册

+ 管理所有用户

	







## 商品管理

**CRUD**



随机推荐















## 购物车

+ 存储订单信息







## 数据库设计

### 用户数据库

> 用户表

|   字段   |  类型   |              注释              | 备注 |
| :------: | :-----: | :----------------------------: | :--: |
|   uid    | Integer |             用户id             | 主键 |
| username | varchar |             用户名             |      |
| password | varchar |              密码              |      |
|   role   | Integer | 角色（1:管理员 2:卖家 3:买家） |      |



### 商品数据库

> 商品表

|   字段   |  类型   |   注释   | 备注 |
| :------: | :-----: | :------: | :--: |
|   gid    | Integer |  商品id  | 主键 |
|  gname   | varchar | 商品名称 |      |
| gcontent | varchar | 商品详情 |      |
|   gnum   | Integer | 商品数量 |      |
|  gmoney  |  Float  | 商品价格 |      |
|   tid    | Integer |  种类id  | 外键 |
|   uid    | Integer |  商家id  | 外键 |



> 商品种类表

| 字段  |  类型   |   注释   | 备注 |
| :---: | :-----: | :------: | :--: |
|  tid  | Integer |  种类id  | 主键 |
| tname | varchar | 种类名称 |      |



### 购物车数据库

> 订单表

| 字段 |  类型   |   注释   | 备注 |
| :--: | :-----: | :------: | :--: |
| oid  | Integer |  订单id  | 主键 |
| uid  | Integer |  买家id  | 外键 |
| onum | varchar | 订单编号 |      |



> 订单明细表

|   字段   |  类型   |    注释    | 备注 |
| :------: | :-----: | :--------: | :--: |
|   oid    | Integer |   订单id   | 主键 |
|   gid    | Integer |   商品id   | 外键 |
|   gnum   | Integer |  商品数量  |      |
| summoney |  float  | 商品总价格 |      |









