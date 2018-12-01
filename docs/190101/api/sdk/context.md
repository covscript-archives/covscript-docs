# Covariant Script SDK文档
## Context(解释器上下文环境)
Context(解释器上下文环境)是Covariant Script 3中非常重要和基础的组件之一  
![](http://covscript.org/docs/190101/api/sdk/framework.png)  
图示为Covariant Script 3的架构
所以要运行文件，首先要创建解释器上下文环境。创建上下文环境相关的函数一共有三个：
> 定义于头文件`<covscript/covscript.hpp>`

```c++
cs::array cs::parse_cmd_args(int, const char *[]);
cs::context_t cs::create_context(const cs::array &);
cs::context_t cs::create_subcontext(const cs::context_t &);
```
第一个函数用于将main函数的参数解析为cs::array  
第二个函数是创建一个独立的上下文环境，需要传入运行参数
第三个函数是创建一个依赖于另外一个上下文环境的子上下文环境，它会与父环境共享一定的资源，比如Covariant Script解释器在引入包文件时创建的就是子上下文环境

## 范例
```c++
#include <covscript/covscript.hpp>
int main(int argc, const char *argv[])
{
    if (argc <= 1)
        return -1;
    cs::context_t context = cs::create_context(cs::parse_cmd_args(argc - 1, argv + 1));
    context->instance->compile(argv[1]);
    context->instance->interpret();
    cs::function_invoker<cs::number(cs::number, cs::number)> test(context, "test");
    int result = test(1, 2);
    cs::function_invoker<void(cs::number)> println(context, "system.out.println");
    println(result);
    return 0;
}
```
在这个例子中我们首先创建了一个上下文环境，编译并解释了一个Covariant Script程序，并与这个程序交互  
Covariant Script调用C++的函数在以前的版本中已经非常方便，但在Covariant Script 3中我们又加入了cs::function_invoker简化了C++调用Covariant Script中函数的过程  
由于Covariant Script的函数都是动态类型，没有固定的返回类型和参数类型，所以cs::function_invoker的模板参数中填写的参数仅为期望，我们称之为期望函数类型(Expected Function Type,EFT)。明显的，同一个函数可能拥有无数种EFT，按需声明即可。不同EFT的cs::function_invoker之间**不可以**相互赋值。