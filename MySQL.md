# MySQL

## MySQL 5.7 官方文档笔记

### 目录

- 前言与法律声明
- 1. General Information
    - 1.1 About This Manual
    - 1.2 Overview of the MySQL Database Management System
    - 1.3 What Is New in MySQL 5.7
    - 1.4 Server and Status Variables and Options Added, Deprecated, or Removed in MySQL 5.7
    - 1.5 MySQL Information Sources
    - 1.6 How to Report Bugs or Problems
    - 1.7 MySQL Standards Compliance
    - 1.8 Credits

- 2. 安装与升级
  - 2.1 General Installation Guidance
  - 2.2 Installing MySQL on Unix/Linux Using Generic Binaries
  - 2.3 Installing MySQL on Microsoft Windows
  - 2.4 Installing MySQL on macOS
  - 2.5 Installing MySQL on Linux
  - 2.6 Installing MySQL Using Unbreakable Linux Network (ULN)
  - 2.7 Installing MySQL on Solaris
  - 2.8 Installing MySQL on FreeBSD
  - 2.9 Installing MySQL from Source
  - 2.10 Postinstallation Setup and Testing
  - 2.11 Upgrading MySQL
  - 2.12 Downgrading MySQL
  - 2.13 Perl Installation Notes

- 3. 教程

  - 3.1 连接与断开服务器/Connecting to and Disconnecting from the Server
  - 3.2 输入查询/Entering Queries
  - 3.3 创建和使用一个数据库/Creating and Using a Database

    - 3.3.1 创建和选择数据库/Creating and Selecting a Database
    - 3.3.2 创建表/Creating a Table
    - 3.3.3 加载数据到表/Loading Data into a Table
    - 3.3.4 从表中提取信息/Retrieving Information from a Table

  - 3.4 获取数据库或表的信息/Getting Information About Databases and Tables
  - 3.5 批处理模式/Using mysql in Batch Mode
  - 3.6 常用查询示例/Examples of Common Queries

    - 3.6.1 列的最大值/The Maximum Value for a Column
    - 3.6.2 包含指定列最大值的行/The Row Holding the Maximum of a Certain Column
    - 3.6.3 每组列的最大值/Maximum of Column per Group
    - 3.6.4 每一组包含指定列最大值的行/The Rows Holding the Group-wise Maximum of a Certain Column
    - 3.6.5 使用用户定义变量/Using User-Defined Variables
    - 3.6.6 使用外键/Using Foreign Keys
    - 3.6.7 搜索两个关键词/Searching on Two Keys
    - 3.6.8 计算每天访问数/Calculating Visits Per Day
    - 3.6.9 使用AUTO_INCREMENT/Using AUTO_INCREMENT

  - 3.7 MySQL与Apache结合/Using MySQL with Apache

