# URI与URL的区别

URI，是统一资源标识符，用来唯一的表示一个资源。WEB上每种资源如HTML文档、图像、视频片段、程序等都是一个来URI来定位的，

URI一般有三部分组成

1.访问资源的命名机制

2.存放资源的主机名

3.资源自身的名称，有路径表示，着重强调与资源





URL，是统一资源定位器，它是一种具体的URI,即URL可以用来表示一个资源，而且还指名了如何locacate这个资源。

URL是Internet上用来描述信息资源的字符串，主要用在各种WWW客户程序和服务器程序上，特别是著名的Mosaic。采用URL可以用一种统一的格式来描述各种信息资源，包括文件、服务器的地址和目录等。URL一般由三部组成：①协议(或称为服务方式)②存有该资源的主机IP地址(有时也包括端口号)③主机资源的具体地址。如目录和文件名等





**复杂点**

首先，URI，是uniform resource identifier，统一资源标识符，用来唯一的标识一个资源。而URL是uniform resource locator，统一资源定位器， 它是一种具体的URI，即URL可以用来标识一个资源，而且还指明了如何locate这个资源。而URN，uniform resource name，统一资源命名，是通过名字来标识资源， 比如mailto:[java-net@java.sun.com](mailto:java-net@java.sun.com)。也就是说，URI是以一种抽象的，高层次概念定义统一资源标识，而URL和URN则是具体的资源标识的方式。URL和URN都是一种URI。 在Java的URI中，一个URI实例可以代表绝对的，也可以是相对的，只要它符合URI的语法规则。而URL类则不仅符合语义，还包含了定位该资源的信息，因此它不能是相对的，schema必须被指定。