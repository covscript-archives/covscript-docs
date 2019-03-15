# 参考文档
此文档对应Covariant Script标准`190101`
## 版权信息

```
Licensed under the Covariant Innovation General Public License,
Version 1.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

https://covariant.cn/licenses/LICENSE-1.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

版权所有 © 2019 Michael Lee(李登淳)

使用此程序即代表你同意并遵守**智锐科创通用公共许可证**的所有条款，保留所有权利。  

[Github主页](https://github.com/covscript)  
[Email](mailto:mikecovlee@163.com)

## 目录 ##
+ 类型
    + [数值类型](./types/number)
    + [逻辑类型](./types/boolean)
    + [指针类型](./types/pointer)
    + [字符类型](./types/char)
    + [文字类型](./types/string)
    + [数组类型](./types/array)
    + [线性表类型](./types/list)
    + [映射类型](./types/pair)
    + [散列表类型](./types/hash_map)
+ 语法
    + [预处理](./syntax/preprocessor)
    + [模块](./syntax/modules)
    + [变量](./syntax/variables)
    + [表达式](./syntax/expression)
    + [作用域](./syntax/domains)
    + [流控制](./syntax/statements)
    + [函数](./syntax/function)
    + [异常](./syntax/exceptions)
    + [结构](./syntax/structure)
+ API
    + 标准库
        + [全局](./api/std/global)
        + [异常](./api/std/exception)
        + [输入输出流](./api/std/iostream)
        + [系统](./api/std/system)
        + [运行时](./api/std/runtime)
        + [数学](./api/std/math)
        + [字符](./api/std/char)
        + [文字](./api/std/string)
        + [数组](./api/std/array)
        + [线性表](./api/std/list)
        + [映射](./api/std/pair)
        + [散列表](./api/std/hash_map)
    + 扩展库
        + [ImGui](./api/ext/imgui)
        + [Darwin](./api/ext/darwin)
        + [Regex](./api/ext/regex)
        + [Codec](./api/ext/codec)
        + [Streams](./api/ext/streams)
        + [SQLite](./api/ext/sqlite)
        + [Network](./api/ext/network)
    + 第三方库
        + Picasso
        + Asserts
        + JVM
+ 解释器
    + 命令行参数
        + [解释器](./program/cmd_args/cs)
        + [交互式解释器](./program/cmd_args/cs_repl)
    + 扩展库开发
        + [Callable对象](./program/ext_dev/callable)
        + [C/C++ Native Interface](./program/ext_dev/cni)
        + [Covariant Script扩展](./program/ext_dev/extension)
        + 类型扩展
            + 支持`this`
            + 定制名称
            + 规定行为 
    + 解释器API
        + [运行文件](./api/sdk/context)
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