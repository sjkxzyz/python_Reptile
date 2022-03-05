# python_Reptile
记录一下学习爬虫的过程，欢迎大佬指正！
# 爬虫基础_HTTP基本原理
## URL
URI:统一资源标志符
URL:统一资源定位符
URL是URI的子集
除了URL，URI还有一个子集，叫作URN,即统一资源名称。URN只为资源命名而不指定如何定位资源。URN使用非常少。
URL基本组成格式：
    scheme://[username:password@]hostname[:port][/path][;parameters][?query][#fragment]
    其中 []中的内容代表非必要部分。
各部分含义：
    scheme:协议。常用的协议有http，https，ftp等，另外scheme也被常称作protocol,两者都代表协议的意思。
    username,password:用户名，密码。在某些情况下URL需要用户提供用户名和密码才能访问。
    hostname：主机地址。可以为域名或ip地址。
    port：端口。这是服务器设定的服务端口。但是有些URL没有端口信息，这是使用了默认的端口。http协议默认端口为80，https默认端口为443.
    为什么设置端口?
    
    path:路径。指的是网络资源在服务器中的指定地址，比如http://github.com/favicon.ico中的path就是favicon.ico，指的是访问Github根目录下的favicon.ico
    parameters:参数。用来指定访问某个资源时的附加信息，比如http://8.8.8.8:12345/hello;user中user就是parameters。但是现状parameters用的比较少，所以目前很多人会把query部分称作参数，甚至把parameters和query混用。严格意义说，parameters是分号（;）后面的内容。
    
    query：查询。用来查询某类资源。如果有多个查询，则用&隔开。比如http://www.baidu.com/s?wd=nba&ie=utf-8,其中query部分就是                 wd=nba&ie=utf-8。由于query比parameters用的多，所以平常我们见到的参数，GET请求参数，parameters，params等称多数指的也是query。         严格意义来说，应该用query来表示。
    
    fragment:片段。它是对资源描述的部分补充，可以理解为资源内部标签。目前它有两个主要的应用：
        1.用作单页面路由，比如现代前端框架Vue，React都可以借助它来做路由管理；
        2.用作HTML锚点，用它可以控制一个页面打开时自动下滑滚动到某个特定的位置。 
        
## HTTP
