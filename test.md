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

####参数####




