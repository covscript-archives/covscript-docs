### 数组类型扩展

代码|功能
:---:|:---:
`iterator`|数组迭代器名称空间
`var at(array,number)`|访问指定的元素,同时进行越界检查
`var front(array)`|访问第一个元素
`var back(array)`|访问最后一个元素
`[iterator] begin(array)`|返回指向容器第一个元素的迭代器
`[iterator] term(array)`|返回指向容器尾端的迭代器
`boolean empty(array)`|检查容器是否为空
`number size(array)`|返回容纳的元素数
`void clear(array)`|删除全部内容
`[iterator] insert(array,[iterator],var)`|插入元素, 插入到迭代器指向的元素之前,返回指向插入的元素的迭代器
`[iterator] erase(array,[iterator])`|删除元素,返回指向要删除的元素的下一个元素的迭代器
`void push_front(array,var)`|在容器的开始处插入新元素
`void pop_front(array)`|删除第一个元素
`void push_back(array,var)`|将元素添加到容器末尾
`void pop_back(array)`|删除最后一个元素
`hash_map to_hash_map(array)`|将数组转换为散列表,要求数组中元素必须都是映射
`list to_list(array)`|将数组转换为链表

#### 数组迭代器名称空间

代码|功能
:---:|:---:
`[iterator] forward([iterator])`|向前移动迭代器
`[iterator] backward([iterator])`|向后移动迭代器
`var data([iterator])`|访问迭代器指向的元素