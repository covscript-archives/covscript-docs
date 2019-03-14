#### `iostream` 名称空间

代码|功能
:---:|:---:
`seekdir`|寻位方向名称空间
`openmode`|打开方式名称空间
`istream`|输入流名称空间
`ostream`|输出流名称空间
`[istream/ostream] fstream(string path,[openmode] mode)`|新建一个文件流,具体类型取决于打开方式
`void setprecision(number)`|设置输出精度(`to_string` 的精度)

#### 寻位方向名称空间

代码|功能
:---:|:---:
`start`|流的开始
`finish`|流的结尾
`present`|当前位置

#### 打开方式名称空间

代码|功能
:---:|:---:
`in`|为读打开(输入流)
`out`|为写打开(清空内容,输出流)
`app`|为写打开(追加内容,输出流)

#### 输入流名称空间

代码|功能
:---:|:---:
`char get([istream])`|读取字符
`char peek([istream])`|读取下一个字符而不删除
`void unget([istream])`|放回字符
`string getline([istream])`|读取一行
`number tell([istream])`|返回流位置指示器
`void seek([istream],number pos)`|设置流位置
`void seek_from([istream],[seekdir],number offset)`|设置相对寻位方向的流位置
`boolean good([istream])`|检查是否有错误
`boolean eof([istream])`|检查是否到达文件结尾
`var input([istream])`|从流中获取输入(格式化)
`void ignore([istream])`|忽略流中下一行前所有内容

#### 输出流名称空间

代码|功能
:---:|:---:
`void put([ostream],char)`|插入字符
`number tell([ostream])`|返回流位置指示器
`void seek([ostream],number pos)`|设置流位置
`void seek_from([ostream],[seekdir],number offset)`|设置相对寻位方向的流位置
`void flush([ostream])`|与底层存储设备同步
`boolean good([ostream])`|检查是否有错误
`void print([ostream],var)`|向流中输出内容,仅可输出支持 `to_string` 的类型(不换行)
`void println([ostream],var)`|向流中输出内容,仅可输出支持 `to_string` 的类型(换行)