- 4. MySQL程序
    
  - 4.1 概览/Overview of MySQL Programs
  - 4.2 使用MySQL程序/Using MySQL Programs

    - 4.2.1 调用MySQL程序/Invoking MySQL Programs
    - 4.2.2 指定程序选项/Specifying Program Options

      - 4.2.2.1 命令行参数/Using Options on the Command Line
      - 4.2.2.2 使用配置文件/Using Option Files
      - 4.2.2.3 影响配置文件处理的命令行参数/Command-Line Options that Affect Option-File Handling
      - 4.2.2.4 参数修饰符/Program Option Modifiers
      - 4.2.2.5 使用参数来设置程序变量/Using Options to Set Program Variables
      - 4.2.2.6 参数默认值、期望值和`=`/Option Defaults, Options Expecting Values, and the = Sign

    - 4.2.3 连接服务器命令参数/Command Options for Connecting to the Server
    - 4.2.4 使用命令参数连接服务器/Connecting to the MySQL Server Using Command Options
    - 4.2.5 连接传输层协议/Connection Transport Protocols
    - 4.2.6 连接压缩控制/Connection Compression Control
    - 4.2.7 设置环境变量/Setting Environment Variables

  - 4.3 Server和Server启动程序/Server and Server-Startup Programs

    - 4.3.1 服务器/mysqld — The MySQL Server
    - 4.3.2 mysqld_safe — MySQL Server Startup Script
    - 4.3.3 mysql.server — MySQL Server Startup Script
    - 4.3.4 mysqld_multi — Manage Multiple MySQL Servers

  - 4.4 MySQL安装相关程序/Installation-Related Programs

    - 4.4.1 编译MySQL错误消息文件/comp_err — Compile MySQL Error Message File
    - 4.4.2 舒适化MySQL数据目录/mysql_install_db — Initialize MySQL Data Directory
    - 4.4.3 配置插件/mysql_plugin — Configure MySQL Server Plugins
    - 4.4.4 增强MySQL安装安全性/mysql_secure_installation — Improve MySQL Installation Security
    - 4.4.5 创建SSL/RSA文件/mysql_ssl_rsa_setup — Create SSL/RSA Files
    - 4.4.6 加载时区表/mysql_tzinfo_to_sql — Load the Time Zone Tables
    - 4.4.7 检查更新MySQL表/mysql_upgrade — Check and Upgrade MySQL Tables

  - 4.5 客户端/Client Programs

    - 4.5.1 命令行客户端/mysql — The MySQL Command-Line Client

      - 4.5.1.1 客户端参数/mysql Client Options
      - 4.5.1.2 客户端命令/mysql Client Commands
      - 4.5.1.3 客户端日志/mysql Client Logging
      - 4.5.1.4 客户端的服务端帮助/mysql Client Server-Side Help
      - 4.5.1.5 执行文本文件中的SQL语句/Executing SQL Statements from a Text File
      - 4.5.1.6 客户端注意事项/mysql Client Tips

    - 4.5.2 服务器管理程序/mysqladmin — A MySQL Server Administration Program
    - 4.5.3 表维护程序/mysqlcheck — A Table Maintenance Program
    - 4.5.4 数据库备份程序/mysqldump — A Database Backup Program
    - 4.5.5 数据导入程序/mysqlimport — A Data Import Program
    - 4.5.6 数据库备份程序/mysqlpump — A Database Backup Program
    - 4.5.7 显示数据库、表、列信息/mysqlshow — Display Database, Table, and Column Information
    - 4.5.8 负载仿真客户端/mysqlslap — A Load Emulation Client

  - 4.6 管理与实用工具/Administrative and Utility Programs

    - 4.6.1 离线InnoDB文件校验实用工具/innochecksum — Offline InnoDB File Checksum Utility
    - 4.6.2 显示选文索引信息/myisam_ftdump — Display Full-Text Index information
    - 4.6.3 MyISAM表维护工具/myisamchk — MyISAM Table-Maintenance Utility

      - 4.6.3.1 常规选项/myisamchk General Options
      - 4.6.3.2 检查选项/myisamchk Check Options
      - 4.6.3.3 修复选项/myisamchk Repair Options
      - 4.6.3.4 其他选项/Other myisamchk Options
      - 4.6.3.5 获取表信息/Obtaining Table Information with myisamchk
      - 4.6.3.6 内存使用/myisamchk Memory Usage

    - 4.6.4 显示MyISAM日志文件内容/myisamlog — Display MyISAM Log File Contents
    - 4.6.5 生成压缩只读MyISAM表/myisampack — Generate Compressed, Read-Only MyISAM Tables
    - 4.6.6 MySQL配置实用工具/mysql_config_editor — MySQL Configuration Utility
    - 4.6.7 二进制日志文件处理实用工具/mysqlbinlog — Utility for Processing Binary Log Files

      - 4.6.7.1 十六进制格式/mysqlbinlog Hex Dump Format
      - 4.6.7.2 行事件显示/mysqlbinlog Row Event Display
      - 4.6.7.3 备份二进制日志文件/Using mysqlbinlog to Back Up Binary Log Files
      - 4.6.7.4 指定Server ID/Specifying the mysqlbinlog Server ID

    - 4.6.8 慢日志文件总结/mysqldumpslow — Summarize Slow Query Log Files

  - 4.7 程序开发实用工具/Program Development Utilities

    - 4.7.1 显示编译的客户端选项/mysql_config — Display Options for Compiling Clients
    - 4.7.2 显示配置文件选项/my_print_defaults — Display Options from Option Files
    - 4.7.3 将StackTrace的值解析为符号/resolve_stack_dump — Resolve Numeric Stack Trace Dump to Symbols

  - 4.8 其他程序/Miscellaneous Programs

    - 4.8.1 解压mysqldump的lz4压缩包/lz4_decompress — Decompress mysqlpump LZ4-Compressed Output
    - 4.8.2 显示MySQL错误消息信息/perror — Display MySQL Error Message Information
    - 4.8.3 字符串替换/replace — A String-Replacement Utility
    - 4.8.4 主机名和IP解析互转/resolveip — Resolve Host name to IP Address or Vice Versa
    - 4.8.5 解压mysqldump的zlib压缩包/zlib_decompress — Decompress mysqlpump ZLIB-Compressed Output

  - 4.9 环境变量/Environment Variables
  - 4.10 Unix信号处理/Unix Signal Handling in MySQL

