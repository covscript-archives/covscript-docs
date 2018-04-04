# 参考文档
此文档对应Covariant Script标准`180401`
## 版权信息

版权所有 © 2018 Michael Lee(李登淳)  

此程序是免费软件：您可以根据自由软件基金会发布的 GNU Affero 通用公共许可协议（版本3的许可协议）或（可选）更新的版本对其进行重新分发和/或修改。  
我们在分发此程序时希望它会有用，但没有任何的保证; 甚至没有对适销性或特定用途的适用性的暗示保证。有关更多详细信息，请参阅 GNU Affero 通用公共许可协议。  
您应该收到 GNU Affero 通用公共许可协议的副本以及此程序。 如果没有，请参阅：http://www.gnu.org/licenses  
使用此程序即代表你同意并遵守 GNU Affero 通用公共许可协议的所有条款，保留所有权利。  

[Github主页](https://github.com/covscript)  
[Email](mailto:mikecovlee@163.com)

## 目录 ##
+ 类型
    + [数值类型](http://covscript.org/docs/180401/types/number)
    + [逻辑类型](http://covscript.org/docs/180401/types/boolean)
    + [指针类型](http://covscript.org/docs/180401/types/pointer)
    + [字符类型](http://covscript.org/docs/180401/types/char)
    + [文字类型](http://covscript.org/docs/180401/types/string)
    + [数组类型](http://covscript.org/docs/180401/types/array)
    + [线性表类型](http://covscript.org/docs/180401/types/list)
    + [映射类型](http://covscript.org/docs/180401/types/pair)
    + [散列表类型](http://covscript.org/docs/180401/types/hash_map)
+ 语法
    + [预处理](http://covscript.org/docs/180401/syntax/preprocessor)
    + [模块](http://covscript.org/docs/180401/syntax/modules)
    + [变量](http://covscript.org/docs/180401/syntax/variables)
    + [表达式](http://covscript.org/docs/180401/syntax/expression)
    + [作用域](http://covscript.org/docs/180401/syntax/domains)
    + [流控制](http://covscript.org/docs/180401/syntax/statements)
    + [函数](http://covscript.org/docs/180401/syntax/function)
    + [异常](http://covscript.org/docs/180401/syntax/exceptions)
    + [结构](http://covscript.org/docs/180401/syntax/structure)
+ API
    + 标准库
        + [全局](http://covscript.org/docs/180401/api/std/global)
        + [异常](http://covscript.org/docs/180401/api/std/exception)
        + [输入输出流](http://covscript.org/docs/180401/api/std/iostream)
        + [系统](http://covscript.org/docs/180401/api/std/system)
        + [运行时](http://covscript.org/docs/180401/api/std/runtime)
        + [数学](http://covscript.org/docs/180401/api/std/math)
        + [字符](http://covscript.org/docs/180401/api/std/char)
        + [文字](http://covscript.org/docs/180401/api/std/string)
        + [数组](http://covscript.org/docs/180401/api/std/array)
        + [线性表](http://covscript.org/docs/180401/api/std/list)
        + [映射](http://covscript.org/docs/180401/api/std/pair)
        + [散列表](http://covscript.org/docs/180401/api/std/hash_map)
    + 扩展库
        + [ImGui](http://covscript.org/docs/180401/api/ext/imgui)
        + [Darwin](http://covscript.org/docs/180401/api/ext/darwin)
        + [Regex](http://covscript.org/docs/180401/api/ext/regex)
        + [Streams](http://covscript.org/docs/180401/api/ext/streams)
        + [SQLite](http://covscript.org/docs/180401/api/ext/sqlite)
        + [Network](http://covscript.org/docs/180401/api/ext/network)
    + 第三方库
        + Picasso
        + Asserts
        + JVM
+ 解释器
    + 命令行参数
        + [解释器](http://covscript.org/docs/180401/program/cmd_args/cs)
        + [交互式解释器](http://covscript.org/docs/180401/program/cmd_args/cs_repl)
    + 扩展库开发
        + [Callable对象](http://covscript.org/docs/180401/program/ext_dev/callable)
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