### 全局

代码|功能
:---:|:---:
`context`|运行环境
`char`|字符类型
`number`|数值类型
`boolean`|逻辑类型
`pointer`|指针类型
`string`|文字类型
`list`|链表类型
`array`|数组类型
`pair`|映射类型
`hash_map`|哈希表类型
`exception`|异常名称空间
`iostream`|输入输出流名称空间
`system`|系统名称空间
`runtime`|运行时名称空间
`math`|数学名称空间
`[range] range(number stop)`|生成一个步长为1的一个区间[0, stop)
`[range] range(number start, number stop[, number step=1])`|生成一个步长为step(默认为1)的区间[start, stop)
`number to_integer(var)`|将一个变量转换为整数
`string to_string(var)`|将一个变量转换为文字
`string type(var)`|获取一个变量的类型名
`var clone(var)`|复制一个变量并返回
`void swap(var,var)`|交换两个变量的值