- 5. MySQL服务器管理
    
  - 5.1 服务器/The MySQL Server

    - 5.1.1 配置MySQL服务器/Configuring the Server
    - 5.1.2 默认配置/Server Configuration Defaults
    - 5.1.3 服务器选项、系统变量、状态变量参考/Server Option, System Variable, and Status Variable Reference
    - 5.1.4 系统变量参考/Server System Variable Reference
    - 5.1.5 状态变量参考/Server Status Variable Reference
    - 5.1.6 命令选项/Server Command Options
    - 5.1.7 服务器系统变量/Server System Variables
    - 5.1.8 使用系统变量/Using System Variables

      - 5.1.8.1 系统变量权限/System Variable Privileges
      - 5.1.8.2 动态系统变量/Dynamic System Variables
      - 5.1.8.3 结构化系统变量/Structured System Variables

    - 5.1.9 服务器状态变量/Server Status Variables
    - 5.1.10 服务器SQL模式/Server SQL Modes
    - 5.1.11 连接管理/Connection Management

      - 5.1.11.1 连接接口/Connection Interfaces
      - 5.1.11.2 DNS查询和主机缓存/DNS Lookups and the Host Cache

    - 5.1.12 IPv6支持/IPv6 Support

      - 5.1.12.1 确认系统是否支持IPv6/Verifying System Support for IPv6
      - 5.1.12.2 配置MySQL服务器允许IPv6连接/Configuring the MySQL Server to Permit IPv6 Connections
      - 5.1.12.3 使用IPv6本机地址连接/Connecting Using the IPv6 Local Host Address
      - 5.1.12.4 使用IPv6非本地地址连接/Connecting Using IPv6 Nonlocal Host Addresses
      - 5.1.12.5 从Broker处获取IPv6地址/Obtaining an IPv6 Address from a Broker

    - 5.1.13 时区支持/MySQL Server Time Zone Support
    - 5.1.14 服务端帮助支持/Server-Side Help Support
    - 5.1.15 服务端跟踪客户端会话状态变更/Server Tracking of Client Session State Changes
    - 5.1.16 服务端关闭流程/The Server Shutdown Process

  - 5.2 数据目录/The MySQL Data Directory
  - 5.3 `mysql`系统数据库/The mysql System Database
  - 5.4 服务器日志/MySQL Server Logs

    - 5.4.1 查询一般查询日志和慢查询日志输出位置/Selecting General Query Log and Slow Query Log Output Destinations
    - 5.4.2 错误日志/The Error Log

      - 5.4.2.1 Error Logging on Windows
      - 5.4.2.2 Error Logging on Unix and Unix-Like Systems
      - 5.4.2.3 日志输出到系统日志/Error Logging to the System Log
      - 5.4.2.4 错误日志过滤/Error Log Filtering
      - 5.4.2.5 错误日志输出格式/Error Log Output Format
      - 5.4.2.6 错误日志刷盘和重命名/Error Log File Flushing and Renaming

    - 5.4.3 一般查询日志/The General Query Log
    - 5.4.4 二进制日志/The Binary Log

      - 5.4.4.1 二进制日志格式/Binary Logging Formats
      - 5.4.4.2 二进制日志格式设置/Setting The Binary Log Format
      - 5.4.4.3 混合二进制日志格式/Mixed Binary Logging Format
      - 5.4.4.4 `mysql`数据库中的表的变更日志格式/Logging Format for Changes to `mysql` Database Tables

    - 5.4.5 慢查询日志/The Slow Query Log
    - 5.4.6 DDL日志/The DDL Log
    - 5.4.7 服务端日志维护/Server Log Maintenance

  - 5.5 服务器插件/MySQL Server Plugins

    - 5.5.1 安装与卸载/Installing and Uninstalling Plugins
    - 5.5.2 获取服务器插件信息/Obtaining Server Plugin Information
    - 5.5.3 MySQL Enterprise Thread Pool

      - 5.5.3.1 Thread Pool Elements
      - 5.5.3.2 Thread Pool Installation
      - 5.5.3.3 Thread Pool Operation
      - 5.5.3.4 Thread Pool Tuning

    - 5.5.4 查询重写插件/The Rewriter Query Rewrite Plugin

      - 5.5.4.1 安装与卸载/Installing or Uninstalling the Rewriter Query Rewrite Plugin
      - 5.5.4.2 使用/Using the Rewriter Query Rewrite Plugin
      - 5.5.4.3 参考/Rewriter Query Rewrite Plugin Reference

    - 5.5.5 Version Tokens

      - 5.5.5.1 Version Tokens Elements
      - 5.5.5.2 Installing or Uninstalling Version Tokens
      - 5.5.5.3 Using Version Tokens
      - 5.5.5.4 Version Tokens Reference

    - 5.5.6 MySQL Plugin Services

      - 5.5.6.1 The Locking Service
      - 5.5.6.2 The Keyring Service

  - 5.6 服务器用户定义函数/MySQL Server User-Defined Functions

    - 5.6.1 安装与卸载/Installing and Uninstalling User-Defined Functions
    - 5.6.2 获取用户定义函数信息/Obtaining User-Defined Function Information

  - 5.7 单机多实例/Running Multiple MySQL Instances on One Machine

    - 5.7.1 设置多个数据目录/Setting Up Multiple Data Directories
    - 5.7.2 Running Multiple MySQL Instances on Windows

      - 5.7.2.1 Starting Multiple MySQL Instances at the Windows Command Line
      - 5.7.2.2 Starting Multiple MySQL Instances as Windows Services

    - 5.7.3 在Unix环境下运行多实例/Running Multiple MySQL Instances on Unix
    - 5.7.4 在多实例下使用客户端程序/Using Client Programs in a Multiple-Server Environment

  - 5.8 调试/Debugging MySQL

    - 5.8.1 调试MySQL服务器/Debugging a MySQL Server

      - 5.8.1.1 编译调试版MySQL/Compiling MySQL for Debugging
      - 5.8.1.2 创建跟踪文件/Creating Trace Files
      - 5.8.1.3 Using WER with PDB to create a Windows crashdump
      - 5.8.1.4 gdb下调试mysqld/Debugging mysqld under gdb
      - 5.8.1.5 使用Stack Trace/Using a Stack Trace
      - 5.8.1.6 利用服务器日志寻找mysqld错误原因/Using Server Logs to Find Causes of Errors in mysqld
      - 5.8.1.7 表损坏时创建一个测试用例/Making a Test Case If You Experience Table Corruption

    - 5.8.2 调试MySQL客户端/Debugging a MySQL Client
    - 5.8.3 DBUG包/The DBUG Package
    - 5.8.4 使用DTrace跟踪mysqld/Tracing mysqld Using DTrace

      - 5.8.4.1 mysqld DTrace探针参考/mysqld DTrace Probe Reference

