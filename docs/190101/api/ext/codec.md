# Codec 扩展

代码|功能
:---:|:---:
`base32`|Base32编码译码器名称空间
`base64`|Base64编码译码器名称空间

## Base32编码译码器名称空间

代码|功能
:---:|:---:
`standard`|标准编码译码器(rfc4648)
`rfc4648`|RFC4648编码译码器
`crockford`|Crockford编码译码器
`hex`|二进制编码译码器

## Base64编码译码器名称空间

代码|功能
:---:|:---:
`standard`|标准编码译码器(rfc4648)
`rfc4648`|RFC4648编码译码器
`url`|为链接优化的RFC4648编码译码器
`url_unpadded`|为链接优化的RFC4648编码译码器，无对齐符号`=`

## 译码器函数

代码|功能
:---:|:---:
`string encode([codec], string)`|编码
`string decode([codec], string)`|译码