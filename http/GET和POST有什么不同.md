# GET和POST有什么不同

- GET参数通过url传递，POST放在body中（http协议规定，url在请求头中，所以大小限制很小）
- GET请求在URL中传递的参数是由长度限制的，而POST没有
- GET在浏览器回退时无害的，而POST会再次提交请求
- GET会被浏览器主动的cache,而POST不会，除非手动设置
- GET比POST更不安全，因为参数直接暴露在URL中，所以不能用来传递敏感信息
- 对于参数的数据类型，GET只能接受ASCII字符，而POST没有限制
- GET产生一个TCP数据包，POST产生两个TCP数据包。
- 对于GET方式的请求，浏览器会把http的header和data一并发送出去，服务器响应200（返回数据），而POST浏览器先发送header,服务器响应100继续，浏览器再发送data,服务器响应200（但会数据）