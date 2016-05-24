海外购api测试
=============

商品列表
--------

####接口地址####

``/higo/list``

####请求方式####

``GET``

####参数#####

|  参数  | 含义                    | 是否必须              |允许值的范围及含义                   |
|--------|-------------------------|-----------------------|-------------------------------------|
| top    | 是否海淘主推商品        | 否 （为空默认0）      |0 表示普通商品列表，1表示主推商品列表|


####返回信息####

返回格式 json

#####成功#####

`
    {
        "status":200,
        "msg":"获取海淘商品列表成功",
        "content":[
               {
                  "goods_id": "1101686",
                  "name": "海淘测试一,",
                  "group_title": "",
                  "group_long_title": "",
                  "product_sku": "P5694875C841BA:1",
                  "seaamoy_price": 13,
                  "seaamoy_top_pic": "http://images.test.zhiwo.com/product/2016/0119/13468781174507945589.jpg",
                  "group_discount": "9.9",
                  "type_id": "2",
                  "cat_id": "197",
                  "efficacy_ids": "",
                  "brand_id": "420",
                  "stock": "195",
                  "uptime": "0",
                  "downtime": "0",
                  "newly": "0",
                  "group_top": "0",
                  "group_status": "0",
                  "is_license": "0",
                  "market_price": "0.00",
                  "lowest_price": "0.00",
                  "brief": "◎贺！台北销售破100万支！台湾紧急空运中国独家上市！\r\n ◎连日韩名星、女人节目老师、名模、杂志编辑、記者也疯狂抢购、讨论！\r\n ◎日本、韩国、台湾的最大美容讨论网站最力推荐商品！！!",
                  "small_pic": "http://images.test.zhiwo.com/product/2016/0119/13468781174507945589.jpg",
                  "big_pic": "http://images.test.zhiwo.com/product/2016/0128/7444360269170012738.jpg",
                  "group_main_pic": "/static/images/empty_pic.jpg",
                  "group_big_pic": "",
                  "group_small_pic": "",
                  "comments_count": "0",
                  "group_virtual_buy_num": "0",
                  "ext_attribute": "a:14:{s:9:\"原产地\";s:0:\"\";s:6:\"规格\";s:0:\"\";s:6:\"质地\";s:0:\"\";s:12:\"生产日期\";s:4:\"2016\";s:9:\"保质期\";s:4:\"2016\";s:6:\"包装\";s:0:\"\";s:6:\"功效\";s:12:\"美容养颜\";s:12:\"适合肤质\";s:0:\"\";s:12:\"适合人群\";s:0:\"\";s:12:\"使用方法\";s:0:\"\";s:12:\"产品介绍\";s:0:\"\";s:24:\"美容顾问使用体验\";s:0:\"\";s:12:\"特别说明\";s:0:\"\";s:12:\"温馨提示\";s:234:\"由于部分商品包装更换较为频繁，因此您收到的货品有可能与图片不完全一致，请您以收到的商品实物为准，同时我们会尽量做到及时更新，由此给您带来不便多多谅解，谢谢！\";}",
                  "promotion_tag": "",
                  "seaamoy_pic": "http://images.test.zhiwo.com/product/2016/0119/18285568789856083639.jpg",
                  "havestock": "1",
                  "efficacy_tags": [],
                  "seaamoy_status": 1
                },
                ......
        ]
    }
`

#####失败#####

`
    {
        "status":204,
        "msg":"获取海淘商品列表失败",
        "content":[]
    }
`

商品详情
-------

####接口地址####

``/higo/detail``

####请求方式####

``GET``


####参数####

|  参数  | 含义                    | 是否必须              |允许值的范围及含义                   |
|--------|-------------------------|-----------------------|-------------------------------------|
|goods_id| 海淘商品id              | 是                    | 商品列表中的id                      |


####返回信息####

返回格式 json

#####成功#####

