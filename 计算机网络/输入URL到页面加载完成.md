# 输入URL到页面加载完成过程
> 这个过程是随着知识量的增长而不停扩展的，某些其他文章重点写过的就不详述了。

1. 浏览器开启一个线程来处理这个请求，对URL判断如果是http协议就按照web方式处理；

2. 浏览器查找域名的IP地址。这一步包括 DNS 具体的查找过程，包括：浏览器缓存->系统缓存->……，DNS服务器逐层向上朝赵，最后将查到IP地址返回给浏览器；

3. 浏览器与服务器建立连接：**三次握手**；

4. 进行HTTP协议会话，浏览器发送请求报文);

5. 服务器后端找到相应的请求处理程序；

6. 处理结束后返回响应报文，将数据返回给浏览器；

7. 浏览器下载返回的数据（HTML文档），同时设置缓存；

8. 浏览器对整个 HTML 结构进行解析，形成 DOM 树；与此同时，它还需要对相应的 CSS 文件进行解析，形成 CSS 树（CSSOM）。接下来，需要结合 DOM + CSSOM，进行渲染；

9. 执行 HTML 中代码时，根据需要，浏览器会继续请求图片、CSS、JavsScript等文件，过程同请求 HTML；

10. 断开连接：**四次挥手**。