1. 技术栈
   - Spring Cloud + Spring Boot + MyBatis-Plus + MySQL + Kafka + Redis +  Elasticsearch + Kafka Stream + XXL-JOB + MongoDB + Docker + Jenkins 
2. 主要职能
   - 完成项目需求分析和技术方案设计，完成数据库设计和技术选型。
   - 微服务拆分：用户个人服务、文章服务、自媒体服务、用户行为服务、检索服务、评论服务、平台管理服务等。
   - 整合MongoDB，以非结构化数据存储用户评论、评论点赞、评论回复等数据；
   - 使用 Kafka 实现自媒体文章上下架的异步处理。
   - 使用Redis设计限流组件，针对用户行为，如：频繁点赞、评论、发送验证码登行为进行时间窗口限流；
   - 使用XXL-JOB设计定时任务场景，例如：定时文章发布、定时同步Redis数据到MySQL、定时计算热点文章等等；
   - 使用 Elasticsearch 实现文章搜索功能，并优化搜索性能。
   - 使用 Kafka Stream 进行实时数据分析，为推荐系统提供数据支持。
   - 使用 Docker 进行项目部署，并使用 Jenkins 实现持续集成和持续交付。