- 6. 安全
    
  - 6.1 一般安全问题/General Security Issues
  - 6.2 访问控制与账号管理/Access Control and Account Management
  - 6.3 使用加密连接/Using Encrypted Connections
  - 6.4 安全插件/Security Plugins
  - 6.5 MySQL Enterprise Data Masking and De-Identification
  - 6.6 MySQL Enterprise Encryption
  - 6.7 SELinux

- 7. 备份与恢复
    
  - 7.1 备份与恢复类型/Backup and Recovery Types
  - 7.2 备份方法/Database Backup Methods
  - 7.3 备份示例与恢复策略/Example Backup and Recovery Strategy
  - 7.4 使用`mysqldump`进行备份/Using mysqldump for Backups
  - 7.5 增量恢复/Point-in-Time (Incremental) Recovery
  - 7.6 MyISAM表维护与灾难恢复/MyISAM Table Maintenance and Crash Recovery

- 8. 优化

  - 8.1 优化概览/Optimization Overview
  - 8.2 优化SQL语句/Optimizing SQL Statements
  - 8.3 优化与索引/Optimization and Indexes
  - 8.4 数据库结构优化/Optimizing Database Structure
  - 8.5 InnoDB表优化/Optimizing for InnoDB Tables
  - 8.6 MyISAM表优化/Optimizing for MyISAM Tables
  - 8.7 MEMORY表优化/Optimizing for MEMORY Tables
  - 8.8 理解查询执行计划/Understanding the Query Execution Plan
  - 8.9 控制查询优化器/Controlling the Query Optimizer
  - 8.10 缓冲和缓存/Buffering and Caching
  - 8.11 锁优化/Optimizing Locking Operations
  - 8.12 MySQL Server优化/Optimizing the MySQL Server
  - 8.13 性能测量/Measuring Performance (Benchmarking)
  - 8.14 检查服务器线程信息/Examining Server Thread (Process) Information

