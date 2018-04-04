# Callable对象
> 定义于头文件`<covscript/core.hpp>`

**Callable对象**是Covariant Script中的可调用对象，在C++中表示为`cs::var(cs:vector&)`。凡是符合这个函数签名的对象，包括普通函数，Lambda表达式以及含有`operator()`的可调用对象都可以保存为Callable对象。
## 成员类型
```
function_type
```  
定义为`std::function<cs::var(cs::vector &)>`
## 成员对象
```
enum class types
```    
Callable类型
+ `types::normal` 普通函数
+ `types::constant` 常量函数（可编译期调用）
+ `types::member_fn` 成员函数
## 成员函数
```
callable() = delete;
```  
默认构造函数（删除）
```
callable(const callable &);
```  
复制构造函数
```
callable(const function_type &func, bool constant = false);
```  
构造一个Callable对象，第二个参数将决定这个Callable是否能在编译期被调用（设置为`true`即为可被调用）
```
callable(const function_type &func, types type);
```  
构造一个Callable对象，第二个参数为这个Callable的类型
```
bool is_constant() const;
```  
判断是否为常量函数
```
bool is_member_fn() const;
```  
判断是否为成员函数
```
cs::var call(cs::vector &args) const;
```  
调用Callable并返回其返回值