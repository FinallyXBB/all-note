# GitBook安装
**安装gitbook简单步骤：**

1.安装Node.js
```
上官网下载node.js并安装
验证：node -v // 查看安装是否成功
```
2.安装gitbook
```
npm install gitbook-cli -g
gitbook -V // 查看版本，时间较长，如果失败请多次尝试
```
3.建立书籍
```
gitbook init // 初始化书籍
生成SUMMARY.md和README.md文件，前者管理书籍目录。
```
4.查看书籍
```
gitbook serve // 生成静态网页，并启动服务器，默认访问端口4000,可在浏览器访问
```
5.编辑书籍
请查阅相关语法简介。