- 9. 语言结构

  - 9.1 字面值/Literal Values
  - 9.2 Schema对象名/Schema Object Names
  - 9.3 关键字和保留字/Keywords and Reserved Words
  - 9.4 用户定义变量/User-Defined Variables
  - 9.5 表达式/Expressions
  - 9.6 备注/Comments

- 10. 字符集、校对、Unicode

  - 10.1 常规字符集和校对/Character Sets and Collations in General
  - 10.2 MySQL中的字符集和校对/Character Sets and Collations in MySQL
  - 10.3 指定字符集和校对/Specifying Character Sets and Collations
  - 10.4 连接字符集和校对/Connection Character Sets and Collations
  - 10.5 配置字符集和校对/Configuring Application Character Set and Collation
  - 10.6 错误消息字符集/Error Message Character Set
  - 10.7 列字符集约定/Column Character Set Conversion
  - 10.8 校对问题/Collation Issues
  - 10.9 Unicode支持/Unicode Support
  - 10.10 支持的字符集和校对/Supported Character Sets and Collations
  - 10.11 字符集限制/Restrictions on Character Sets
  - 10.12 设置错误消息语言/Setting the Error Message Language
  - 10.13 添加字符集/Adding a Character Set
  - 10.14 为字符集添加校对/Adding a Collation to a Character Set
  - 10.15 字符集配置/Character Set Configuration
  - 10.16 MySQL服务器区域设定支持/MySQL Server Locale Support

- 11. 数据类型

  - 11.1 数值类型/Numeric Data Types
  - 11.2 日期与时间/Date and Time Data Types
  - 11.3 字符串/String Data Types
  - 11.4 空间类型/Spatial Data Types
  - 11.5 JSON/The JSON Data Type
  - 11.6 默认值/Data Type Default Values
  - 11.7 存储要求/Data Type Storage Requirements
  - 11.8 为列选择合适的数据类型/Choosing the Right Type for a Column
  - 11.9 使用其他数据库引擎的数据类型/Using Data Types from Other Database Engines

