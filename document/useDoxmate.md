在windows下面使用doxmate

1. 下载node.js（msi）并安装 http://www.nodejs.org/download/

2. 添加环境变量 (看你具体安装路径);C:\Users\Administrator\AppData\Roaming\npm

3. 安装doxmate : 打开cmd 运行 npm install doxmate -g 

到此已安装完成；


在包含package.json 、readme.md的目录下运行doxmate build

或者:doxmate build -o output -s wordpress 


修改doxmate 生成文档样式

C:\Users\Administrator\AppData\Roaming\npm\node_modules\doxmate\templates\default

此目录下：

api.html ： 扫描lib下面的js生成的文档
doc.html : 扫描doc目录下面的md文件，生成的文档
index.ejs : 生成doc目录下面的md文件的索引
header.ejs : 页面头部
footer.ejs : 页面尾部
sidebar.ejs : lib下面js生成的文档内容
section.html : lib下面js生成的文档的索引

也可以修改base.css 


doc 目录下md文件排序 : 

文件名前面下划线越多，排名越靠前,在header.ejs 中修改

```
          var keys = Object.keys(docs);
          keys.sort(function (a, b) {
          //按照名称前端的_排序，越多越靠前
          var a_pri = a.lastIndexOf('_');
          var b_pri = b.lastIndexOf('_');
            return a_pri > b_pri ? -1 : 1;
          });
```


http://api.guanyisoft.com/

http://gop.guanyierp.com/

http://oms.guanyisoft.com/

http://wiki.open.qq.com/wiki/website/%E7%BD%91%E7%AB%99%E6%8E%A5%E5%85%A5wiki%E7%B4%A2%E5%BC%95

