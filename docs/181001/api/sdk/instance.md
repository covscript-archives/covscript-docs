# Covariant Script SDK文档
## Instance(解释器实例)

Covariant Script 1.3.x将每一个Covariant Script程序包装为独立的运行环境，也就是说无论是实际存在于磁盘中的文件还是REPL环境都是运行在一个Instance中。由此可见Instance在Covariant Script SDK中的地位是十分重要的，所以本文档从Instance开始介绍整个Covariant Script SDK。  
Covariant Script SDK允许任意数量的Instance同时存在，但由于所有的Instance共享一个全局资源空间，所以在任何Instance初始化之前必须首先初始化全局资源。