### `regex` 扩展

代码|<p/>
:---:|:---:
`result`|Regex Result 名称空间
`[regex] build(string)`|构建一个正则表达式
`[result] match([regex],string)`|匹配正则表达式到整个字符序列
`[result] search([regex],string)`|匹配正则表达式到字符序列的任何部分
`string replace([regex],string str,string fmt)`|以格式化的替换文本来替换正则表达式匹配的出现位置

#### Regex Result 名称空间

代码|<p/>
:---:|:---:
`boolean ready([result])`|检查结果是否合法
`boolean empty([result])`|检查匹配是否成功
`number size([result])`|返回完全建立的结果状态中的匹配数
`number length([result],number)`|返回特定子匹配的长度
`number position([result],number)`|返回特定子匹配首字符的位置
`string str([result],number)`|返回特定子匹配的字符序列
`string prefix([result])`|返回目标序列起始和完整匹配起始之间的子序列
`string suffix([result])`|返回完整匹配结尾和目标序列结尾之间的子序列

**注意:
Regex 扩展会抛出异常。**