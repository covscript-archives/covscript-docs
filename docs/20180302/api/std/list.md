### 链表类型扩展

代码|<p/>
:---:|:---:
`iterator`|链表迭代器名称空间
`var front(list)`|访问第一个元素
`var back(list)`|访问最后一个元素
`[iterator] begin(list)`|返回指向容器第一个元素的迭代器
`[iterator] term(list)`|返回指向容器尾端的迭代器
`boolean empty(list)`|检查容器是否为空
`number size(list)`|返回容纳的元素数
`void clear(list)`|删除全部内容
`[iterator] insert(list,[iterator],var)`|插入元素, 插入到迭代器指向的元素之前,返回指向插入的元素的迭代器
`[iterator] erase(list,[iterator])`|删除元素,返回指向要删除的元素的下一个元素的迭代器
`void push_front(list,var)`|在容器的开始处插入新元素
`void pop_front(list)`|删除第一个元素
`void push_back(list,var)`|将元素添加到容器末尾
`void pop_back(list)`|删除最后一个元素
`void remove(list,var)`|删除所有与指定变量相等的元素
`void reverse(list)`|将该链表的所有元素的顺序反转
`void unique(list)`|删除连续的重复元素

#### 链表迭代器名称空间

代码|<p/>
:---:|:---:
`[iterator] forward([iterator])`|向前移动迭代器
`[iterator] backward([iterator])`|向后移动迭代器
`var data([iterator])`|访问迭代器指向的元素