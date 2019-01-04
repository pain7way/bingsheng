select A.openid openid,
A.coupon_id coupon_id,
A.event event,
A.recv_time recv_time,
B.csr_store_id store_id 
from
(select log.distinct_id openid,
       product.spu_code coupon_id,
       log.event event,
       log.recv_time recv_time
from (select distinct_id,coupon_id,event,recv_time from src_qianfan.wechat_mini_program_log where length(coupon_id)=5 and plaza_id=1102588 and dt='2019-01-03' and coupon_id is not null) as log left join src_mall.product as product on log.coupon_id=product.id) as A left join src_qf_prod_coupon.coupon_store_rule as B on A.coupon_id=B.c_no 

UNION ALL 

select log.distinct_id openid,
       c_product.product_no coupon_id,
       log.event event,
       log.recv_time recv_time,
       c_product.publisher_store_id store_id
from (select distinct_id,coupon_id,event,recv_time from src_qianfan.wechat_mini_program_log where length(coupon_id)=14 and plaza_id=1102588 and dt='2019-01-03' and coupon_id is not null) as log left join dwd.coupon_product as c_product on log.coupon_id=c_product.product_no;

