- 12. 函数与运算符

  - 12.1 SQL函数与运算符参考/SQL Function and Operator Reference
  - 12.2 用户定义函数参考/User-Defined Function Reference
  - 12.3 表达式求值中的类型转换/Type Conversion in Expression Evaluation
  - 12.4 运算符/Operators
  - 12.5 流程控制函数/Flow Control Functions
  - 12.6 数值函数与运算符/Numeric Functions and Operators
  - 12.7 日期与时间函数/Date and Time Functions
  - 12.8 字符串函数和运算符/String Functions and Operators
  - 12.9 MySQL使用的日历/What Calendar Is Used By MySQL?
  - 12.10 全文搜索函数/Full-Text Search Functions
  - 12.11 类型转换函数与运算符/Cast Functions and Operators
  - 12.12 XML函数/XML Functions
  - 12.13 位操作函数与运算符/Bit Functions and Operators
  - 12.14 加密与压缩函数/Encryption and Compression Functions
  - 12.15 锁/Locking Functions
  - 12.16 Information Functions
  - 12.17 空间分析函数/Spatial Analysis Functions
  - 12.18 JSON函数/JSON Functions
  - 12.19 Functions Used with Global Transaction Identifiers (GTIDs)
  - 12.20 聚集函数/Aggregate Functions
  - 12.21 其他函数/Miscellaneous Functions
  - 12.22 Precision Math

- 13. SQL语句

  - 13.1 数据定义语句/Data Definition Statements
  - 13.2 数据操作语句/Data Manipulation Statements
  - 13.3 事务与锁/Transactional and Locking Statements
  - 13.4 复制/Replication Statements
  - 13.5 准备语句/Prepared Statements
  - 13.6 复合语句/Compound Statements
  - 13.7 数据库管理语句/Database Administration Statements
  - 13.8 Utility Statements

- 14. InnoDB存储引擎

  - 14.1 InnoDB介绍/Introduction to InnoDB
  - 14.2 InnoDB与ACID模型/InnoDB and the ACID Model
  - 14.3 InnoDB多版本/InnoDB Multi-Versioning
  - 14.4 InnoDB架构/InnoDB Architecture
  - 14.5 InnoDB内存结构/InnoDB In-Memory Structures
  - 14.6 InnoDB外存结构/InnoDB On-Disk Structures
  - 14.7 InnoDB锁与事务模型/InnoDB Locking and Transaction Model
  - 14.8 InnoDB配置/InnoDB Configuration
  - 14.9 InnoDB表与页压缩/InnoDB Table and Page Compression
  - 14.10 InnoDB文件格式管理/InnoDB File-Format Management
  - 14.11 InnoDB行格式/InnoDB Row Formats
  - 14.12 InnoDB磁盘I/O与文件空间管理/InnoDB Disk I/O and File Space Management
  - 14.13 InnoDB和在线DDL/InnoDB and Online DDL
  - 14.14 InnoDB Data-at-Rest Encryption
  - 14.15 InnoDB启动配置与系统变量/InnoDB Startup Options and System Variables
  - 14.16 InnoDB`INFORMATION_SCHEMA`表/InnoDB INFORMATION_SCHEMA Tables
  - 14.17 InnoDB与Performance Schema集成/InnoDB Integration with MySQL Performance Schema
  - 14.18 InnoDB监视器/InnoDB Monitors
  - 14.19 InnoDB备份与恢复/InnoDB Backup and Recovery
  - 14.20 InnoDB与复制/InnoDB and MySQL Replication
  - 14.21 InnoDB memcached插件/InnoDB memcached Plugin
  - 14.22 InnoDB排错/InnoDB Troubleshooting
  - 14.23 InnoDB Limits
  - 14.24 InnoDB Restrictions and Limitations

- 15. 可选存储引擎

  - 15.1 设置存储引擎/Setting the Storage Engine
  - 15.2 The MyISAM Storage Engine
  - 15.3 The MEMORY Storage Engine
  - 15.4 The CSV Storage Engine
  - 15.5 The ARCHIVE Storage Engine
  - 15.6 The BLACKHOLE Storage Engine
  - 15.7 The MERGE Storage Engine
  - 15.8 The FEDERATED Storage Engine
  - 15.9 The EXAMPLE Storage Engine
  - 15.10 其他存储引擎/Other Storage Engines
  - 15.11 MySQL存储引擎架构概览/Overview of MySQL Storage Engine Architecture

- 16. 复制（Replication）

  - 16.1 配置/Configuring Replication
  - 16.2 实现/Replication Implementation
  - 16.3 解决方案/Replication Solutions
  - 16.4 注意事项/Replication Notes and Tips

