# Covariant Script扩展
Covariant Script扩展是基于动态链接库实现的功能扩展系统，Covariant Script通过模块系统将模块接入主程序。  
Covariant Script扩展包括了常规扩展和类型扩展，这里我们介绍的是常规扩展。  
## 头文件和依赖
理论上编写Covariant Script扩展只需要`<covscript/dll.hpp>`和Covariant Script核心组件，但由于Covariant Script核心组件依赖`Mozart`,`LibDLL`和`sparsepp`等，请务必完整安装Covariant Script SDK。  
如果你已经完整安装了Covariant Script SDK，你只需要包含`<covscript/dll.hpp>`即可。  
Covariant Script使用的标准是C++11，请使用较新的编译器以支持全部功能。  
## 名称空间类
Covariant Script要求每个扩展至少有一个静态的扩展类对象以供CovariantScript模块系统读取。
> 定义于头文件`<covscript/core.hpp>`

### 成员类型
> 无

### 成员函数
```c++
name_space();
```
默认构造函数
****
```c++
name_space(const name_space &) = delete;
```
复制构造函数（删除）
****
```c++
explicit name_space(const cs::domain_t &);
```
使用已有的作用域构造一个名称空间对象
****
```c++
~name_space();
```
析构函数
****
```c++
name_space& add_var(const std::string &, const cs::var &);
```
增加新变量
****
```c++
cs::var &get_var(const std::string &);
const cs::var &get_var(const std::string &) const;
```
获取名称空间中的变量
****
```c++
cs::domain_t get_domain() const;
```
获取名称空间对应的作用域

## 扩展主函数
扩展主函数的功能主要是加载扩展的功能，Covariant Script扩展系统会传入一个名称空间类指针，只需将相关功能注册到里面即可。实际上还有一部分必需的Covariant Script功能在扩展主函数被调用之前会被自动加载。
扩展主函数的形式很简单：
```c++
void cs_extension_main(cs::name_space *my_ext_ns) {
    // TODO
}
```
其中，`my_ext_ns`是Covariant Script扩展系统传入的指向扩展根名称空间对象的指针，可以根据需要更换为其他名称。

## 范例：Hello，My extension
```c++
#include <covscript/dll.hpp>
#include <iostream>

void cs_extension_main(cs::name_space *my_ext_ns) {
    my_ext_ns->add_var("hello", cs::make_cni([]{
        std::cout<<"Hello, My extension"<<std::endl;
    }));
}
```
将此段代码保存并编译为动态链接库即可被Covariant Script扩展系统加载，注意在编译的时候要链接Covariant Script SDK提供的静态链接库。编译输出的文件需要重命名为`[Extension Name].cse`方便Covariant Script扩展系统识别，假设我们这里输出的文件为`my_ext.cse`，那么在Covariant Script中调用扩展功能就非常方便了：
```
import my_ext
my_ext.hello()
```
此程序会输出：`Hello, My extension`。  
**注意：可能需要使用运行参数指定import路径帮助Covariant Script扩展系统找到扩展。**