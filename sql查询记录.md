app_compass.baseinfo_goods
------------------
    select count(*) from app_compass.baseinfo_goods;
    select min(now_date),max(now_date),min(op_time),max(op_time) from app_compass.baseinfo_goods;


src_qianfan.wechat_mini_program_log
------------------
    select count(*) from src_qianfan.wechat_mini_program_log;
    select count(*) from src_qianfan.wechat_mini_program_log where plaza_id=1000772 and dt='2019-01-02';
    select count(*) from src_qianfan.wechat_mini_program_log where plaza_id=1000772 and dt='2018-12-31';
    select dt,count(*) from src_qianfan.wechat_mini_program_log where plaza_id=1000772 and dt like '2018-12-%' group by dt;
    select count(*) from src_qianfan.wechat_mini_program_log where plaza_id=1001145 and dt='2019-01-01';
    select * from src_qianfan.wechat_mini_program_log limit 1;
    select min(dt) dt_min,max(dt) dt_max from src_qianfan.wechat_mini_program_log;


src_basedata.base_store
------------------
    select min(dt) dt_min,
    max(dt) dt_max,
    min(op_time) op_time_min,
    max(op_time) op_time_max 
    from src_basedata.base_store;

    select store_id,
    store_name,
    plaza_id,
    plaza_name,
    business_id,
    business_name from src_basedata.base_store where plaza_id=1105288;
    
    select plaza_id,plaza_name from src_basedata.base_store where plaza_name like '北京%';
    select distinct plaza_id from src_basedata.base_store;
    select store_id,store_name,plaza_id,plaza_name from src_basedata.store where plaza_id=1001145;
    select store_id,store_name,plaza_id,plaza_name from src_basedata.store where store_id=100007644;



src_qf_prod_coupon.coupon
------------------
    select count(*) from src_qf_prod_coupon.coupon;
    
    select min(dt) min_dt,
    max(dt) max_dt,
    min(op_time) min_optime,
    max(op_time) max_optime 
    from src_qf_prod_coupon.coupon;



src_mall.product
------------------
    select count(*) from src_mall.product;
    
    select min(dt) dt_min,
    max(dt) dt_max,
    min(op_time) op_time_min,
    max(op_time) op_time_max 
    from src_mall.product;


src_qf_prod_coupon.coupon_store_rule
------------------
    select count(*) from src_qf_prod_coupon.coupon_store_rule;

    select min(dt) dt_min,
    max(dt) dt_max,
    min(op_time) op_time_min,
    max(op_time) op_time_max from src_qf_prod_coupon.coupon_store_rule;



src_qf_prod_coupon.coupon_stock
------------------
    select count(*) from src_qf_prod_coupon.coupon_stock;

    select min(dt) dt_min,
    max(dt) dt_max,
    min(op_time) op_time_min,
    max(op_time) op_time_max from src_qf_prod_coupon.coupon_stock;