- 17. 组复制（Group Replication）

  - 17.1 背景/Group Replication Background
  - 17.2 Getting Started
  - 17.3 监控/Monitoring Group Replication
  - 17.4 操作/Group Replication Operations
  - 17.5 安全/Group Replication Security
  - 17.6 系统变量/Group Replication System Variables
  - 17.7 要求与限制/Requirements and Limitations
  - 17.8 常见问题/Frequently Asked Questions
  - 17.9 技术细节/Group Replication Technical Details

- 18. MySQL Shell

- 19. 将MySQL作为文档存储

  - 19.1 关键概念/Key Concepts
  - 19.2 将MySQL设置为文档存储/Setting Up MySQL as a Document Store
  - 19.3 MySQL for Visual Studio快速指南/Quick-Start Guide: MySQL for Visual Studio
  - 19.4 X Plugin

- 20. MySQL NDB Cluster 7.5 and NDB Cluster 7.6

  - 20.1 NDB Cluster Overview
  - 20.2 NDB Cluster Installation
  - 20.3 Configuration of NDB Cluster
  - 20.4 NDB Cluster Programs
  - 20.5 Management of NDB Cluster
  - 20.6 NDB Cluster Replication
  - 20.7 NDB Cluster Release Notes

- 21. 分区（Partitioning）

  - 21.1 MySQL分区概览/Overview of Partitioning in MySQL
  - 21.2 分区类型/Partitioning Types
  - 21.3 分区管理/Partition Management
  - 21.4 Partition Pruning
  - 21.5 Partition Selection
  - 21.6 分区限制/Restrictions and Limitations on Partitioning

- 22. 存储对象（Stored Objects）

  - 22.1 定义存储程序/Defining Stored Programs
  - 22.2 使用存储过程/Using Stored Routines
  - 22.3 使用触发器/Using Triggers
  - 22.4 使用事件调度器/Using the Event Scheduler
  - 22.5 使用视图/Using Views
  - 22.6 存储对象访问控制/Stored Object Access Control
  - 22.7 存储程序二进制日志/Stored Program Binary Logging
  - 22.8 存储程序限制/Restrictions on Stored Programs
  - 22.9 视图限制/Restrictions on Views

- 23. INFORMATION_SCHEMA 表

  - 23.1 简介/Introduction
  - 23.2 The INFORMATION_SCHEMA CHARACTER_SETS Table
  - 23.3 The INFORMATION_SCHEMA COLLATIONS Table
  - 23.4 The INFORMATION_SCHEMA COLLATION_CHARACTER_SET_APPLICABILITY Table
  - 23.5 The INFORMATION_SCHEMA COLUMNS Table
  - 23.6 The INFORMATION_SCHEMA COLUMN_PRIVILEGES Table
  - 23.7 The INFORMATION_SCHEMA ENGINES Table
  - 23.8 The INFORMATION_SCHEMA EVENTS Table
  - 23.9 The INFORMATION_SCHEMA FILES Table
  - 23.10 The INFORMATION_SCHEMA GLOBAL_STATUS and SESSION_STATUS Tables
  - 23.11 The INFORMATION_SCHEMA GLOBAL_VARIABLES and SESSION_VARIABLES Tables
  - 23.12 The INFORMATION_SCHEMA KEY_COLUMN_USAGE Table
  - 23.13 The INFORMATION_SCHEMA ndb_transid_mysql_connection_map Table
  - 23.14 The INFORMATION_SCHEMA OPTIMIZER_TRACE Table
  - 23.15 The INFORMATION_SCHEMA PARAMETERS Table
  - 23.16 The INFORMATION_SCHEMA PARTITIONS Table
  - 23.17 The INFORMATION_SCHEMA PLUGINS Table
  - 23.18 The INFORMATION_SCHEMA PROCESSLIST Table
  - 23.19 The INFORMATION_SCHEMA PROFILING Table
  - 23.20 The INFORMATION_SCHEMA REFERENTIAL_CONSTRAINTS Table
  - 23.21 The INFORMATION_SCHEMA ROUTINES Table
  - 23.22 The INFORMATION_SCHEMA SCHEMATA Table
  - 23.23 The INFORMATION_SCHEMA SCHEMA_PRIVILEGES Table
  - 23.24 The INFORMATION_SCHEMA STATISTICS Table
  - 23.25 The INFORMATION_SCHEMA TABLES Table
  - 23.26 The INFORMATION_SCHEMA TABLESPACES Table
  - 23.27 The INFORMATION_SCHEMA TABLE_CONSTRAINTS Table
  - 23.28 The INFORMATION_SCHEMA TABLE_PRIVILEGES Table
  - 23.29 The INFORMATION_SCHEMA TRIGGERS Table
  - 23.30 The INFORMATION_SCHEMA USER_PRIVILEGES Table
  - 23.31 The INFORMATION_SCHEMA VIEWS Table
  - 23.32 InnoDB相关表/INFORMATION_SCHEMA InnoDB Tables
  - 23.33 线程池相关表/INFORMATION_SCHEMA Thread Pool Tables
  - 23.34 连接控制相关表/INFORMATION_SCHEMA Connection-Control Tables
  - 23.35 INFORMATION_SCHEMA MySQL Enterprise Firewall Tables
  - 23.36 Show语句扩展/Extensions to SHOW Statements

