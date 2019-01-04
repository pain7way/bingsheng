app_compass.baseinfo_goods
------------------
    select count(*) from app_compass.baseinfo_goods;
    select min(now_date),max(now_date),min(op_time),max(op_time) from app_compass.baseinfo_goods;
    
    select coupon_id,
    plaza_id,
    coupon_type,
    sale_price,
    face_value,
    show_begin_time,
    show_end_time,
    coupon_title 
    from app_compass.baseinfo_goods where coupon_id=31180;


src_qianfan.wechat_mini_program_log
------------------
    select count(*) from src_qianfan.wechat_mini_program_log;
    select count(*) from src_qianfan.wechat_mini_program_log where plaza_id=1000772 and dt='2019-01-02';
    select count(*) from src_qianfan.wechat_mini_program_log where plaza_id=1000772 and dt='2018-12-31';
    select dt,count(*) from src_qianfan.wechat_mini_program_log where plaza_id=1000772 and dt like '2018-12-%' group by dt;
    select count(*) from src_qianfan.wechat_mini_program_log where plaza_id=1001145 and dt='2019-01-01';
    select * from src_qianfan.wechat_mini_program_log limit 1;
    select min(dt) dt_min,max(dt) dt_max from src_qianfan.wechat_mini_program_log;
    select distinct coupon_id from src_qianfan.wechat_mini_program_log where coupon_id is not null limit 50;
    select min(dt),max(dt) from src_qianfan.wechat_mini_program_log where coupon_id=063005385396;


src_basedata.base_store（通过门店id找到门店信息）
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
    select store_id,store_name,plaza_id,plaza_name from src_basedata.base_store where plaza_id=1000771;
    select store_id,store_name,plaza_id,plaza_name from src_basedata.base_store where store_id=100007644;
    select store_id,store_name,plaza_id,plaza_name from src_basedata.base_store where store_id=100002072;
    select store_id,store_name,plaza_id,plaza_name from src_basedata.base_store where store_id=100010747;



src_qf_prod_coupon.coupon（获取券的描述信息，只是9位数的券）
------------------
    select count(*) from src_qf_prod_coupon.coupon;
    
    select min(dt) min_dt,
    max(dt) max_dt,
    min(op_time) min_optime,
    max(op_time) max_optime 
    from src_qf_prod_coupon.coupon;



src_mall.product（5位数的券id转化为9位数的券id）
------------------
    select count(*) from src_mall.product;
    
    select min(dt) dt_min,max(dt) dt_max,min(op_time) op_time_min,max(op_time) op_time_max from src_mall.product;
    
    select spu_code,id from src_mall.product where id=29269;
    select spu_code,id from src_mall.product where spu_code=190130490;


src_qf_prod_coupon.coupon_store_rule(通过券id找到门店id，只是9位数的券id)
------------------
    select count(*) from src_qf_prod_coupon.coupon_store_rule;

    select min(dt) dt_min,
    max(dt) dt_max,
    min(op_time) op_time_min,
    max(op_time) op_time_max from src_qf_prod_coupon.coupon_store_rule;
    
    select csr_store_id,c_no from src_qf_prod_coupon.coupon_store_rule where c_no=190130490;



src_qf_prod_coupon.coupon_stock（获取券的库存，只是9位数的券id）
------------------
    select count(*) from src_qf_prod_coupon.coupon_stock;

    select min(dt) dt_min,
    max(dt) dt_max,
    min(op_time) op_time_min,
    max(op_time) op_time_max from src_qf_prod_coupon.coupon_stock;














