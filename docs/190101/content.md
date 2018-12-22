# 参考文档
此文档对应Covariant Script标准`190101`
## 版权信息

版权所有 © 2018 Michael Lee(李登淳)  

Licensed under the Apache License, Version 2.0 (the "License");  
you may not use this file except in compliance with the License.  
You may obtain a copy of the License at  
  
http://www.apache.org/licenses/LICENSE-2.0  
  
Unless required by applicable law or agreed to in writing, software  
distributed under the License is distributed on an "AS IS" BASIS,  
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
See the License for the specific language governing permissions and  
limitations under the License.  
  
使用此程序即代表你同意并遵守Apache许可协议的所有条款，保留所有权利。  

[Github主页](https://github.com/covscript)  
[Email](mailto:mikecovlee@163.com)

## 目录 ##
+ 类型
    + [数值类型](http://covscript.org/docs/190101/types/number)
    + [逻辑类型](http://covscript.org/docs/190101/types/boolean)
    + [指针类型](http://covscript.org/docs/190101/types/pointer)
    + [字符类型](http://covscript.org/docs/190101/types/char)
    + [文字类型](http://covscript.org/docs/190101/types/string)
    + [数组类型](http://covscript.org/docs/190101/types/array)
    + [线性表类型](http://covscript.org/docs/190101/types/list)
    + [映射类型](http://covscript.org/docs/190101/types/pair)
    + [散列表类型](http://covscript.org/docs/190101/types/hash_map)
+ 语法
    + [预处理](http://covscript.org/docs/190101/syntax/preprocessor)
    + [模块](http://covscript.org/docs/190101/syntax/modules)
    + [变量](http://covscript.org/docs/190101/syntax/variables)
    + [表达式](http://covscript.org/docs/190101/syntax/expression)
    + [作用域](http://covscript.org/docs/190101/syntax/domains)
    + [流控制](http://covscript.org/docs/190101/syntax/statements)
    + [函数](http://covscript.org/docs/190101/syntax/function)
    + [异常](http://covscript.org/docs/190101/syntax/exceptions)
    + [结构](http://covscript.org/docs/190101/syntax/structure)
+ API
    + 标准库
        + [全局](http://covscript.org/docs/190101/api/std/global)
        + [异常](http://covscript.org/docs/190101/api/std/exception)
        + [输入输出流](http://covscript.org/docs/190101/api/std/iostream)
        + [系统](http://covscript.org/docs/190101/api/std/system)
        + [运行时](http://covscript.org/docs/190101/api/std/runtime)
        + [数学](http://covscript.org/docs/190101/api/std/math)
        + [字符](http://covscript.org/docs/190101/api/std/char)
        + [文字](http://covscript.org/docs/190101/api/std/string)
        + [数组](http://covscript.org/docs/190101/api/std/array)
        + [线性表](http://covscript.org/docs/190101/api/std/list)
        + [映射](http://covscript.org/docs/190101/api/std/pair)
        + [散列表](http://covscript.org/docs/190101/api/std/hash_map)
    + 扩展库
        + [ImGui](http://covscript.org/docs/190101/api/ext/imgui)
        + [Darwin](http://covscript.org/docs/190101/api/ext/darwin)
        + [Regex](http://covscript.org/docs/190101/api/ext/regex)
        + [Codec](http://covscript.org/docs/190101/api/ext/codec)
        + [Streams](http://covscript.org/docs/190101/api/ext/streams)
        + [SQLite](http://covscript.org/docs/190101/api/ext/sqlite)
        + [Network](http://covscript.org/docs/190101/api/ext/network)
    + 第三方库
        + Picasso
        + Asserts
        + JVM
+ 解释器
    + 命令行参数
        + [解释器](http://covscript.org/docs/190101/program/cmd_args/cs)
        + [交互式解释器](http://covscript.org/docs/190101/program/cmd_args/cs_repl)
    + 扩展库开发
        + [Callable对象](http://covscript.org/docs/190101/program/ext_dev/callable)
        + [C/C++ Native Interface](http://covscript.org/docs/190101/program/ext_dev/cni)
        + [Covariant Script扩展](http://covscript.org/docs/190101/program/ext_dev/extension)
        + 类型扩展
            + 支持`this`
            + 定制名称
            + 规定行为 
    + 解释器API
        + [运行文件](http://covscript.org/docs/190101/api/sdk/context)
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