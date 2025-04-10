1. 技术栈
   - Spring Boot + MyBatis-Plus + MySQL + Redis + Redisson + Lua + HyperLogLog + Nginx
2. 主要职能
   - **短信登录**：基于Redis实现分布式Session，使用Token替代JSessionId，通过Hash结构存储用户信息并设置TTL，结合双拦截器实现无感知Token续期，解决集群环境下Session一致性问题，用户登录成功率100%。
   - **商户查询缓存**：设计多级缓存架构，集成布隆过滤器拦截无效请求（缓存穿透）、SETNX互斥锁与逻辑过期方案应对突发流量（缓存击穿）、随机TTL分散过期时间（缓存雪崩），商户详情页查询QPS提升300%。
   - **优惠券秒杀**：通过Redis原子操作（DECR）预减库存拦截超卖请求，结合Lua脚本实现“库存预减+订单创建+消息推送”原子操作；基于Redisson分布式锁解决集群环境锁误删问题，订单数据异步写入Redis Stream队列削峰，数据库压力降低70%。
   - **限流控制**：基于Redis滑动窗口算法限制用户高频操作（如频繁发送验证码），拦截恶意请求超90%，系统稳定性达99.99%。
   - **社交与统计功能**
     - 好友关注：基于Redis Set实现关注/取关，SINTERSTORE计算共同关注列表；
     - 签到与点赞：BitMap记录连续签到，BITFIELD快速统计周期数据，SortedSet实现点赞排行榜，List存储用户行为流水；
     - UV统计：HyperLogLog完成亿级用户访问去重统计，内存占用仅为传统方案的5%。
   - **地理位置检索**：通过GeoHash计算坐标哈希值，Redis GEO实现1km内商户毫秒级检索，响应时间≤50ms。
   - **缓存一致性**：采用“延时双删+MQ重试”策略保障数据库与缓存最终一致，结合Prometheus实时监控Redis内存及命中率，动态优化BigKey拆分策略。
