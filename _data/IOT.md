1. 技术栈
   - Spring Boot + MyBatis-Plus + MySQL + Redis + Docker + Nginx + RabbitMQ + OkHttp 
2. 主要职能
   - 主导碳核算引擎的后端架构设计，研发智能碳效分析算法，通过对接生态环境部碳监测平台API，实现企业级碳排放数据的实时采集与标准化处理。
   - 基于 OkHttp 对接政府碳监测平台 API，使用 ReentrantLock + 双重校验 解决 Token 并发刷新问题，接口响应时间稳定在 200ms 内，支撑 1000+ 物联网终端设备并发上报。
   - 研发办公设备能效动态评分模型，利用 Redis ZSET 实时排序设备能耗效率，结合 RocketMQ 延迟消息 实现空调、照明等设备的定时调控策略，综合节能率提升 22%。

