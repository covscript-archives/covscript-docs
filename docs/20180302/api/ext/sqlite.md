### SQLite 扩展

`statement`|SQLite 语句名称空间
`integer`|SQLite 整数类型
`real`|SQLite 浮点类型
`text`|SQLite 文本类型

`[sqlite] open(string path)`|打开或创建一个 SQLite 数据库
`[statement] prepare([sqlite] database,string sql)`|准备一个 SQLite 语句

#### SQLite 语句名称空间

代码|<p/>
:---:|:---:
`boolean done([statement])`|判断是否执行完毕
`void reset([statement])`|重置语句
`void exec([statement])`|执行语句
`number column_count([statement])`|获取记录数量
`[type] column_type([statement],number index)`|获取记录类型
`string column_name([statement],number index)`|获取记录名称
`string column_decltype([statement],number index)`|推导记录类型
`number column_integer([statement],number index)`|获取整数记录
`number column_real([statement],number index)`|获取浮点记录
`string column_text([statement],number index)`|获取文本记录
`number bind_param_count([statement])`|绑定参数数量
`void bind_integer([statement],number index,number data)`|绑定整数参数
`void bind_real([statement],number index,number data)`|绑定浮点参数
`void bind_text([statement],number index,string data)`|绑定文本参数
`void clear_bindings([statement])`|清除所有绑定

**注意:
SQLite 扩展会抛出异常。**