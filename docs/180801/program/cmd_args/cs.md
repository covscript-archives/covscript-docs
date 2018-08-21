# 解释器参数
`cs [参数...] <文件> <运行参数...>`  

参数|功能
:---:|:---:
`--compile-only`|仅编译。
`--dump-ast`|导出抽象语法树。  
`--wait-before-exit`|等待进程退出。  
`--log-path PATH`|设置日志和导出AST路径。  
`--import-path PATH`|设置`import`路径。

**注意，若不设置日志和导出AST路径，这两者将直接输出至标准输出流**