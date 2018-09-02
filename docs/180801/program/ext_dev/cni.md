# C/C++ Native Interface
> 定义于头文件`<covscript/cni.hpp>`

**C/C++ Native Interface**，简称**CNI**，是CovScript中一种特殊的[Callable对象](http://covscript.org/docs/180801/program/ext_dev/callable)。  
CNI可以说是CovScript与原生语言交互的主要渠道，因为CNI能够转发来自Callable对象的调用到任意普通C++函数上。相对于普通的Callable对象，CNI的使用门槛要低的多，你只需要确保你绑定到CNI上的函数不是模板函数或者是重载函数即可。  
CNI的性能理论上可能相对于直接使用Callable对象要低一些，因为CNI强制对参数合法性进行检查，而且展开参数的过程也需要一定的运行时开销。但事实上CNI所带来的性能损失比用户自己展开参数列表要小得多，而且安全性也能得到保证。  
在最新版本的Covariant Script中CNI加入了对类型转换的支持，用户将能够自定义转换的类型和方式从而大幅度降低移植成本。  

## 成员类型
> 无

## 成员对象
> 无

## 成员函数
```c++
cni() = delete;
```
默认构造函数（删除）

****

```c++
cni(const cni &);
```
复制构造函数

****

```c++
template<typename T> cni(T &&val)
```
构造一个CNI并将参数指定的函数绑定在CNI上，此函数将应用全局设定的转换规则

****

```c++
template<typename T, typename X> cni(T &&val, cs::cni_type<X>);
```  
构造一个CNI并将参数指定的函数绑定在CNI上，此函数将应用自定义的转换规则。自定义转换规则由`cs::cni_type`指定，需要将函数类型作为模板参数传入，形式如下：
```c++
cs::cni_type<Return_Type(Argument_List...)>
```
应用此参数将直接跳过CNI的自动转换规则

****

```c++
~cni();
```
析构函数

****

```c++
cs::var operator()(cs::vector &args) const
```
调用操作符重载函数，这使得CNI成为能被Callable对象识别的可调用对象

## 公共函数
在实际应用中我们几乎不会遇到直接构造CNI的情况，所以CovScript提供了更方便的公共函数，可以直接构造能够被读取的Callable对象。