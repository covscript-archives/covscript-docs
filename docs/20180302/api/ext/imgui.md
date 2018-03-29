# ImGui 扩展

代码|功能
:---:|:---:
application|应用程序名称空间
bmp_image|位图名称空间
keys|特殊键名称空间
dirs|方位名称空间
flags|窗口参数名称空间
### OPEN GL 函数

代码|功能
:---:|:---:
`number get_monitor_count()`|获取屏幕数量
`number get_monitor_width(number monitor_id)`|获取指定屏幕的宽度
`number get_monitor_height(number monitor_id)`|获取指定屏幕的高度
### 应用程序

代码|功能
:---:|:---:
`[application] fullscreen_application(number monitor_id,string title)`|创建全屏应用
`[application] window_application(number width,number height,string title)`|创建窗口应用
`[image] load_bmp_image(string path)`|加载 24bit 位图
`[vec2] vec2(number a,number b)`|创建二维向量
`[vec4] vec4(number a,number b,number c,number d)`|创建四维向量
`number get_framerate()`|获取帧率
### 样式

代码|功能
:---:|:---:
`void add_font(string str,number size)`|增加字体
`void style_color_classic()`|切换到经典配色
`void style_color_light()`|切换到亮色配色
`void style_color_dark()`|切换到暗色配色
### 窗口

代码|功能
:---:|:---:
`void set_next_window_pos([vec2] pos)`|设置下一个窗口位置
`void set_window_pos([vec2] pos)`|设置当前窗口位置
`number get_window_pos_x()`|获取当前窗口位置`x`坐标
`number get_window_pos_y()`|获取当前窗口位置`y`坐标
`void set_next_window_size([vec2] size)`|设置下一个窗口大小
`void set_window_size([vec2] size)`|设置当前窗口大小
`void set_next_window_focus()`|设置下一个窗口为焦点
`void set_window_focus()`|设置当前窗口为焦点
`number get_window_width()`|获取当前窗口宽度
`number get_window_height()`|获取当前窗口高度
`void show_demo_window(boolean open)`|打开示例窗口
`void begin_window(string str,boolean open,array flags_arr)`|开始新窗口布局
`void end_window()`|结束窗口布局
`void begin_child(string str)`|开始新子滚动区域
`void end_child()`|结束子滚动区域
### 布局

代码|功能
:---:|:---:
`void begin_group()`|开始新组
`void end_group()`|结束组
`void separator()`|横向分割线
`void same_line()`|设置下一个控件为同一行
`void spacing()`|插入空格
`void indent()`|缩进
`void unindent()`|反缩进
### 标识符
*标识符一般用于右键菜单等，默认情况下标识符就是控件名，但有些控件无 ID 时就要特别标示*  
*一般控件名可使用 `Text##ID` 的形式指定控件的标识符*

代码|功能
:---:|:---:
`void push_id(string id)`|创建新标识符
`void pop_id()`|结束标识符
### 控件
*按钮类控件会在被按下时返回真*  
*输入框需要指定字符缓冲区的大小*

代码|功能
:---:|:---:
`void text(string str)`|文本控件
`void bullet()`|圆圈提示控件，会自动插入`same_line()`
`boolean button(string str)`|按钮
`boolean arrow(string str,[dir] dir)`|箭头按钮
`void image([image] img,[vec2] size)`|图片
`boolean image_button([image] img,[vec2] size)`|图片按钮
`void check_box(string str,boolean val)`|多选框
`void radio_button(string str,number v,number v_button)`|单选框
`void progress_bar(number fraction,string overlay)`|进度条，进度的范围是`0~1`
`void combo_box(string str,number current,array items)`|下拉框
`void slider_float(string str,number n,number min,number max)`|拖动条
`void input_text(string str,string text,number buff_size)`|输入框
`void input_text_multiline(string str,string text,number buff_size)`|多行输入框
`void color_edit3(string str,[vec4] color)`|三色色彩编辑器
`void color_edit4(string str,[vec4] color)`|四色色彩编辑器
`void selectable(string str,boolean selected)`|可选控件
`void list_box(string str,number current,array items)`|列表控件
### 树形结构

代码|功能
:---:|:---:
`boolean tree_node(string label)`|创建新的树节点
`void tree_pop()`|结束树节点
*注意，只有 tree_node()返回真时才需要调用 tree_pop()*
### 菜单

代码|功能
:---:|:---:
`boolean begin_main_menu_bar()`|开始主菜单布局
`void end_main_menu_bar()`|结束主菜单布局
`boolean begin_menu_bar()`|开始窗口菜单布局
`void end_menu_bar()`|结束窗口菜单布局
`boolean begin_menu(string str,boolean enabled)`|开始菜单项
`void end_menu()`|结束菜单项
`boolean menu_item(string str,string shortcut,boolean enabled)`|菜单项目
`boolean begin_popup_item(string id)`|开始控件右键菜单布局
`boolean begin_popup_window()`|开始窗口右键菜单布局
`boolean begin_popup_background()`|开始背景右键菜单布局
`void end_popup()`|结束右键菜单布局
*注意，只有菜单成功打开才需要调用结束函数*
### 焦点