`
    {
        "status":200,
        "msg":"获取商品详情成功",
          "content": {
            "goods_info": {
              "goods_id": "1101686",
              "name": "海淘测试一,",
              "product_sku": "P5694875C841BA:1",
              "uptime": "0",
              "downtime": "0",
              "newly": "0",
              "seaamoy_price": "13.00",
              "seaamoy_pic": "http://images.test.zhiwo.com/product/2016/0119/18285568789856083639.jpg",
              "market_price": "0.00",
              "lowest_price": "0.00",
              "brief": "◎贺！台北销售破100万支！台湾紧急空运中国独家上市！\r\n ◎连日韩名星、女人节目老师、名模、杂志编辑、記者也疯狂抢购、讨论！\r\n ◎日本、韩国、台湾的最大美容讨论网站最力推荐商品！！!",
              "big_pic": "http://images.test.zhiwo.com/product/2016/0128/7444360269170012738.jpg",
              "small_pic": "http://images.test.zhiwo.com/product/2016/0119/13468781174507945589.jpg",
              "group_big_pic": "",
              "group_main_pic": "/static/images/empty_pic.jpg",
              "group_small_pic": "",
              "intro": "",
              "use_method": "",
              "ext_attribute": {
                "原产地": "",
                "规格": "",
                "质地": "",
                "生产日期": "2016",
                "保质期": "2016",
                "包装": "",
                "功效": "美容养颜",
                "适合肤质": "",
                "适合人群": "",
                "使用方法": "",
                "产品介绍": "",
                "美容顾问使用体验": "",
                "特别说明": "",
                "温馨提示": "由于部分商品包装更换较为频繁，因此您收到的货品有可能与图片不完全一致，请您以收到的商品实物为准，同时我们会尽量做到及时更新，由此给您带来不便多多谅解，谢谢！"
              },
              "comments_count": "0",
              "group_virtual_buy_num": "0",
              "cat_id": "197",
              "brand_id": "420",
              "efficacy_ids": "",
              "stock": 195,
              "sales_channel": "4",
              "goods_point": "0.0",
              "max_buy": "0",
              "min_buy": "0",
              "marketable": "true",
              "max_buy_limit_time": "0",
              "orderlimit": "0",
              "userlimit": "0",
              "taxation": 11.5,
              "_taxation": "50.00",
              "efficacy_tags": [],
              "favorite": "2",
              "cat_name": "单方纯精油",
              "efficacy": "",
              "arr_efficacy": [],
              "urlName": "%E6%B5%B7%E6%B7%98%E6%B5%8B%E8%AF%95%E4%B8%80%2C"
            },
            "brand_info": {
              "brand_id": "420",
              "brand_name": "123",
              "brand_name_en": "",
              "brand_alias": "",
              "brand_desc": "",
              "brand_url": "/products/420-0-0-10-0-0.html",
              "brand_logo": "",
              "new_logo_url": "",
              "brand_middle_logo": "",
              "brand_banner": "",
              "brand_small_logo": "http://images.zhiwo.com/brand/s132.jpg",
              "brand_license": ""
            }
          }
    }
`

#####失败#####

``
{
  "status": 202,
  "msg": "海淘商品不存在",
  "content": []
}
``

海淘确认订单
-----------

####接口地址####

`/higo/order`

####请求方式####

``POST``

####参数####

|  参数   | 含义                    | 是否必须              |允许值的范围及含义                   |
|---------|-------------------------|-----------------------|-------------------------------------|
|uid      | 用户id                  | 是                    | 用户登录成功后返回uid               |
|token    | 用户token               | 是                    | 用户登录成功后返回的token           |
|goods_id | 海淘商品id              | 是                    | 商品列表中的id                      |
|goods_num| 购买数量                | 否                    | 要购买的商品数量为空是默认为1件     |

####返回信息####

返回格式json

#####成功####

