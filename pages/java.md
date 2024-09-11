public:: true

	- webserver
	  collapsed:: true
		- ![image.png](../assets/image_1666083597640_0.png)
		- 静态服务器一般是缓存资源用的，动态服务器是动态来产生内容的。Http是应用层的协议，而UDP和TCP都是TCP层的。
		- 缓存服务器是用来提高性能的，而数据服务器是用来存储数据的。
		- ![image.png](../assets/image_1666083884101_0.png)
	- 反射
	  collapsed:: true
		- ![image.png](../assets/image_1666091859500_0.png)
			- **理解方式1**：当我们使用new SomeClass创建一个类的对象时，实际上JVM会在字节码存储区域或者类加载器中丢一个类的模子，或者说丢一个类的信息，然后有了这个模子才能创建我们的对象。反射机制的作用就是，让模子的准备者 从  JVM这个虚拟机 转变为 程序运行期时的使用者。因为，反射机制 对 使用者的角色进行了反转，使得  其从单纯的使用者身份  变成了 类信息的提供方。
			- **理解方式2：** 通过镜子我们才能看请 自身的样貌和体型， 通过反射我们才能够看到类名、类的属性、类的构造器和类的方法，换句话说 单纯有JVM创建类的模子的过程对我们使用者来说是隐藏不可见的。
			- **反射的意义：因为框架是需要变动的，利用反射能够实现这种变动**
			- **反射获取的三种方式：**
			  collapsed:: true
				- 通过类的对象来获取class对象：类比于拿到iphone手机来推测出其设计图纸
				- 直接通过类本身的class属性来获取：相当于是联系到了iphone的设计师，直接从设计师拿来拿来了设计图纸
				- 通过类的完全路径来获得：相当于知道了设计图的藏匿地址，通过寻宝或者说东洋大盗方式直接盗取
					- 这种方式的好处是能降低程序的耦合度，因为前两种方式都要求类必须已经实现存在，不然会报错，而这种方式中的字符串地址可以后期再补加类
			-
	- XML解析
		- 流程
		  collapsed:: true
			- ![image.png](../assets/image_1666094153159_0.png)
			- ![image.png](../assets/image_1666094251996_0.png)
				- 树形结构或者文档树
			- XML在JAVA中有四种解析方式，这里推荐其中的SAX方式，是一种流模式。还有DOM解析方式，就是将整个文档树都加载到内存中去。
		- 数据处理
- [[maven]]
- [[spring]]
- [[springboot]]
- [[DataStructure]]
- [[JavaScatteredKnowledge]]
  collapsed:: true
	- python中的模块是一个.py文件，而Java中的模块应该是一个包；python中一个模块子功能的实现是通过函数，而 java中的子功能是通过一个类。这样看上去python模块的大小要比java小，但是因为python的代码量低，所以不一定。
- [[DesignPattern(设计模式)]]
- [[抽奖系统]]
- [[八股文]]
- [[Kafka]]
  collapsed:: true
	- kafka2.8.0以前必须要安装对应的zookeeper才能使用，2.8.0版本以后（包括3.0.0）可以不安装zookeeper就能独立地进行使用
	- kafka的定义：
	  collapsed:: true
		- ![image.png](../assets/image_1723338392082_0.png)
		  collapsed:: true
			- 前端埋点通过接口将数据发送到日记服务器，日志服务器上使用文件存储来保存数据，Flume用于监测日志文件的数据变化（每增加一条日志文件都会被记录下来），Hadoop是用来进行大数据分析的。在日常情况下，日志服务器Flume的采集速度< Hadoop的上传速度, 所以Hadoop能够应付得过来；但是在双11期间，Flume的采集速度会大于200MB/s，这时只能使用Kafka集群来进行流量缓冲，Hadoop仍然保持自己的处理速度不变。Kafka集群里“浏览”、“点赞”、“收藏”的数据量本身不一样，因而发送给Hadoop的速度也会有差异，这样Hadoop端就不好调控自身的速度，故这里采用“订阅”模式
			-
			-
	- kafka的功能：
	  collapsed:: true
		- 缓存/消峰
		  collapsed:: true
			- ![image.png](../assets/image_1723340472225_0.png)
		- 解耦
		  collapsed:: true
			- ![image.png](../assets/image_1723340654593_0.png)
			-
		- 异步通信
		  collapsed:: true
			- ![image.png](../assets/image_1723340974655_0.png)
	- 消息队列的两种工作模式：
	  collapsed:: true
		- ![image.png](../assets/image_1723341447890_0.png)
		- 为什么一般来说生产者只有一个，而消费者会有多个呢？这个和制造业的情况很相似吧，比亚迪电动车生产者只有一个，但是消费比亚迪的顾客却很多，本质就是生产难度 > 消费难度
		- 为什么发布/订阅模式里的消息从来都不删除呢？如果队列满了，也还是不删除吗？不同主题对应的消息量应该是不同的，比如一般浏览数据量 > 点赞数据量 > 评论数据量，那么为了保证消息队列的可用性，队列的长度岂不是要满足“最长木板原理”？如果是这样，那必然占用空间比点对点模式大得多？
		-
	-
- [[Dubbo]]
	- dubbo是面向接口代理的、高性能的RPC调用框架，它最重要的功能就是服务的自动注册和发现：能够支持多种注册中心服务，服务实例在注册中心上的上线和下线能实时感知
	- dubbo架构图：
		- provider建立在container启动的基础上，然后向registry进行register动作；同时，consumer从registry上进行subscribe，当registry上已经有相应的provider后就会notify给这个consumer；consumer调用provider；在整个过程中，会有monitor对consumer和provider的行为进行监控
	- dubbo支持的注册中心：
		- multicast注册中心
		- zookeeper注册中心
		- redis注册中心
		- Simple注册中心
		-