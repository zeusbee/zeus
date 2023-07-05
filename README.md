# zeus 介绍
Zeus (宙斯)古希腊神话中，众神之王。拥有强大的能力维持天地间秩序。数据服务zeus（统一数据服务平台） 将拥有强大的数据聚合、集成、加工能力，提供业务稽核、数据可视化、用户画像、统一数据API、实施监测、风控策略等一系列衍生产品。（是一个美好的愿望。。。。）
# zeus 适用场景
* 业户稽核
* 数据可视化、数据地图
* 用户画像
* 实施监测
* 智能营销、自动化营销
* 实时检测
* 统一数据服务API

# zeus 架构
[zeus架构图](https://www.processon.com/diagraming/64a449e9db2f304bcc2b7d39 "zeus")

* 数据源：db binlong,MQ(Kafka,RocketMQ)，dubbo,http 等，可按需求自由扩展SDK
* 数据加工层：Flink 任务完成数据加工处理，实时、离线数据处理完成后统一存储
* 物理存储层：加工后的数据存储在屋里存储层，可按照应用场景，实时性要求选择CH,Redis,MongoDB ，Hadoop 等存储介质
* 逻辑存储层：从提供的数据服务出发，提供所需的数据视图，一个视图可以对应一个或多个物理存储单元。逻辑存储基于db，table 实现，数据服务查询数据基于逻辑存储层db.table 方式查询数据
* 数据映射层：维护逻辑存储层和物理存储层关系，逻辑存储层：物理存储层=1:n (emm..有必要吗？会不会引发其他问题？)

# 技术选型
整体架构细化、拆分完成再定。大方向按架构图为准。

# TBD
| Task  | Owner |状态  | 备注 |
|  ----  | ----  |  ----  | ----  |
|架构设计  | 艾尼 |doing  |  |