`{
   "status": 200,
   "msg": "获取海淘商品结算数据成功",
   "content": {
     "goods_info": {
       "goods_id": "1101686",
       "name": "海淘测试一,",
       "product_sku": "P5694875C841BA:1",
       "uptime": "0",
       "downtime": "0",
       "newly": "0",
       "seaamoy_price": "13.00",
       "seaamoy_pic": "http://images.test.zhiwo.com/product/2016/0119/18285568789856083639.jpg",
       "market_price": "0.00",
       "lowest_price": "0.00",
       "brief": "◎贺！台北销售破100万支！台湾紧急空运中国独家上市！\r\n ◎连日韩名星、女人节目老师、名模、杂志编辑、記者也疯狂抢购、讨论！\r\n ◎日本、韩国、台湾的最大美容讨论网站最力推荐商品！！!",
       "big_pic": "http://images.test.zhiwo.com/product/2016/0128/7444360269170012738.jpg",
       "small_pic": "http://images.test.zhiwo.com/product/2016/0119/13468781174507945589.jpg",
       "group_big_pic": "",
       "group_main_pic": "/static/images/empty_pic.jpg",
       "group_small_pic": "",
       "intro": "",
       "use_method": "",
       "ext_attribute": "a:14:{s:9:\"原产地\";s:0:\"\";s:6:\"规格\";s:0:\"\";s:6:\"质地\";s:0:\"\";s:12:\"生产日期\";s:4:\"2016\";s:9:\"保质期\";s:4:\"2016\";s:6:\"包装\";s:0:\"\";s:6:\"功效\";s:12:\"美容养颜\";s:12:\"适合肤质\";s:0:\"\";s:12:\"适合人群\";s:0:\"\";s:12:\"使用方法\";s:0:\"\";s:12:\"产品介绍\";s:0:\"\";s:24:\"美容顾问使用体验\";s:0:\"\";s:12:\"特别说明\";s:0:\"\";s:12:\"温馨提示\";s:234:\"由于部分商品包装更换较为频繁，因此您收到的货品有可能与图片不完全一致，请您以收到的商品实物为准，同时我们会尽量做到及时更新，由此给您带来不便多多谅解，谢谢！\";}",
       "comments_count": "0",
       "group_virtual_buy_num": "0",
       "cat_id": "197",
       "brand_id": "420",
       "efficacy_ids": "",
       "stock": 195,
       "sales_channel": "4",
       "goods_point": "0.0",
       "max_buy": "0",
       "min_buy": "0",
       "marketable": "true",
       "max_buy_limit_time": "0",
       "orderlimit": "0",
       "userlimit": "0",
       "taxation": 11.5,
       "_taxation": "50.00",
       "efficacy_tags": [],
       "favorite": "2",
       "total_price": 26,
       "total_taxation": 23,
       "seaamoy_num": 2,
       "cat_name": "单方纯精油",
       "need_taxation": 13
     },
     "address_info": {
       "addr_id": "335",
       "member_id": "797323",
       "name": "沙丽娜",
       "area": "山东省/德州市/宁津县",
       "province": "山东省",
       "city": "德州市",
       "district": "宁津县",
       "addr": "山东省-德州市-宁津县 北京市海淀区大望路啦啦啦啦",
       "zip": "100010",
       "tel": "",
       "mobile": "18810552193",
       "email": "",
       "idcard": "12022******5023",
       "def_addr": "1"
     },
     "goods_price": "26.00",
     "need_taxation": "13.00",
     "delivery_channel": "Express_5",
     "account_balance": "39552.58",
     "freight": "20.00",
     "allow_deposit": true,
     "need_amount": "59.00"
   }
 }
`

#####失败####

`
{
  "status": 20X,
  "msg": "错误信息"
}`

海淘下单
-------

####接口地址####

`/higo/pay`

####请求方式####

`POST`

####参数####


