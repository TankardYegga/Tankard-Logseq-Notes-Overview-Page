public:: true

- CAP:
  collapsed:: true
	- 学习链接：
		- https://javaguide.cn/distributed-system/protocol/cap-and-base-theorem.html#base-%E7%90%86%E8%AE%BA%E7%9A%84%E6%A0%B8%E5%BF%83%E6%80%9D%E6%83%B3
		- https://ravindraelicherla.medium.com/cap-theorem-simplified-28499a67eab4
	- 问题：
		- CP中的一致性到底是每个分区各自保证分区内的一致性，还是说只有一个分区提供服务，其他分区的读写操作全部停止？
			- 答案是后者，在没有分区故障时，每个分区能够保证自己的一致性，但是发生故障后，只有包含主节点的分区能够继续提供服务，而其他分区的服务需要等待网络故障解决后才能恢复
			-
	-
- [[Dubbo]]
- [[mit/6.824]]
- [[深入理解分布式共识算法]]
- [[InterestedMentors]]
-
-