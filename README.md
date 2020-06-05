# Shoppe(微信小程序版)

## 说明

> PC版：[shoppe]( https://github.com/chao0225/shoppe_vue_pc )。

> 后端： [shoppe-server](https://github.com/chao0225/shoppe-server) 。

## 项目简介

此网站是一个商城，前端基于微信小程序，后端部分及数据库设计由自己完成，后期由后端人员接手负责。

项目包含4个tabBar：首页、发现页（即商品展示页）、购物车、我的。另有商品详情页、我的收藏、订单结算页面、我的订单。

实现了商品的展示、商品分类查询、关键字搜索商品、商品详细信息展示、用户购物车、订单结算、用户订单、用户收藏列表。

## 技术栈

- **前端：** 原生微信小程序

- **后端：**`Node.js`、`Koa框架`

- **数据库：**`Mysql`

## 功能模块

### 登录

小程序在启动的时候调用 **wx.login** 获取登录凭证（**code**），然后把code回传到项目的后端服务器 ，调用**auth.code2Session**接口，换取用户唯一标识 **OpenID** 和 会话密钥 **session_key**。 然后把 **OpenID** 注册到项目数据库生成本系统的唯一 **user_id** ，用于在本项目的业务验证。

### 首页

首页主要是对商品的展示，有轮播图展示推荐的商品，热门商品分类九宫格、分类别对热门商品进行展示。

![](https://images.gitee.com/uploads/images/2020/0401/161111_eef9d51b_6502229.png "home.png")

### 发现（即全部商品）

全部商品页面集成了全部商品展示、商品分类查询，以及根据关键字搜索商品结果展示。

![](https://images.gitee.com/uploads/images/2020/0401/161740_47485f62_6502229.png "goods.png")

### 商品详情页

商品详情页主要是对某个商品的详细信息进行展示，用户可以在这里把喜欢的商品加入购物车或收藏列表。

![](https://images.gitee.com/uploads/images/2020/0401/161817_1ca7835d_6502229.png "detail.png")

### 我的购物车

购物车采用[omix](https://github.com/Tencent/omi)进行全局状态管理，实现了购物车商品的添加、删除、增加商品数量、选择结算商品、全选购物车商品结算等功能。

![](https://images.gitee.com/uploads/images/2020/0401/161830_131f4776_6502229.png "shoppingCart.png")

### 订单结算

用户在购物车选择了准备购买的商品后，点击“去结算”按钮，会来到该页面。
用户在这里选择收货地址，确认订单的相关信息，然后确认购买。

![](https://images.gitee.com/uploads/images/2020/0401/161845_65e9733b_6502229.png "confirmOrder.png")

### 我的收藏

用户在商品的详情页，可以通过点击加入 喜欢 按钮，把喜欢的商品加入到收藏列表。

![](https://images.gitee.com/uploads/images/2020/0401/161900_5d526a39_6502229.png "collection.png")

### 我的订单

对用户的所有订单进行展示。

![](https://images.gitee.com/uploads/images/2020/0401/161912_d96ab272_6502229.png "orders.png")

### 我的

![](https://images.gitee.com/uploads/images/2020/0401/161923_06f4eb76_6502229.png "mine.png")

## 运行项目

```
请clone项目到本地
git clone https://github.com/hai-27/store-miniprogram.git
导入项目到微信开发者工具即可
```
