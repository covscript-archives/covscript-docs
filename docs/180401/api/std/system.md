#### `system` 名称空间

代码|功能
:---:|:---:
`console`|控制台名称空间
`file`|文件名称空间
`path`|路径名称空间
`args`|运行参数(`Array`)
`in`|标准输入流
`out`|标准输出流
`number run(string)`|在系统环境中运行一条指令,返回错误码
`string getenv(string)`|获取环境变量的值并返回
`void exit(number)`|清理资源并退出

#### 控制台名称空间

代码|功能
:---:|:---:
`number terminal_width()`|获取控制台宽度
`number terminal_height()`|获取控制台高度
`void gotoxy(number x, number y)`|移动光标
`void echo(boolean)`|设置光标可见性
`void clrscr()`|清屏
`char getch()`|获取键盘输入
`bool kbhit()`|判断是否有键盘输入

#### 文件名称空间

代码|功能
:---:|:---:
`boolean copy(string,string)`|复制文件
`boolean remove(string)`|删除文件
`boolean exists(string)`|判断文件是否存在
`boolean rename(string,string)`|重命名/移动文件

### 路径名称空间

代码|功能
:---:|:---:
`type`|路径类型名称空间
`info`|路径信息名称空间
`separator`|路径分隔符
`delimiter`|路径定界符
`array scan(string)`|扫描路径

#### 路径类型名称空间

代码|功能
:---:|:---:
`unknown`|未知
`fifo`|管道
`sock`|套接字
`chr`|字符设备
`dir`|文件夹
`blk`|块设备
`reg`|常规
`lnk`|链接

#### 路径信息名称空间

代码|功能
:---:|:---:
`string name([path_info])`|获取路径名
`[path_type] type([path_info])`|获取路径类型