|  参数          | 含义                    | 是否必须              |允许值的范围及含义                       |
|----------------|-------------------------|-----------------------|-----------------------------------------|
|uid             | 用户id                  | 是                    | 用户登录成功后返回uid                   |
|token           | 用户token               | 是                    | 用户登录成功后返回的token               |
|goods_id        | 海淘商品id              | 是                    | 商品列表中的id                          |
|goods_num       | 购买数量                | 否                    | 要购买的商品数量为空是默认为1件         |
|address_id      |收货地址id               | 是                    | 收货地址id，用户选择的地址id            |
|delivery_channel|配送方式                 | 是                    | 配送方式不支持货到付款，必须Express_5   |
|gateway         |支付方式                 | 是                    | 支付方式只能为三种Deposit，Alipay,Wcpay |
|remarks         |用户订单备注             | 否                    | 用户留言，可以为空                      |


####返回数据####

返回格式json

#####成功#####

`{
   "status": 200,
   "msg": "下单成功",
   "content": {
     "order_id": 1605241042230,
     "receive_name": "沙丽娜",
     "receive_mobile": "18810552193",
     "receive_address": "山东省-德州市-宁津县 北京市海淀区大望路啦啦啦啦",
     "total_amount": "39.50",
     "balance_amount": "0.00",
     "gateway": "Wcpay",
     "address": {
       "address_id": 335,
       "receive_name": "沙丽娜",
       "receive_addr": "山东省-德州市-宁津县 北京市海淀区大望路啦啦啦啦",
       "receive_mobile": "18810552193",
       "receive_zip": "100010",
       "receive_tel": "",
       "receive_idcard": "12022******5023"
     },
     "order_info": {
       "order_id": 1605241042230,
       "create_time": 1464057743,
       "goods_amount": 13,
       "total_amount": 39.5,
       "freight": "20.00",
       "balance_amount": 0,
       "coupon_amount": 0,
       "coupon_codes": "",
       "market_rule_id": 0,
       "market_rule_type": "",
       "need_amount": 39.5,
       "gateway": "Wcpay",
       "pay_way": "Wcpay",
       "pay_status": 0,
       "delivery_channel": "Express_5",
       "financial_examine": 1,
       "member_id": "797323",
       "member_name": "18932669921",
       "goods_list": [
         {
           "gid": "1101686",
           "from": "seaamoy",
           "time": 1464057743,
           "price": "13.00",
           "num": 1,
           "free": 2,
           "vip": 0,
           "item_price": "13.00",
           "goods_id": "1101686",
           "name": "海淘测试一,",
           "product_sku": "P5694875C841BA:1",
           "mall_price": 0,
           "marketable": "true",
           "stock": 195,
           "market_price": "0.00",
           "small_pic": "http://images.test.zhiwo.com/product/2016/0119/13468781174507945589.jpg",
           "big_pic": "http://images.test.zhiwo.com/product/2016/0128/7444360269170012738.jpg",
           "min_buy": "0",
           "max_buy": "0",
           "max_buy_limit_time": "0",
           "orderlimit": "0",
           "userlimit": "0",
           "comments_count": "0",
           "pic_thumb": "http://images.test.zhiwo.com/product/2016/0119/13468781174507945589.jpg"
         }
       ],
       "address_id": 335,
       "receive_name": "沙丽娜",
       "receive_province": "山东省",
       "receive_city": "德州市",
       "receive_district": "宁津县",
       "receive_addr": "山东省-德州市-宁津县 北京市海淀区大望路啦啦啦啦",
       "receive_zip": "100010",
       "receive_tel": "",
       "receive_mobile": "18810552193",
       "score_used": "",
       "score_get": "",
       "remarks": "123",
       "order_refer": "app",
       "order_channel": "",
       "receive_idcard": "12022******5023",
       "tax_rate": 6.5,
       "real_tax_rate": 6.5
     },
     "order_sign": false
   }
 }
`

#####错误#####

`{
    "status":2xx,
    "msg":"错误信息"
}
`







