1. 技术栈
   - Spring Boot + MyBatis-Plus + MySQL + Redis + Nginx + RabbitMQ + HttpClient + Docker
2. 主要职能
   - 负责技术选型、框架搭建、需求评审、工期评估、核心业务开发；
   - 通过阿里 OSS 技术实现⽂件上传下载以及云存储功能。
   - 对接物联网设备接入平台API，实现基于MQTT的物联网数据（光照，温度，湿度等）属性实时上报，物联网命令下发终端实时控制。
   - 基于历史数据训练LSTM用电量预测模型，通过HttpClient封装TensorFlow Serving推理接口，实现未来24小时能耗峰谷预警，辅助策略生成准确率达88%。
   - 使用Nginx作为Http服务器，部署静态资源，实现Tomcat的负载均衡，以及反向代理
   - 使用Apache POI，封装了对Excel表格的常用操作，用于时段用电量异常数据的导出。
   - 研发办公设备能效动态评分模型，利用 Redis ZSET 实时排序设备能耗效率，结合 RocketMQ 延迟消息 实现空调、照明等设备的定时调控策略，综合节能率提升 22%。

