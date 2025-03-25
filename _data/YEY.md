1. 技术栈：
   - SpringBoot + MyBatis-Plus + Redis + Nginx + RabbitMq + MySql + Ruoyi
2. 主要职能
   - 开发 **图像合规性校验模块**，集成阿里云OSS存储医疗商品资质文件，通过 **MD5指纹比对** + Redis布隆过滤器拦截重复文件上传，存储成本降低35%
   - 实现 **Redis Lua脚本+分布式锁** 的库存扣减方案，解决保健品秒杀场景下的超卖问题，2000 QPS压力测试下数据一致性达99.99%
   - 实现 **方案时效性控制**，采用Redis Hash存储方案有效期，结合ZSET自动清理过期方案，内存占用减少40%