代码|功能
:---:|:---:
`void set_scroll_here()`|将滚动条滚动到当前位置
`void set_keyboard_focus_here()`|设置上一个控件为键盘焦点
### 工具

代码|功能
:---:|:---:
`boolean is_item_hovered()`|返回控件是否被鼠标悬停
`string get_clipboard_text()`|获取剪贴板文字
`void set_clipboard_text(string str)`|设置剪贴板文字
### 输入

代码|功能
:---:|:---:
`number get_key_index([keys] key)`|获取特殊键序号
`boolean is_key_down(number key)`|返回键是否激发
`boolean is_key_pressed(number key)`|返回键是否按下
`boolean is_key_released(number key)`|返回键是否松开
`boolean is_mouse_clicked(number button)`|返回鼠标按键是否单击
`boolean is_mouse_double_clicked(number button)`|返回鼠标按键是否双击
`boolean is_mouse_dragging(number button)`|返回鼠标是否拖动
`number get_mouse_pos_x()`|获取鼠标位置`x`坐标
`number get_mouse_pos_y()`|获取鼠标位置`y`坐标
`number get_mouse_drag_delta_x()`|获取鼠标拖动`x`坐标变化值
`number get_mouse_drag_delta_y()`|获取鼠标拖动`y`坐标变化值
### 画板

代码|功能
:---:|:---:
`void add_line([vec2] a,[vec2] b,[vec4] color,number thickness)`|画线
`void add_rect([vec2] a,[vec2] b,[vec4] color,number rounding,number thickness)`|绘制矩形线框
`void add_rect_filled([vec2] a,[vec2] b,[vec4] color,number rounding)`|填充矩形
`void add_quad([vec2] a,[vec2] b,[vec2] c,[vec2] d,[vec4] color,number thickness)`|绘制四边形线框
`void add_quad_filled([vec2] a,[vec2] b,[vec2] c,[vec2] d,[vec4] color)`|填充四边形
`void add_triangle([vec2] a,[vec2] b,[vec2] c,[vec4] color,number thickness)`|绘制三角形线框
`void add_triangle_filled([vec2] a,[vec2] b,[vec2] c,[vec4] color)`|填充三角形
`void add_circle([vec2] centre,number radius,[vec4] color,number seg,number thickness)`|画圆
`void add_circle_filled([vec2] centre,number radius,[vec4] color,number seg)`|填充圆
`void add_text([vec2] pos,[vec4] color,string text)`|绘制文字
`void add_image([image] image,[vec2] a,[vec2] b)`|绘制图片
## 应用程序名称空间

代码|功能
:---:|:---:
`number get_window_width([application] app)`|获取主窗口宽度
`number get_window_height([application] app)`|获取主窗口高度
`void set_window_size([application] app,number width,number height)`|设置主窗口大小
`void set_window_title([application] app,string str)`|设置主窗口标题
`void set_bg_color([application] app,[vec4] color)`|设置主窗口背景色
`boolean is_closed([application] app)`|判断主窗口是否已经关闭
`void prepare([application] app)`|准备帧
`void render([application] app)`|渲染帧
*一般情况下一个程序只允许有一个应用程序实例，多个实例的行为未定义*  
*ImGui 要求在渲染前必须准备帧，渲染帧将会呈现当前帧到屏幕上*  
*典型的主循环结构如下*
```
while !app.is_closed()
    app.prepare()
    # 循环体
    app.render()
end
```
## 位图名称空间

代码|功能
:---:|:---:
`number get_width([image] image)`|获取图片宽度
`number get_height([image] image)`|获取图片高度
## 方位名称空间

代码|功能
:---:|:---:
`left`|左
`right`|右
`up`|上
`down`|下
## 窗口参数名称空间

代码|功能
:---:|:---:
`no_title_bar`|无标题栏
`no_resize`|不允许调整大小
`no_move`|不允许移动位置
`no_scroll_bar`|无滚动条
`no_collapse`|不允许折叠
`always_auto_resize`|自动调整大小
`no_saved_settings`|不保存设置
`menu_bar`|开启菜单栏
`horizontal_scroll_bar`|开启横向滚动条
## 特殊键名称空间

代码|功能
:---:|:---:
`tab`|制表键
`left`|方向左键
`right`|方向右键
`up`|方向上键
`down`|方向下键
`page_up`|向上翻页键
`page_down`|向下翻页键
`home`|主页键
`end_key`|结束键
`insert`|插入键
`delete`|删除键
`backspace`|退格键
`space`|空格键
`enter`|回车键
`escape`|回退键
`ctrl_a`|Ctrl+A
`ctrl_c`|Ctrl+C
`ctrl_v`|Ctrl+V
`ctrl_x`|Ctrl+X
`ctrl_y`|Ctrl+Y
`ctrl_z`|Ctrl+Z

**注意：**  
+ ImGui 扩展会抛出异常。