### Darwin 扩展

代码|<p/>
:---:|:---:
`ui`|Darwin UI 名称空间
`core`|Darwin Core 名称空间
`drawable`|Darwin Drawable 名称空间
`black`|黑色
`white`|白色
`red`|红色
`green`|绿色
`blue`|蓝色
`pink`|粉色
`yellow`|黄色
`cyan`|青色
`[pixel] pixel(char,[color] front,[color] back)`|创建一个像素
`[drawable] picture(number width,number height)`|创建一幅图片(`Drawable`)
`void load()`|加载 Darwin 功能
`void exit()`|退出 Darwin 功能
`boolean is_kb_hit()`|判断是否有按键按下
`char get_kb_hit()`|获取按下的按键
`void fit_drawable()`|使画布适合当前屏幕大小
`[drawable] get_drawable()`|获取画布
`void update_drawable()`|将画布中的内容更新至屏幕上
`void set_frame_limit(number fps)`|设置帧率
`void set_draw_line_precision(number)`|设置画线精度

#### Darwin UI 名称空间

代码|<p/>
:---:|:---:
`void message_box(string title,string message,string button)`|弹出一个消息对话框
`var input_box(string title,string message,string default,boolean format)`|弹出一个输入对话框

#### Darwin Core 名称空间

代码|<p/>
:---:|:---:
`char get_char([pixel])`|获取像素的字符
`void set_char([pixel],char)`|设置像素的字符
`[color] get_front_color([pixel])`|获取像素的前景色
`void set_front_color([pixel],[color])`|设置像素的前景色
`[color] get_back_color([pixel])`|获取像素的背景色
`void set_back_color([pixel],[color])`|设置像素的背景色

### Darwin Drawable 名称空间

代码|<p/>
:---:|:---:
`void load_from_file([drawable],string path)`|从指定路径加载图片(Darwin CDPF 图片文件)
`void save_to_file([drawable],string path)`|将图片保存至指定路径(Darwin CDPF 图片文件)
`void clear([drawable])`|清空画布
`void fill([drawable],[pixel])`|填充画布
`void resize([drawable],number width,number height)`|重新设置画布大小
`number get_width([drawable])`|获取画布宽度
`number get_height([drawable])`|获取画布高度
`[pixel] get_pixel([drawable],number x,number y)`|获取画布上的点
`void draw_pixel([drawable],number x,number y,[pixel])`|在画布上画点
`void draw_line([drawable],number x1,number y1,number x2,number y2,[pixel])`|在画布上画线
`void draw_rect([drawable],number x,number y,number width,number height,[pixel])`|在画布上绘制线框
`void fill_rect([drawable],number x,number y,number width,number height,[pixel])`|在画布上填充矩形
`void draw_triangle([drawable],number x1,number y1,number x2,number y2,number x3,number y3,[pixel])`|在画布上绘制三角形
`void fill_triangle([drawable],number x1,number y1,number x2,number y2,number x3,number y3,[pixel])`|在画布上填充三角形
`void draw_string([drawable],number x,number y,string,[pixel])`|在画布上绘制文字
`void draw_picture([drawable],number x,number y,[drawable])`|将一幅图片绘制到画布上

**注意:
Darwin 扩展会抛出异常。**