#### `runtime` 名称空间

代码|<p/>
:---:|:---:
`std_version`|标准版本号(`Number`)
`void info()`|解释器版本信息
`string get_import_path()`|获取引入目录
`number time()`|获取计时器的读数,单位毫秒
`void delay(number)`|使程序暂停一段时间,单位毫秒
`[exception] exception(string)`|新建运行时异常
`[hash_value] hash(var)`|计算一个变量的哈希值
`[expression] build([context],string)`|构建一个可用于计算的表达式
`var solve([context],[expression])`|计算一个表达式
`[namespace] dynamic_import([context],string path,string name)`|动态加载一个扩展,规则与 import 语句相同