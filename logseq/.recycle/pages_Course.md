-
- [[flomo]]
  #+flomo_tag: Course
	- 2022-03-04 14:04:32
	   #Course/web数据管理
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTc1MDIxNTg
	  #+flomo_id: MTc1MDIxNTg
	  #+created: 2022-03-04 14:04:32
	  #+updated: 2022-03-04 14:20:13
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-04/370015/e425517f0837e69be8250813a21f290c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=r8vBM7sO0tz7e1py%2Fx96UPh32ho%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-04/370015/936f8abd8bdb01421546abf1835e1f65.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=wEvIfQhKri9BUHvEQCBr2hFBrTw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-04/370015/0a42c7260a8ca3f22b244c07b0c9072e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=qmNgAEvrxgoF7o09%2BpUSqgYuRaU%3D)
		  #+isImg: true
	-
	- 2022-03-03 15:31:57
	   #Course #Algorithm/KMP 
	  
	  https://pan.baidu.com/play/video#/video?path=%2F07-%E5%B7%A6%E7%A8%8B%E4%BA%91_%E7%AE%97%E6%B3%95%E4%B8%8E%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E8%BF%9B%E9%98%B6%E7%8F%AD%2F04KMP%E7%AE%97%E6%B3%95%E5%8F%8A%E5%85%B6%E6%89%A9%E5%B1%95.mp4&t=-1
	  * JAVA中的indexOf使用的不是KMP算法，是对KMP优化的一种算法，和KMP的算法复杂度一样都是O(N)，只是小常数不一样。
	  
	  * KMP的应用：1）判断一个字符串s1是否是另外一个字符串s2的旋转词
	  *只需将s1 + s1 = s, 即将s1重复两遍，再利用KMP判断s2是否是s的子串即可；*
	  2）判断一棵树中的数字排列是否与另外一棵树的某个子树的排列完全相同，*也就是说一棵树的子树是另外一棵完整的树*
	  *思路：将结点值进行序列化，然后进行两个序列的KMP匹配。*
	  
	  
	  
	  先序遍历整棵树的结点，每个结点的值相当于是原来字符串中的一个字符，先序遍 历是没有歧义的，具有唯一性。代码实现的时候是用了一个string的数组，每个string对应于一个结点的取值。
	  在所有结点值的右边添加下划线然后连接所有结点的做法会存在bug，不匹配的两棵子树在这种方法下有可能匹配；在结点值的两边添加下划线然后连接所有结点，这样不会存在bug，但是会很麻烦。
	  
	  *二叉树序列化为什么要补空：空就是在结构上占据一个位置，保证后续没有了；如果不补空，可能会出现两个不同的二叉树具有相同序列这样的现象。补充后这个序列就代表唯一的二叉树结构。*
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTc0MTY0NTg
	  #+flomo_id: MTc0MTY0NTg
	  #+created: 2022-03-03 15:31:57
	  #+updated: 2022-03-11 09:09:09
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/0d88e567e793a72f98810b917d180a6c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=jT%2FWJl0QA6Lw6HS6iL5bMA0y5iE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/0b90121acb5dda0bc90c3b18a99441cc.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=XgYkZ0FnVtwtJEVAaQQFcm01r7E%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/69a60566002aceb3ec1ad3e12c20a988.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=Ci9eZKkKonyJ1xsHfxhVidhw15o%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/784c30e134832659de6f49c84028b045.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=qPv8UKTNn2WPfegMo2JHiioTEhw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/f4abf8a59026f0fa4be14f5dfd556831.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=Oq%2BNh2EjdcFMr5yzAO67GnDtP5M%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/0b7aafb4643561cd0bf22d62fbaf8f6c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=1h8myzJZi3Pu8eDdTM%2F%2FDL0GYew%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/ef588a673a116f774fff46e350c1b2dc.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=e0qo8bSxvPR9Xd7im8x%2FhveAs5k%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/9bfd5c6365c5b47c3570b9efa8023a17.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=FSP64QcS6AZY5mF7LUGRzvhASbQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/fce6e28039b427cb12eb45ea81c03fb9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=v9uXMyAEW44EOi4%2B0UGwjYPVQOk%3D)
		  #+isImg: true
	-
	- 2022-03-03 11:08:08
	   #English #Course
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTczOTQzODE
	  #+flomo_id: MTczOTQzODE
	  #+created: 2022-03-03 11:08:08
	  #+updated: 2022-03-03 11:08:08
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-03/370015/1646276878522FDAB55BD251F9B49.jpg?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137944&Signature=c%2BIkfjF34vZ8YxHvVToPjy9thJA%3D)
		  #+isImg: true
	-
	- 2022-03-02 19:39:14
	   #Course/云计算
	  虚拟化的资源利用率不到95%，结点之间的通信效率比较低，且存在安全问题，不适用并行计算场景
	  
	  弹性、聚合
	  
	  软件虚拟化针对操作系统
	  内存虚拟化
	  硬件虚拟化
	  
	  全虚拟化代价大，需要把代码转化成另外一种模式执行
	  半虚拟化告诉虚拟机是一个虚拟机，调用敏感指令，开销比较小；需要改写虚拟机的操作系统
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTczNDI1MjI
	  #+flomo_id: MTczNDI1MjI
	  #+created: 2022-03-02 19:39:14
	  #+updated: 2022-03-02 19:43:54
	-