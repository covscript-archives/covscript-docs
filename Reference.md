# Covariant Script编程语言：参考文档 #
## 目录 ##
+ 语法
    + 预处理
    + 模块
    + 变量
    + 作用域
    + 流控制
    + 函数
    + 异常
    + 结构
+ API
    + 标准库
    + 扩展库
        + ImGui
        + Darwin
        + Regex
        + Streams
        + SQLite
        + Network
    + 第三方库
        + Picasso
        + Asserts
        + JVM
+ 解释器
    + 命令行参数
    + 扩展库开发
        + Callable对象
        + C/C++ Native Interface
        + 类型扩展
            + 支持`this`
            + 定制名称
            + 规定行为 
    + 解释器API
        + 运行文件
        + 运行语句
        + 运行时交互
            + 获取/增添变量
            + 调用Covariant Script函数
            + 定制运行环境
    + 二次开发
        + 项目结构
        + Covariant Mozart程序库
        + 类型系统
        + 函数和FFI
            + Callable对象
            + Covariant Script函数
            + C/C++ Native Interface
        + 扩展系统
        + 预处理
        + 词法分析
        + 语法分析
        + 代码生成
            + AST构建
            + 优化器
            + 生成目标代码
        + 运行时实例
            + 代码运行
            + AST求值
        + REPL