- 24. MySQL Performance Schema

  - 24.1 快速入门/Performance Schema Quick Start
  - 24.2 构建配置/Performance Schema Build Configuration
  - 24.3 启动配置/Performance Schema Startup Configuration
  - 24.4 运行时配置/Performance Schema Runtime Configuration
  - 24.5 查询/Performance Schema Queries
  - 24.6 Instrument命名约定/Performance Schema Instrument Naming Conventions
  - 24.7 状态监控/Performance Schema Status Monitoring
  - 24.8 原子与分子事件/Performance Schema Atom and Molecule Events
  - 24.9 当前和历史事件/Performance Schema Tables for Current and Historical Events
  - 24.10 语句摘要/Performance Schema Statement Digests
  - 24.11 Performance Schema General Table Characteristics
  - 24.12 Performance Schema Table Descriptions
  - 24.13 选项与变量参考/Performance Schema Option and Variable Reference
  - 24.14 命令选项/Performance Schema Command Options
  - 24.15 系统变量/Performance Schema System Variables
  - 24.16 状态变量/Performance Schema Status Variables
  - 24.17 内存分配模型/The Performance Schema Memory-Allocation Model
  - 24.18 插件/Performance Schema and Plugins
  - 24.19 使用Performance Schema进行问题诊断/Using the Performance Schema to Diagnose Problems
  - 24.20 Migrating to Performance Schema System and Status Variable Tables
  - 24.21 限制/Restrictions on Performance Schema

- 25. MySQL sys Schema

  - 25.1 使用sys要求/Prerequisites for Using the sys Schema
  - 25.2 使用`sys` schema/Using the sys Schema
  - 25.3 进度报告/sys Schema Progress Reporting
  - 25.4 `sys`对象参考/sys Schema Object Reference

- 26. Connectors and APIs

  - 26.1 MySQL Connector/C++
  - 26.2 MySQL Connector/J
  - 26.3 MySQL Connector/NET
  - 26.4 MySQL Connector/ODBC
  - 26.5 MySQL Connector/Python
  - 26.6 libmysqld, the Embedded MySQL Server Library
  - 26.7 MySQL C API
  - 26.8 MySQL PHP API
  - 26.9 MySQL Perl API
  - 26.10 MySQL Python API
  - 26.11 MySQL Ruby APIs
  - 26.12 MySQL Tcl API
  - 26.13 MySQL Eiffel Wrapper

- 27. MySQL Enterprise Edition

  - 27.1 MySQL Enterprise Monitor Overview
  - 27.2 MySQL Enterprise Backup Overview
  - 27.3 MySQL Enterprise Security Overview
  - 27.4 MySQL Enterprise Encryption Overview
  - 27.5 MySQL Enterprise Audit Overview
  - 27.6 MySQL Enterprise Firewall Overview
  - 27.7 MySQL Enterprise Thread Pool Overview
  - 27.8 MySQL Enterprise Data Masking and De-Identification Overview

- Chapter 28 MySQL Workbench
- Appendix A MySQL 5.7 Frequently Asked Questions
- Appendix B Error Messages and Common Problems
- Appendix C Indexes
- MySQL Glossary