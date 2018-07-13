# 流式 API 扩展

代码|功能
:---:|:---:
`[streams] of(list)`|从 `list` 构建一个 `stream` 对象
`void for_each([streams],function action)`|对流中每一个元素执行一次 `action`
`[streams] peek([streams],function action)`|与 `for_each` 功能相同,但 `peek` 不会终止流
`number count([streams])`|返回当前流中可操作元素的数目
`[streams] skip([streams],number)`|跳过前 `n` 个元素
`[streams] reverse([streams])`|将流中的元素顺序颠倒
`[streams] filter([streams],function predicate)`|用当前流中的所有符合条件的元素创建一个新流
`[streams] map([streams],function mapper)`|对流中的元素执行 `mapper`,并将结果创建一个新流
`[streams] reduce([streams],identity,function accumulator)`|对流中的元素执行 `accumulator`,并将结果返回
`[streams] limit([streams],number)`|设置流中可操作元素的数目
`boolean any_match([streams],function predicate)`|只要流中有元素符合 `predicate`,就返回 `true`
`boolean all_match([streams],function predicate)`|只有流中所有元素都符合 `predicate`,才返回 `true`
`boolean none_match([streams],function predicate)`|只有流中所有元素都不符合 `predicate`,才返回 `true`
`var find_any([streams])`|从流中任意选取一个元素返回
`var find_first([streams])`|返回流中第一个元素
`list to_list([streams])`|将当前流中可操作元素作为一个 `list` 返回