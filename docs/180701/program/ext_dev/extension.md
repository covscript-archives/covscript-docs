# Covariant Script扩展
Covariant Script扩展是基于动态链接库实现的功能扩展系统，Covariant Script通过模块系统将模块接入主程序。  
Covariant Script扩展包括了常规扩展和类型扩展，这里我们介绍的是常规扩展。  
## 头文件和依赖
理论上编写Covariant Script扩展只需要`<covscript/extension.hpp>`和Covariant Script核心组件，但由于Covariant Script核心组件依赖`Mozart`,`LibDLL`和`sparsepp`等，请务必完整安装Covariant Script SDK。  
如果你已经完整安装了Covariant Script SDK，你只需要包含`<covscript/extension.hpp>`即可。  
Covariant Script使用的标准是C++11，请使用较新的编译器以支持全部功能。  
## 扩展类
Covariant Script要求每个扩展至少有一个静态的扩展类对象以供CovariantScript模块系统读取。
> 定义于头文件`<covscript/core.hpp>`

**注意，`cs::extension`是`cs::name_space`的别名**
### 成员类型
> 无

### 成员函数
```
name_space();
```
默认构造函数
```
name_space(const name_space &) = delete;
```
复制构造函数（删除）
```
name_space(const cs::domain_t &);
```
使用已有的作用域构造一个名称空间对象
```
~name_space();
```
析构函数
```
void add_var(const std::string &, const cs::var &)
```
增加新变量
```
cs::var &get_var(const std::string &)
```
获取名称空间中的变量
```
cs::domain_t get_domain() const
```
获取名称空间对应的作用域

## 扩展主函数