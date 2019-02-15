-----

item  
=====
| 参数名称 | 备注 | 库 | 表 | 特征  |
| ----- | ----- | ----- | ----- | -----  |
| couponid | 物料id物料唯一标识 | app_compass | app_compass.baseinfo_goods | couponid |
| coupon_title | 券名称 | app_compass | app_compass.baseinfo_goods | coupon_title  |
| scheme_type | 券细分类型(如代金券、兑换券、停车券等) | app_compass | app_compass.baseinfo_goods | scheme_type  |
| plaza_id | 广场id | app_compass | app_compass.baseinfo_goods | plaza_id  |
| plaza_name | 广场名 | src_basedata | src_basedata.base_store | plaza_name  |
| coupon_type | 券类型 | app_compass | app_compass.baseinfo_goods | coupon_type  |
| sale_price | 券售价 | app_compass | app_compass.baseinfo_goods | sale_price  |
| face_value | 券面额 | app_compass | app_compass.baseinfo_goods | face_value  |
| show_begin_time | 投放开始时间 | app_compass | app_compass.baseinfo_goods | show_begin_time  |
| show_end_time | 投放结束时间 | app_compass | app_compass.baseinfo_goods | show_end_time  |
| coupon_channel | 投放渠道 | app_compass | app_compass.baseinfo_goods | coupon_channel  |
| coupon_channel_id | 投放渠道id | app_compass | app_compass.baseinfo_goods | coupon_channel_id  |
| c_type | 券类型(1:代金券 2:礼品券 3:折扣券 4:停车券) | src_qf_prod_coupon | src_qf_prod_coupon.coupon | c_type  |
| c_title | 券名称 | src_qf_prod_coupon | src_qf_prod_coupon.coupon | c_title  |
| c_subtitle | 券副标题 | src_qf_prod_coupon | src_qf_prod_coupon.coupon | c_subtitle  |
| c_person_each_limit | 每人限领,0不限制 | src_qf_prod_coupon | src_qf_prod_coupon.coupon | c_person_each_limit  |
| c_person_daily_each_limit | 每人每日限领,0不限制 | src_qf_prod_coupon | src_qf_prod_coupon.coupon | c_person_daily_each_limit  |
| c_use_period | 使用有效期（1固定，2活动） | src_qf_prod_coupon | src_qf_prod_coupon.coupon | c_use_period  |
| c_use_rule | 满多少使用(分),0不限制 | src_qf_prod_coupon | src_qf_prod_coupon.coupon | c_use_rule  |
| c_expired_after_hours | 自领取多少小时内有效 | src_qf_prod_coupon | src_qf_prod_coupon.coupon | c_expired_after_hours  |
| cs_stock_num | 可用数 | src_qf_prod_coupon | src_qf_prod_coupon.coupon_stock | cs_stock_num  |
| csr_store_id | 门店id | src_basedata | src_basedata.base_store | csr_store_id  |
| store_name | 门店名 | src_basedata | src_basedata.base_store | store_name  |
| business_name | 业态名 | src_basedata | src_basedata.base_store | business_name  |
| business_id | 业态id | src_basedata | src_basedata.base_store | business_id  |
| now_date | 时间 | app_compass | app_compass.baseinfo_goods | now_date |


******

action 
=====
| 参数名称 | 备注 | 库 | 表 | 特征  |
| ----- | ----- | ----- | ----- | -----  |
| coupon_id | 物料id，物料唯一标识 | app_compass | app_compass.baseinfo_goods | coupon_id  |
| distinct_id | imei/idfa，手机号、openID | src_qianfan | src_qianfan.wechat_mini_program_log | distinct_id  |
| mobile | 手机 | app_compass | app_compass.baseinfo_goods | mobile  |
| event | 事件id | src_qianfan | src_qianfan.wechat_mini_program_log | event  |
| recv_time  | 行为发生时间戳，秒级时间戳(需要确定是请求前还是请求后曝光，event_id去确定-赵淑云) | src_qianfan | src_qianfan.wechat_mini_program_log | recv_time  |
| plaza_id | 优惠券适合的广场id（同item上报信息） | app_compass | app_compass.baseinfo_goods | plaza_id  |
| plaza_name | 广场名 | src_basedata | src_basedata.base_plaza  | plaza_name  |
| uid_type | 0-imei/idfa，2- 手机号，3-openID |  |  |   |




























