﻿# TiDB 中文技术文档

## 目录

+ 关于 TiDB
  - [TiDB 简介](overview.md)
  - [TiDB 整体架构](architecture.md)
  - [TiDB 核心特性](features.md)
+ TiDB 快速入门
  - [快速入门指南](QUICKSTART.md)
  - [SQL 基本操作](try-tidb.md)
+ TiDB 用户文档
  + TiDB 数据库管理
    - [TiDB 服务](sql/tidb-server.md)
    - [TiDB 进程启动参数](sql/server-command-option.md)
    - [TiDB 数据目录](sql/tidb-server.md#tidb-数据目录)
    - [TiDB 系统数据库](sql/system-database.md)
    - [TiDB 系统变量](sql/variable.md)
    - [TiDB 专用系统变量和语法](sql/tidb-specific.md)
    - [TiDB 服务器日志文件](sql/tidb-server.md#tidb-服务器日志文件)
    - [TiDB 访问权限管理](sql/privilege.md)
    - [TiDB 用户账户管理](sql/user-account-management.md)
    - [使用加密连接](sql/encrypted-connections.md)
  + TiDB SQL 优化和执行
    - [SQL 优化流程简介](sql/sql-optimizer-overview.md)
    - [理解 TiDB 执行计划](sql/understanding-the-query-execution-plan.md)
    - [统计信息](sql/statistics.md)
  + 语言结构
    - [字面值](sql/literal-values.md)
    - [数据库、表、索引、列和别名](sql/schema-object-names.md)
    - [关键字和保留字](sql/keywords-and-reserved-words.md)
    - [用户变量](sql/user-defined-variables.md)
    - [表达式语法](sql/expression-syntax.md)
    - [注释语法](sql/comment-syntax.md)
  + 字符集和时区
    - [字符集支持](sql/character-set-support.md)
    - [字符集配置](sql/character-set-configuration.md)
    - [时区](sql/time-zone.md)
  + 数据类型
    - [数值类型](sql/datatype.md#数值类型)
    - [日期和时间类型](sql/date-and-time-types.md)
    - [字符串类型](sql/datatype.md#字符串类型)
    - [JSON 数据类型](sql/datatype.md#json-类型)
    - [枚举类型](sql/datatype.md#枚举类型)
    - [集合类型](sql/datatype.md#集合类型)
    - [数据类型默认值](sql/datatype.md#数据类型的默认值)
  + 函数和操作符
    - [函数和操作符概述](sql/functions-and-operators-reference.md)
    - [表达式求值的类型转换](sql/type-conversion-in-expression-evaluation.md)
    - [操作符](sql/operators.md)
    - [控制流程函数](sql/control-flow-functions.md)
    - [字符串函数](sql/string-functions.md)
    - [数值函数与操作符](sql/numeric-functions-and-operators.md)
    - [日期和时间函数](sql/date-and-time-functions.md)
    - [位函数和操作符](sql/bit-functions-and-operators.md)
    - [Cast 函数和操作符](sql/cast-functions-and-operators.md)
    - [加密和压缩函数](sql/encryption-and-compression-functions.md)
    - [信息函数](sql/information-functions.md)
    - [JSON 函数](sql/json-functions.md)
    - [GROUP BY 聚合函数](sql/aggregate-group-by-functions.md)
    - [其他函数](sql/miscellaneous-functions.md)
    - [精度数学](sql/precision-math.md)
  + SQL 语句语法
    - [数据定义语句 (DDL)](sql/ddl.md)
    - [数据操作语句 (DML)](sql/dml.md)
    - [事务语句](sql/transaction.md)
    - [数据库管理语句](sql/admin.md)
    - [Prepared SQL 语句语法](sql/prepare.md)
    - [实用工具语句](sql/util.md)
    - [TiDB SQL 语法图](https://pingcap.github.io/sqlgram/)
  - [Generated Column](sql/generated-columns.md)
  - [Connectors 和 API](sql/connection-and-APIs.md)
  - [TiDB 事务隔离级别](sql/transaction-isolation.md)
  - [错误码与故障诊断](sql/error.md)
  - [与 MySQL 兼容性对比](sql/mysql-compatibility.md)
  - [TiDB 内存控制](sql/tidb-memory-control.md)
  - [慢查询日志](sql/slow-query.md)
  + 高级功能
    - [历史数据回溯](op-guide/history-read.md)
    - [垃圾回收 (GC)](op-guide/gc.md)
+ TiDB 运维文档
  - [软硬件环境需求](op-guide/recommendation.md)
  + 部署集群
    - [Ansible 部署方案（强烈推荐）](op-guide/ansible-deployment.md)
    - [离线 Ansible 部署方案](op-guide/offline-ansible-deployment.md)
    - [Docker 部署方案](op-guide/docker-deployment.md)
    - [Docker Compose 部署方案](op-guide/docker-compose.md)
    - [跨数据中心部署方案](op-guide/cross-dc-deployment.md)
  + 配置集群
    - [参数解释](op-guide/configuration.md)
    - [TiDB 配置项解释](op-guide/tidb-config-file.md)
    - [使用 Ansible 变更组件配置](op-guide/ansible-deployment-rolling-update.md#变更组件配置)
    - [开启 TLS 验证](op-guide/security.md)
    - [生成自签名证书](op-guide/generate-self-signed-certificates.md)
    - [集群拓扑结构配置](op-guide/location-awareness.md)
  + 监控集群
    - [整体监控框架概述](op-guide/monitor-overview.md)
    + 重要监控指标详解
      - [Overview](op-guide/dashboard-overview-info.md)
      - [TiDB](op-guide/tidb-dashboard-info.md)
      - [PD](op-guide/dashboard-pd-info.md)
      - [TiKV](op-guide/dashboard-tikv-info.md)
    - [组件状态 API & 监控](op-guide/monitor.md)
  + 扩容缩容
    - [集群扩容缩容方案](op-guide/horizontal-scale.md)
    - [使用 Ansible 扩容缩容](op-guide/ansible-deployment-scale.md)
  + 升级
    - [升级组件版本](op-guide/ansible-deployment-rolling-update.md#升级组件版本)
    - [TiDB 2.0 升级操作指南](op-guide/tidb-v2.0-upgrade-guide.md)
    - [TiDB 2.1 升级操作指南](op-guide/tidb-v2.1-upgrade-guide.md)
  - [性能调优](op-guide/tune-tikv.md)
  + 备份与迁移
    - [备份与恢复](op-guide/backup-restore.md)
    + 数据迁移
      - [数据迁移概述](op-guide/migration-overview.md)
      - [全量导入](op-guide/migration.md#使用-mydumperloader-全量导入数据)
      - [增量导入](op-guide/migration.md#使用-syncer-增量导入数据)
  - [故障诊断](trouble-shooting.md)
+ TiDB 周边工具
  - [Syncer](tools/syncer.md)
  - [mydumper](tools/mydumper.md)
  - [Loader](tools/loader.md)
  + Data Migration
    - [简介](tools/dm/overview.md)
    - [使用限制](tools/dm/overview.md#使用限制)
    - [使用 DM 同步数据](tools/dm/practice.md)
    - 配置
      - [任务配置](tools/dm/task-configuration-file-intro.md)
  + TiDB-Lightning
    - [简介](tools/lightning/overview-architecture.md)
    - [部署执行](tools/lightning/deployment.md)
    - [断点续传](tools/lightning/checkpoints.md)
    - [表库过滤](tools/lightning/filter.md)
    - [监控告警](tools/lightning/monitor.md)
    - [故障诊断](tools/lightning/errors.md)
    - [常见问题与解答](tools/lightning/faq.md)
  - [TiDB-Binlog](tools/tidb-binlog-cluster.md)
  - [PD Control](tools/pd-control.md)
  - [PD Recover](tools/pd-recover.md)
  - [TiKV Control](tools/tikv-control.md)
  - [TiDB Controller](tools/tidb-controller.md)
  - [工具下载](tools/download.md)
+ TiSpark 文档
  - [TiSpark 快速入门指南](tispark/tispark-quick-start-guide.md)
  - [TiSpark 用户指南](tispark/tispark-user-guide.md)
- [常见问题与解答(FAQ)](FAQ.md)
- [最佳实践](https://pingcap.com/blog-cn/tidb-best-practice/)
+ [版本发布历史](releases/rn.md)
  - [2.1.5](releases/2.1.5.md)
  - [2.1.4](releases/2.1.4.md)
  - [2.1.3](releases/2.1.3.md)
  - [3.0 Beta](releases/3.0beta.md)
  - [2.0.11](releases/2.0.11.md)
  - [2.1.2](releases/2.1.2.md)
  - [2.0.10](releases/2.0.10.md)
  - [2.1.1](releases/2.1.1.md)
  - [2.1 GA](releases/2.1ga.md)
  - [2.0.9](releases/209.md)
  - [2.1 RC5](releases/21rc5.md)
  - [2.1 RC4](releases/21rc4.md)
  - [2.0.8](releases/208.md)
  - [2.1 RC3](releases/21rc3.md)
  - [2.1 RC2](releases/21rc2.md)
  - [2.0.7](releases/207.md)
  - [2.1 RC1](releases/21rc1.md)
  - [2.0.6](releases/206.md)
  - [2.0.5](releases/205.md)
  - [2.1 Beta](releases/21beta.md)
  - [2.0.4](releases/204.md)
  - [2.0.3](releases/203.md)
  - [2.0.2](releases/202.md)
  - [2.0.1](releases/201.md)
  - [2.0](releases/2.0ga.md)
  - [2.0 RC5](releases/2rc5.md)
  - [2.0 RC4](releases/2rc4.md)
  - [2.0 RC3](releases/2rc3.md)
  - [2.0 RC1](releases/2rc1.md)
  - [1.1 Beta](releases/11beta.md)
  - [1.1 Alpha](releases/11alpha.md)
  - [1.0](releases/ga.md)
  - [Pre-GA](releases/prega.md)
  - [RC4](releases/rc4.md)
  - [RC3](releases/rc3.md)
  - [RC2](releases/rc2.md)
  - [RC1](releases/rc1.md)
- [TiDB 路线图](ROADMAP.md)
+ 用户案例
  - [北京银行](http://t.cn/RnY8fGn)
  - [海航](http://t.cn/REXx0Qe)
  - [美团点评](http://t.cn/EAFCqhl)
  - [今日头条](http://t.cn/RnLfEMf)
  - [转转](http://t.cn/R1MAXEq)
  - [Mobike](http://t.cn/RT8FbP6)
  - [饿了么（一）](http://t.cn/RucuK6m)
  - [饿了么（二）](http://t.cn/RnsqFT6)
  - [小米科技](http://t.cn/Ey2xCDK)
  - [爱奇艺](http://t.cn/EvErsc1)
  - [易果生鲜](http://t.cn/RTYVhzH)
  - [同程旅游（一）](http://t.cn/RmXeNKR)
  - [同程旅游（二）](http://t.cn/EAmsF08)
  - [去哪儿](http://t.cn/RTKnsL7)
  - [火星文化](http://t.cn/EAuvfcs)
  - [G7](http://t.cn/RQVePoX)
  - [一面数据](http://t.cn/RT9r5di)
  - [凤凰网](http://t.cn/RHRQfNT)
  - [猿辅导](http://t.cn/RTKnKSX)
  - [Mobikok](http://t.cn/Rm1F6lg)
  - [二维火](http://t.cn/R8bXM2f)
  - [客如云](http://t.cn/R1wSEJH)
  - [Ping++](http://t.cn/RE5xYKn)
  - [乐视云](http://t.cn/Rnv3IVs)
  - [零氪科技](http://t.cn/REj7tSv)
  - [威锐达测控](http://t.cn/R3CrviR)
  - [盖娅互娱](http://t.cn/RT9r7hx)
  - [游族网络](http://t.cn/R8k4AWB)
  - [西山居](http://t.cn/RBP12zj)
  - [FUNYOURS JAPAN](http://t.cn/Rnoab5D)
  - [丰巢科技](http://t.cn/EAuvLIv)
  - [特来电](http://t.cn/RrHzUGW)
  - [万达网络](http://t.cn/RTKm6ds)
  - [360金融](http://t.cn/RTKnTev)
  - [中国电信翼支付](http://t.cn/R3Wd9p3)
  - [某电信运营商](http://t.cn/RTYWADg)
+ 更多资源
  - [PingCAP 团队技术博客](https://pingcap.com/blog-cn/)
  - [知乎专栏](https://zhuanlan.zhihu.com/newsql)
  - [Weekly](https://pingcap.com/weekly/)
  - [英文文档](https://pingcap.com/docs)
