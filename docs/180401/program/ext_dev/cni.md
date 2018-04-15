# C/C++ Native Interface
> 定义于头文件`<covscript/cni.hpp>`

**C/C++ Native Interface**，简称**CNI**，是CovScript中一种特殊的[Callable对象](http://covscript.org/docs/180401/program/ext_dev/callable)。  
CNI可以说是CovScript与原生语言交互的主要渠道，因为CNI能够转发来自Callable对象的调用到任意普通C++函数上。相对于普通的Callable对象，CNI的使用门槛要低的多，你只需要确保你绑定到CNI上的函数不是模板函数或者是重载函数即可。  
CNI的性能理论上可能相对于直接使用Callable对象要低一些，因为CNI强制对参数合法性进行检查，而且展开参数的过程也需要一定的运行时开销。但事实上CNI所带来的性能损失比用户自己展开参数列表要小得多，而且安全性也能得到保证。  

## 成员类型
> 无

## 成员对象
> 无

## 成员函数
```
cni() = delete;
```
默认构造函数（删除）
```
cni(const cni &);
```
复制构造函数
```
template<typename T> cni(T &&val)
```
构造一个CNI并将参数指定的函数绑定在CNI上
```
~cni();
```
析构函数
```
cs::var operator()(cs::vector &args) const
```
调用操作符重载函数，这使得CNI成为能被Callable对象识别的可调用对象