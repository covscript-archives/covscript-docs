## 版权信息 ##

版权所有 © 2018 Michael Lee(李登淳)  

此程序是免费软件：您可以根据自由软件基金会发布的 GNU Affero 通用公共许可协议（版本3的许可协议）或（可选）更新的版本对其进行重新分发和/或修改。  
我们在分发此程序时希望它会有用，但没有任何的保证; 甚至没有对适销性或特定用途的适用性的暗示保证。有关更多详细信息，请参阅 GNU Affero 通用公共许可协议。  
您应该收到 GNU Affero 通用公共许可协议的副本以及此程序。 如果没有，请参阅：http://www.gnu.org/licenses  
使用此程序即代表你同意并遵守 GNU Affero 通用公共许可协议的所有条款，保留所有权利。  

[Github主页](https://github.com/covscript)  
[Email](mailto:mikecovlee@163.com)

## 目录 ##
+ 类型
    + [数值类型](http://covscript.org/docs/types/number)
    + [逻辑类型](http://covscript.org/docs/types/boolean)
    + [指针类型](http://covscript.org/docs/types/pointer)
    + [字符类型](http://covscript.org/docs/types/char)
    + [文字类型](http://covscript.org/docs/types/string)
    + [数组类型](http://covscript.org/docs/types/array)
    + [线性表类型](http://covscript.org/docs/types/list)
    + [映射类型](http://covscript.org/docs/types/pair)
    + [散列表类型](http://covscript.org/docs/types/hash_map)
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