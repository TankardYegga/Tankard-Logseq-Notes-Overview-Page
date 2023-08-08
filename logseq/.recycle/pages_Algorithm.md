public:: true

	- #Algorithm/Trick
	  
	  当很难想出巧妙的办法来降低时间复杂度时，通常考虑将最底层的操作通过空间换时间的方式来降低(换句话说就是使用预处理的数据结构来存储一些底层操作需要的信息，这些信息能直接对于底层操作通常来说是O(1)的复杂度的）。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MjI2OTEyNTg
	  #+flomo_id: MjI2OTEyNTg
	  #+created: 2022-04-29 13:52:23
	  #+updated: 2022-04-29 13:53:17
	-
	- #Algorithm/Trick
	  
	  当操作量在10^8至10^9区间范围内，对应的c/c++的运行时间一般在1-2s内，而KAVA/Python/ruby则大致在3-4s的范围内。这种方法可以用来评估自己方法的复杂度是否能够满足OA系统的要求，比如如果你的数据量达到了N=10^6的规模，且算法复杂度是O(N2），毫无疑问最后时间必然会超，就得想办法优化自己的算法到O(N)或者O(NlogN）了。
	  
	  如果在给定数据规模下操作量在10^7及其以下，一般说明你的算法已经优化到底了，或者说至少满足题目的要求了。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MjI2OTExMDQ
	  #+flomo_id: MjI2OTExMDQ
	  #+created: 2022-04-29 13:50:11
	  #+updated: 2022-04-29 13:56:19
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-29/370015/ccc592b5f94cd47ce5e0a921f71093ee.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=EY20J3AhvhKC6iiKudsP54LgsRs%3D)
		  #+isImg: true
	-
	- #Algorithm/BM算法 
	  
	  目前主要是有一些点没有完全搞懂：
	  
	  * 这里面后缀函数起到的作用是什么？与KMP中的前缀函数的作用有什么区别？
	  
	  * 利用递归法求解最长对称后缀时的边界情况为什么要那么处理？
	  
	  BXYZTK
	  XYZTKU
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTk5MjQxNjM
	  #+flomo_id: MTk5MjQxNjM
	  #+created: 2022-03-30 10:50:33
	  #+updated: 2022-03-30 10:50:33
	-
	- #Algorithm/刷题
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTk0MTYyNDk
	  #+flomo_id: MTk0MTYyNDk
	  #+created: 2022-03-24 21:20:22
	  #+updated: 2022-03-25 14:00:05
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/98215da5f26a5ca6308e7e20c8e14ea3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=KM6LHY6TVeYvXDqfHJf23yevyVY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/ce1f147817b5f25196dfe92cf36e45f5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=qlKAbIjHKPtvDjy74N878QxsxPI%3D){:height 28, :width 54}
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/427c4306b24565c2f38cfe31a041760e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=TxbeZ5ulbVm7lGXDTvYJ6LRd5xQ%3D)
		  #+isImg: true
	-
	- #Algorithm/刷题 
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTk0MTI0ODg
	  #+flomo_id: MTk0MTI0ODg
	  #+created: 2022-03-24 20:35:58
	  #+updated: 2022-03-24 21:19:41
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/1844f01ed68f88bf77383250933c2589.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=pbzH54bpExwon3toaYzwkpHuHbo%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/031a8e51a34f4bb87d1c1d93642847de.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=po5jAZGM2Rmkj8RXYaRucsgu8KU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/e7a6c3a4375acf04b62b6a9b7202fa67.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=FESTE5W8MT%2FWI%2FbIxsGkHrQJoYY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/f1ccc14d3ea0c41e47702e96e6a747c9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ig5kgsNEA8SNDj5I5%2Fc3qM4EK0U%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/322ed89b97144dca5c0d1af384aca708.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=3AmJz5vrPnbzX%2BsW8N8s2aruOi0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/159e6b9267e0929d2cf6304eceb5a810.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=i5Nu%2BkLlWlNEAeprSRI6WdQN590%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/427fbb1340a6bce9592a698c21a94fd4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=S%2BPje4KiBXCSuEXPtNo1Kx8SdI0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-24/370015/d92d1f86e22483b88454d7296d8939ad.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ilspAZN5fzgrE3uEMBDsf1jh%2FhQ%3D)
		  #+isImg: true
	-
	- #Algorithm/卡特兰数 
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTk0MTI0MjU
	  #+flomo_id: MTk0MTI0MjU
	  #+created: 2022-03-24 20:35:17
	  #+updated: 2022-03-24 20:35:17
	-
	- #Algorithm/AC自动机                                                                                                     
	  
	  * AC自动机不支持动态添加候选字符串，可以改进但是这不是AC自动机原本的设定
	  
	  * AC自动机不支持删掉候选字符串
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyNjk3NzQ
	  #+flomo_id: MTkyNjk3NzQ
	  #+created: 2022-03-23 11:47:28
	  #+updated: 2022-03-23 14:41:01
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/fcaf538dd2c5dcf071d28cc76438a163.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=yjQ2VlRTDAoOgnyr3ti2b4ttwW8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/41b5aa905298f8b3817f61d4ae741ff0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=j71tQbFUd7KmIEaWcl11OzDpX3E%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/081497757fdff4c673458c9a988fc0bc.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=7ZTPtII12hoAIkYY%2FwWCxUimbWI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/b8bbd72d03056da949c568d28be48580.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=9t%2Bi%2Ba%2BzTaBlbZuj5jHWxBeX7uo%3D)
		  #+isImg: true
	-
	- #Algorithm/AC自动机
	  
	  * *利用AC自动机依次否定文字从0、从1等开始匹配的可能性。*
	  
	  
	  * *图2中描黑表示确实是某个字符串的结尾。*
	  
	  
	  * *fail转一圈中没有描黑的结点是不会收集答案的，收集答案是从树的根结点到该描黑结点的子字符串。*
	  
	  
	  * 如果AC自动机的前缀匹配失败，就会依据fail跳到另外一个树的分支上去，而不是硬生生地非要沿着前缀树的第一条分叉的每个结点绕一圈（这是对绕圈过程的错误理解，是文章中的部分和AC自动机的这部分前缀匹配上了才去绕圈）。
	  
	  
	  * 关于图9的说明：“abctf”是待匹配的文章，前缀树中包含三个前缀码"abck", "bck", "st"，很自然“abck”的k会被描黑、“bck”的k也会被描黑，“st”的t将会被描黑。首先“abctf”的a与AC自动机的a进行匹配，从a的fail指针处绕一圈并没有发现被描黑的点，然后重新回到a；继续往下走，“abctf”的ab与AC自动机的ab进行匹配，从b的fail指针处绕一圈并没有发现被描黑的点，然后重新回到b；继续往下走，“abctf”的abc与AC自动机的abc进行匹配，从c的fail指针绕一圈并没有被描黑的点，然后重新回到c；继续往下走，“abctf”的abct与AC自动机的abck无法匹配，从c的fail指针往下走，走到bc的c结点，“abctf”的bct与AC自动机的bck无法匹配，从c的fail指针继续往下走，走到根结点，这说明“abctf”以a位置开头、以b位置开头、以c位置开头都无法在AC自动机中找到匹配项，只能从t位置开始匹配了。
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyNTU2NTc
	  #+flomo_id: MTkyNTU2NTc
	  #+created: 2022-03-23 09:27:52
	  #+updated: 2022-03-23 10:27:33
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/af098d124acb1025893ed8cde98c3b59.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=FZxHVJ9OtkoNOAO4%2B1WqpaWmvgA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/f18c72b4e8fcbabdab47959e347422b5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=xE%2BNRG7nwohaXWN%2BgyOTQ9gbWs0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/167e48d372f5cba75e88aa64d2eec0d7.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=VlU37vK3Qf1YnEULgfGJG6mj9C8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/a3b463af85d0d00db2062ba3febe5bac.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=MC5erslCX%2FCy0uNQTcK%2FpSDehug%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/246443379d9fe66738e98155c80aa80c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ZrT34PCFIiBH2W%2B4%2BtJQFAs%2FZ%2Bc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/a171cecb1882c3410c62de0aac1cc971.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=5OmUGLWxcGIiz7Hr3a8YqOBM9Gg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/034f9e1d5380982cd28e3d2e9a7f1f2b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=pmPbFZu7pXMKCLGE64dpprJnif8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/6fcb47535795d791c0429bef22af5d14.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=FjEVoFjg1So5gpQyVsOP81ydSfw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/cf2d1f5481d966a2291aba4ebd1b6f5d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=6JBdc9Vh6Wjf%2B0%2B7f5XFVHlyJzY%3D)
		  #+isImg: true
	-
	- #Algorithm/AC自动机
	  
	  *fail指针多次跳转的含义：*所有的可能性都没有丢弃，每个前缀字符串的fail都连接的是当前最大可能性，如果当前可能性不行，则选择次可能性
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyMzk3OTU
	  #+flomo_id: MTkyMzk3OTU
	  #+created: 2022-03-23 00:41:11
	  #+updated: 2022-03-23 09:26:23
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/c0c1b8357f54e8e8410fe792bfd85d37.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=0yziY0dYcAwYmYUGDAcNFIKxCj0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/c7f28631f78d63f84c58317c7f614988.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=NveK6xV2%2Fbu5Ue%2BOi6WqlIZja8Y%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/a37d4a1c322b2e2258ec296d235fce03.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=4Lg8dFs3bLxkfTzSdgiTKINDt1w%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/4209071dc709be8f72838d95af081c2f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=FOtaSBnystnag3%2F1CtD%2FBEH1mwY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/c6f3944d0dce390608945271ad5ec087.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Fh06otaQvLhTczJSdTE6eVcAgyc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/1b3e00bb1df9e571e2b267affe5b6385.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=4StUjvlrHyF15VwzG8DibmW%2Ftcc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/bb579daf4e65771cf7d5de95e66c8aec.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ctv5kN7cA8aFLCbBMJSZ1Mozpr8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/1529dba722fdde6fca6ca4c3d33b9232.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=YhXeyp%2FuArjhNn10mNBXq%2BgNmV0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/6efa229d35030a768808027a5e0a6c4c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Aqs8S60yZ5pRZrIKLNo9cVEv9hs%3D)
		  #+isImg: true
	-
	- #Algorithm/AC自动机
	  
	  * AC自动机是一种特殊的前缀树
	  
	  * 头结点的fail指针人为规定指向空，头结点第一级孩子的fail指针人为规定统统指向头结点
	  
	  * *fail机制是在建立好整个前缀树之后，再加上这种fail指针的过程，不是在添加字符串字符的过程中通过宽度优先建立的*
	  
	  * 来到每个结点的父结点处的时候，是为这个父节点的孩子结点设置fail指针。两种建立机制见图3和图4，其中头结点第一级孩子的fail设置方法是符合图4所示的第二种机制的，只不过此时父节点恰好也是头结点了
	  
	  * *fail指针的含义：拿图9中的abcde这个前缀串为例，其e边的最后一个结点的fail的含义是：如果必须要以e结尾，哪一个另外的前缀串和以e结尾的后缀串彻底相等并长度最大，那么fail指针就指到哪去。很明显，这里bcde、cde、de、e都是与以e结尾的后缀串彻底相等的前缀串，但是bcde是最大的，随意fail指向bcde。*
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyMjM3NjY
	  #+flomo_id: MTkyMjM3NjY
	  #+created: 2022-03-22 21:54:48
	  #+updated: 2022-03-23 00:31:41
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/285617f5a08c7ce4766b061ac22805b5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=WyLaEODimuOEm2rEk0BRxRRH6w8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/230ab94cb9fafe5ebefc689436fa22b1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=KOw0eQTm0fznfeFk22eqeQCVrxs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/946b61cf8378bf9664f53d53208de68b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=cLJIptEDuI9TvaDNRsfzZ0nRDEE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/db6680e6a31ddee15df0c000b9b34501.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=eT6KoyPPcdE7WEMoge3%2FWjzGzqA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/379c15cff6bd141c28b60d6d4e81c901.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=iY4K4CY9N8fUuXj48zhwK4XBlKA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/d6b394b5435e4fa9af41dca3ad5a46b6.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=P9nUpN6ElAg2NArkV4lwhbmai0U%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/a4ffbaff4efbf27990e53944a1465218.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=gnRsY8wdI1FusbeFXxw2cgTONOE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/5ada481e9cd50b895b4e4e3c30a65fee.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=2eniJYl8yZfoqL4KoXR4%2B%2Fc1wYs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-23/370015/30f5f97ec2d89efc3922739751a3856a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=yXIvk1b0tjPx7BAVqfI9WuiuAjE%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/有序表题目
	  
	  问题2：
	  
	  *问题分析：*
	  * 允许实现查找第K小的小（这里的中位数是严格的中位数，偶数必须去平均值）
	  
	  * 允许加入重复值（窗口内有重复值）
	  
	  * 允许增加删除数字（窗口右移和左移），删除数字还只能删除重复数字中的一次
	  
	  
	  *问题解法：*
	  * *还是构造一棵带有all信息的搜索二叉树。*先在左子树中找第k个数，看能不能找到，能就递归；不能则判断第k个数是不是在当前结点，是则找到，不是则在右子树中递归查找。
	  
	  * 可以使用跳表结构来实现，只要是有序表都可以给每个结点添加all信息项。一般使用SB树，因为比赛的同学都用它
	  
	  * 这里具体实现时可以不用添加all这个信息项，将处于数组不同下标处的相同元素值视为不同的结点，也就是说排序时不仅考虑值还考虑数组的下标（两个key做主键）。所以此时SB树仍然只用维持size这个平衡因子就行了
	  
	  
	  *思考：*
	  * *all信息和SB树中的size信息有什么区别呢？*
	  看上去含义一样，其实不一样。因为SB树收集的key是不可重复的，SB不会去统计每个key出现的频数，每个结点的key的size只是以其为根的树中key的种类的总数。而all不一样，all对于树的叶子结点来说，就是叶子结点对应的key的重复的数量，all对应非叶子结点来说，就是其和其孩子结点的包括重复的数量之和，其本身对应的key的重复数量可以直接通过 all - 左孩子的all值 - 右孩子的all值 计算出来。
	  而在本问题中相同key但index不同的元素被视为不同结点，所以就不需要这里的all了。
	  
	  * *如果偏要使用这里的all，调节平衡时all值的改法和size的改法有什么区别呢？*
	  
	  
	  补充：
	  * Java中的TreeMap底层就是红黑树实现的
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyMTc5MTA
	  #+flomo_id: MTkyMTc5MTA
	  #+created: 2022-03-22 20:49:58
	  #+updated: 2022-03-22 21:44:11
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/8ffb98e7ef270cb580a2b84e34bdbfe2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=mqFmLEm3l6rFO%2BGqWxwTY93mavg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/d0f009974a128ec6575fe5110659c081.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=W6kBE9XPBF%2BUf8KBXLuB89wDlSg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/27774cd837f520513b70083e66d78196.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=4jeZl76y2PhcKL4aFuS4hmH7xMY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/ee665347645ac528054501e8b23afb02.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=kIcNuqNE%2BasH5im2x1k4NQVIR4Q%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/有序表题目
	  
	  问题1：
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyMTA0NTc
	  #+flomo_id: MTkyMTA0NTc
	  #+created: 2022-03-22 19:16:03
	  #+updated: 2022-03-22 19:33:36
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/df10536ff3d008669b80982a3a7c26d8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=PN6OlsvjYfFVkyBy%2F2lFYDYoYqA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/ee4bd60e5d652a19565ee1dde64b24ae.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=OBn6oWMz3APqB6WOL5sgCm5ooSQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/d6e0205302d4bab6167b0a6fb6a4e7f1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=81RNcXMwojkz136h4Mq8Trl4248%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/04e3894e76f4fed5011c99f1a28cf8e0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=h1cJd1TEai7dBK5GqAQ6v6UjwlY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/f8f7e76ddbaa15c12f99c6ebb9a4fcf8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=OWhiDHu2uuHbsQ8z8KdQMwYmHUs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/e5d8d83eb6220fc61a6e2fdc7fc6d1c3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=p1cw8O%2FroAlosqR4qbRnMRXpvGw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/cd33994f63cd55edbb9d39e95d3f76c8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ARIUF3W9CKY7sL%2FFreYPe5gc%2FAw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/eee86a1e042d86e02e32a035fec3f4e3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Ge5mbqbls6GzGLGKinP1S0yBlno%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/9d1c108a40bc4dfe6ffbcdf9aa3e13d2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=kz%2F8tk8%2BTnh6EXWYK5Z7bdpDYWs%3D)
		  #+isImg: true
		- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/有序表题目
		  
		  问题1https://flomoapp.com/mine/?memo_id=MTkyMTA0NTc后续：
		  
		  无论使用AVL、SB还是红黑树，只需要注意我们这里对每个结点新添加的信息项all也要随着平衡树的调整而进行相关调整，比如说交换两个位置处结点的all信息。
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyMTE4NTQ
		  #+flomo_id: MTkyMTE4NTQ
		  #+created: 2022-03-22 19:35:27
		  #+updated: 2022-03-22 20:22:51
			- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/ae237338a7fc5d35ad35331b39c2dc08.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=EsY%2B6T5A9Z5JUu30BQzkzuRlHCE%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/48c2e4c79f96e8e2c87e70783b8fca96.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=PnH4SCXAM5wjNF6g980k3fbF%2FLQ%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/48b199c064d0106d8ecf238b2bc1d804.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=nCHv4jD13VaHzSTo4lAJIsi7%2Bac%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/03000aefdc8eea5f6220a3c3d0d67305.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=5umio5izQeEHTa81zKpDfmKtfYE%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/26d9838f0ae058af2d1101750d625bc1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=qH%2BpD%2BJRO0q9A7hckou7lT8u23U%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/a9318095679f1a60ae8a89366a5562af.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=3kzx531gNU6i0AGqKtENjAQ0Xoc%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/218284718190b7a44f9fabaa265bf1a8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=3NHo5A2h9BzziDKGFIDEqIDoWHk%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/d3205b6ee7ea454d4b43c2ede8884112.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=e0X5aM3FroK4MekcPrujXlYfNRk%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/d09811e5fb7234d95434b28d1bcf68a0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=yF4OP2h4ovXv7LDtuSfTT02NYuo%3D)
			  #+isImg: true
			- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/有序表题目
			  
			  问题1https://flomoapp.com/mine/?memo_id=MTkyMTE4NTQ后续2：
			  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyMTU3MjQ
			  #+flomo_id: MTkyMTU3MjQ
			  #+created: 2022-03-22 20:25:13
			  #+updated: 2022-03-22 22:25:46
				- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/24b2460a6f2b686e10c4f04bdbe1bc59.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=q2hAPewChHgO0bcXtM1FTs41ab8%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/5f8b8065263ed64b69b1b6af382a9c2a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=x%2BKl%2BK3VNhUeB9dSFSDkV%2FWYupM%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/0ecc6a0ab7bdf16db89a96c9e1bd625e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137930&Signature=rHNVVvnz25beQtxRB%2Fm1gYWRJnw%3D)
				  #+isImg: true
			-
		-
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/有序表题目
	  *问题0： 不需要对有序表进行改写*
	  * 每行对应的有序表取各自的最小值组成一个新的有序表A，取有序表A的最小值min和最大值max，得到一个可行区间【min，max】，然后将min从这个有序表A中弹出，用min所在的数组行中的下一个最小值替代，然后继续找出min和max得到一个新的可行区间，如果新可行区间有更窄的则更新，不更窄包括相等的都不更新。
	  
	  * 该算法用到了贪心算法。
	  
	  * 这个过程完全不需要改写有序表，这个问题只用使用系统的API就可以完成所有问题了。
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyMDgwMTQ
	  #+flomo_id: MTkyMDgwMTQ
	  #+created: 2022-03-22 18:42:10
	  #+updated: 2022-03-23 00:22:01
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/0b55121d8964e952d07bd0a990b06ad4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=%2BgThx%2FOfdgBO7vVDL4zRd%2FXKv4Y%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/5f0d96a841b27abaeca61260d1a3909c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=bNP0bLkSnXOawLr0E5c3bepaUNA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/fe01d3c14da724700c6a8a83208af9fd.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=V8JoMQMHXSGr6UKrNPjbZzuGfFg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/9159fbd278f1553ee5f076e2c667e333.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=5oRrgGP3Ly67wCwza1XwCEkRit8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/7dc86f555cb6fd948f8f48cdde71114b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=uV0r6BDBfg1zR29AARLEkVlBqsk%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/445b3b0781968463354d7e8bd5d644ff.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ktBnj6guXWoEI4RoEYusG8koS6g%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/红黑树
	  
	  * AVL和SB树都是4种情况需要调整。
	  
	  
	  * AVL树增加或删除结点时平衡性破坏一点点就要调整， 特别灵敏。
	  
	  
	  * SB或者红黑树的扰动性更小，平衡性很模糊，如果插入或者删除代价比较繁重的话，会用红黑树。
	  
	  
	  * 如果插入或者删除代价极其繁重的话就会用B树、B+树或者234树，但是查询效率会降低，只是不用频繁地读写硬盘。
	  
	  
	  * *红黑树在AVL和SB树之间达到了一种平衡*，所以才被经常考到。
	  
	  
	  * *Reddis为啥选择跳表，而不是AVL或者SB树 来作为底层的有序表？*因为reddis可能有序列化的要求，而skiplist比较好序列化，而AVL或者SB树是个结构化的东西不方便序列化。序列化要求就说利用一些离线时间把内存中的数据转换成文件， 以便能够在重启时能进行恢复。
	  
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkyMDY5MTY
	  #+flomo_id: MTkyMDY5MTY
	  #+created: 2022-03-22 18:27:57
	  #+updated: 2022-03-22 18:46:35
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/542f1f1e1b3451102c9d650b4e763859.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=PRDh4691TlVqgMsnWBIbsoFQDMw%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/跳表
	  
	  SB树怎么找第500小？通过增加数据项，但是复杂度也是logN。
	  
	  跳表怎么找第500小? 需要自己找。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxOTUwMTg
	  #+flomo_id: MTkxOTUwMTg
	  #+created: 2022-03-22 16:17:23
	  #+updated: 2022-03-22 18:18:07
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/a04913090eac543f32cb923afe7bfa29.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Q45ydkrPR0WHA9Od6APuTo1ZWNE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/154b14fb983d84ac993dfb40ce37bc37.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=wUEbn0OL15oOR8nCziyc1a3l60c%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/46efb26567af466f8ae612ae773ea52a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=II4a2Di2pDKbKwhgk8%2FYoZckpts%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/跳表
	  
	  高层往底层跳的方式的时间复杂度是LogN，而直接从底层则是O(N).
	  
	  底层指的是下面的层，高层是上面的层，高层的链表结点数要少。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxODgxNTg
	  #+flomo_id: MTkxODgxNTg
	  #+created: 2022-03-22 15:10:00
	  #+updated: 2022-03-22 16:16:23
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/bb589339bed9150a8fd09c638fe5f26a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=GT2C1SFzzLJqExVSUZVMS%2BARWU8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/7d0b0219f8007e9a77b69fc9156fda3f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=jL3cnxPAhSfQuP5gE%2FiM3aGJ4mU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/ec7ed24f1983c767e39638ff8ee9fe50.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=vUgPINfmHczREa9PXJ%2BS%2ByPkf5g%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/321fe4ede1cf53e24c24461fe869811e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Gfv8BXZJPVcCxtRpRZ6H2%2F8snTg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/6235e6d131f3ea2f42eda42690415319.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=QWCUnr0rBBNsQhj2PierjUWCEVc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/10b34be835178cff21ff6220d83ed129.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=6fGZf9wOLhFzX%2BJC1wtSuzG2%2BBs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/8698005d7154d8e4a3ef5d1cff5b0a1b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=NPyWtrxfuPNSYEEEa8rz5TLiGrA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/64cafb4d867c1e18c4e46c0933cb4cb2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=z1eQyKPwHO%2FrD9zUFwk26AbAOWc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/16e9e9bd8ac3a32b31aba9cb3a775253.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=t4qeeUZA2JqdYZDPheO5%2FYsTNPU%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/跳表
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxNjk2MjA
	  #+flomo_id: MTkxNjk2MjA
	  #+created: 2022-03-22 11:28:24
	  #+updated: 2022-03-22 15:09:51
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/0d53582e94aa9df59fac0e5648b72294.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=lv7zNKx231KB%2BqnkIl3SWP6KPx0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/3585507ae7c230c45c6e56800de1c186.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=2PQtHF7SokKLgD6QSHz7tt7m4oc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/934c9a67fda8606656e6be73ea95a768.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=P6u76i2VBUCPTvqjAOjy%2BwojeIY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/6f4981dabc437bd7e8262b6c292866d6.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=GS5mF8k7UnqhKsbjmn7MDaHWIuQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/64f00ec3123d0ffa154ae020c0116e52.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=knYohjPXdBBS6a5w5tBqz5SIc3I%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/8362a0e5be447c321b0215bb514f36e0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=9Oue2tbbQ%2BCE0UhdUbJ1Np6kC%2BQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/1b5d28f70f1dde7e5d5dd02a637d37f3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=5sy9Nv2bdG7ecHaUQKcVon%2BgBuc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/da4c55aaf5e84bee078b86cf61ea16ef.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=9%2FHQxfVg9BcfP93bPiZHK38sklA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/3d780a22d9cc4b1f4096ba5745d64d5c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=92aZHBqhSH89NIE%2BupUSCxUXneo%3D)
		  #+isImg: true
		- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/跳表
		  
		  实现方便，方法先进，与二叉搜索树毫无关系。
		  
		  通过arraylist来实现其可以向外扩充链接条数。在生产业务场景中有可能使用固定大小的数组，这是因为它们的业务可能存在数据量的上限值。
		  
		  跳表增加结点：1）*先生成该结点：*每个结点默认都有个null结点作为向外扩充的链条，其余外扩链接结点的产生是通过概率机制实现的，每次产生一个【0，1）的随机数，如果该随机数<=0.5, 则增加一个外链结点，如果该随机数 > 0.5, 则停止增加外链结点。也就说，每个结点的外链结点数完全是随机决定的，外链结点数也被称作该结点的层数或者说高低 2）*更新最初始结点的外链结点数：*如果当前结点的外链结点数或者层数比初始结点多， 最初始结点就要增加外链结点数至与当前结点一样。总之， 初始结点的外链结点数要始终等于所有其他结点中外链结点数的最大值。可以把最初始结点理解成单链表的头结点，其key同样没有意义 3）*根据该结点的key建立该结点与其他结点的链接：从最初始结点的第一个外链结点出发，沿着该外链结点出发一直到小于等于当前key值的最后一个结点（或者说是大于当前key值的最早的一个结点）或者到null，对于前者是将当前结点插在其后，对于后者是将当前结点插在其前；然后从最初始结点的第二个外链结点出发，重复上述过程；一直到最初始结点的最后一个外链结点为止。这里实际只有1个结点，不可能同时插入多个外链方向，所有这里说的每次的插入都是针对这个新结点的相应层来说的。*
		  整个过程见https://flomoapp.com/mine/?memo_id=MTkxNjk2MjA中的图2。
		  
		  跳表删除结点：
		  
		  查找结点：永远从最高处开始找
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxNDAxODI
		  #+flomo_id: MTkxNDAxODI
		  #+created: 2022-03-22 00:27:38
		  #+updated: 2022-03-22 14:53:08
			- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/b37ef7e125cd4a1ab9ec947f440c3c13.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=%2F46BR7XKoDSEcn7qTLbUaz7MMcE%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/f67ec61e806aca994b02c33cd04d7640.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=9Wgnuj42a95tZqMsHhI6lu8FC%2Fs%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/d94fba9b111ae00a2b8b02184a81eac5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=JXdO3wYVr%2FtSBa0fAPmQzEolJ6M%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/4e7224e11651fe3966a95817a09ce6c9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=0lZBxUS63r2tlhZUerAIHnW%2B%2B%2Fg%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/6b04304d29d417477d74c7706fca6a2b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=v3aEnD0tgLyi%2FaTvetaAg5rNtOE%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/99ffdc20b331de94f58cfb38754c844d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=YyfYJlbbCvRQlwHtsl3Z3IOlI1M%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/4203dd64c62dde1e0f80880349e117d3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=y0OcE7BMBcZpZHIi0kad37aWI2U%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/530bb280080f8427b4d4a015be93e532.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=KOh1UsitULnYgc4VX4HFIelr3ZU%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/328001c24eb36c4aa945c45629cfbe92.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137931&Signature=4PtbB9mQ7%2B%2BM4x9lozFkShgPdXI%3D)
			  #+isImg: true
		-
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/SB树的代码
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxMzg0MDg
	  #+flomo_id: MTkxMzg0MDg
	  #+created: 2022-03-22 00:02:49
	  #+updated: 2022-03-22 16:33:40
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/61cd3c4b27ed463d49041e547865aabc.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=OnKjwTsi9MUorsNx%2FETtR6LTLsE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-22/370015/f3c2b06cbb87826cf514c6439843a5de.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=IydNGXl7aokPGyvPMejGk0VryVU%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/SB树的代码
	  
	  特别注意即便我们能找到离key最近的上一个结点node，我们也不能把这个新的key值加到这棵树中，这是因为在平衡树中加入一个结点后必须要对从这个结点一直到根结点的路径上的所有结点进行平衡性检查，所以在找到的node的左孩子或者右孩子处随便插入该新的key值是不行的，因为这里没有设置parent指针，从而没有办法往上走。但是如果直接从根结点往下查找插入的话，可以利用递归机制逐层向上返回结点，也就实现了向上走的目的。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxMjYwNDk
	  #+flomo_id: MTkxMjYwNDk
	  #+created: 2022-03-21 22:09:40
	  #+updated: 2022-03-22 00:02:42
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/206a5905ef85d0085cea78e042b0d75f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=eCupNe%2F5Dq6MPq8Xxk9xY5Y92bw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/32bc1de8100eb4e620d20df8eb3ff21a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=9FyxI0t6Kk9aYGhZAef4Kdk9b9M%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/5ddbdfeed3e1abba6a24812a4914a431.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=6xscWrOyGkI6wEi8aLGJfiaBOvE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/db492e2da22888df30e360670121d894.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=QaNje1rdPEkeZFthaDGoRgzTXeU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/931fa96f4165daea06b5a22f0d450e45.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=z%2BBD4V3Tgq4aBGCQkBeyOwv3BGs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/5d716a6599cfca0542659e14c61b355a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=DfPBmDT5K9MmxiNPoqWEpwVuCMc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/fbcfe455f91bbdcc1385c1a248a43957.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=WNBNfjxQwtwq8DwAjbP4K0LVh5Q%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/bbe39b727182e515561f8011bfc184b4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=1QJs2jWraoe%2BnvwS1Aw971eI9SE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/395ce53992032b4bebd663d5db015461.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=RFEqqXhcR5TMz6no29fa2xa9kFw%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/AVL树
	  
	  LL只需要做一次旋转；
	  LR情况中需要把LR对应的那个结点一直旋转到树的根结点的位置，也就是说要不断升高其位置。
	  
	  更正一点：*如果LL和LR都违规，且长度一样，必须只能做LL的调整，可以看图5的反例。为此当前结点cur的右孩子比左孩子高度高2时，先去判断cur的右孩子的右孩子的高度是否比cur的左孩子高度刚好多1，如果是则是RR情况，无需再判断RL了，如果不是才需要判断RL；同理当当前结点cur的左孩子比右孩子高度高2时，先去判断cur的左孩子的左孩子的高度是否比cur的右孩子高度刚好多1，如果是则是LL情况，无需再判断LL了。*
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxMTE4MTc
	  #+flomo_id: MTkxMTE4MTc
	  #+created: 2022-03-21 19:28:36
	  #+updated: 2022-03-21 23:31:30
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/1084e9a8bfa48cf9d682851d5eae7ebf.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Kl2s68eZmPoWGbnhA%2BDZxOROMgI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/5f8281e840c701e941dd049fde60971d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=6Q7hUr8pn5GdBGK7cP%2Btmpe1Y8c%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/b63161da2f4e73f987fca0652e41238c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=GwEKMaIlfo7nkAW%2FXnWAhZCP6zQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/65fab4770955a04f2ec863ec656d521c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=2LgUW7x7JF9FhkxinZfbOT5HjMA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/087761b121e36c8361fc92ee3180ac16.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=kSJCDQNjeRyhSs0DLRuve6Njxf4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/aaf27ad62c802d6aed45daf7f0d7a9ae.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=isQCIvSuIAggkDUjImk9QRQvK4M%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/7dfb39ea5bd8d958ce613f81c17cb401.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=zzvc2hO8%2Blo2ked%2FChAPCzbqgf8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/29e6cdc2a268871097a52daeae9b35f5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=qZ0CrWnvLye2T3KgZhTBnB2DQeQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/2afe9a3216cab5b3d71e063537d977e4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=41fpdHuDkL6bKyjbFeWcdqxN6og%3D)
		  #+isImg: true
		- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/AVL
		  四种类型是否一定只会出现一次？可能都中，严格采取对应的调整措施都行。add操作时不可能同时出现LL和LR，但是删除时有可能。
		  
		  *图9说明：如果能够精确区分出LL和LR，不管采用哪种对应的平衡调整方法，都能够使得树平衡。这种说法是错误的！见https://flomoapp.com/mine/?memo_id=MTkxMTE4MTc*
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkwODgyODA
		  #+flomo_id: MTkwODgyODA
		  #+created: 2022-03-21 14:52:23
		  #+updated: 2022-03-21 23:40:14
			- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/12b36333c734231bcf6caa5248e8257b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=F3EqYxCUDb818ag%2BK63DG36rLk8%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/f66bb7a35073af478d053db00dc7ab6b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=BjXpa9zP13EEwRJSYPv2YNiGvTs%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/572a0580da724a4b2eab53fd2933616a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=uIbq4M8cgx%2F5pQqVQW46EoizFVk%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/f059786a184e9eef35c6491d48cb68a3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=jde%2FR26TN5fLVqgWrrP96e77mpk%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/31068905c45f0585f57dafb741c11b0c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=jJSzYmRUmw3J0x7Fwcuj6BZ7ts4%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/d0868a9828cf15dc83fdeb7114cc84fa.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=MgUnLV1ULv4Y2BmuefGuD0yIJBA%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/dcec6b35d515a0c0da05b0dda81632a5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=s%2F896zjmyKnbxyI2aKj3JXOW%2BXY%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/eda76fb837e23e629abc15213fb6c0a2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=KHTLtXwvI4ib6KLWGkAjPRO7gu0%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/b30949307734f8937b1d778c6046dfea.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137932&Signature=rj7bNNUjJKP%2BKarJG1LQGxHn6A8%3D)
			  #+isImg: true
		-
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/SB树
	  
	  SB数被更多的用来作为有序表改写使用，因为其比AVL要快，平衡性比AVL模糊，扰动比AVL小。
	  
	  
	  *高手的代码中add的时候进行平衡性调整，但是删除时不进行调整，这是由递归来实现的，有时候可能会出现峰值使得复杂度不是logN，但是均摊下来还是LogN。*
	  
	  任何递归行为都可以改成迭代行为，迭代行为更有，因为递归行为有更多的系统准备工作。
	  
	  *图4中m(a)和m(x)的调整顺序无所谓，但是m(d)一定是最后一个。*
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxMDU3MjE
	  #+flomo_id: MTkxMDU3MjE
	  #+created: 2022-03-21 18:01:30
	  #+updated: 2022-03-21 23:41:23
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/11e52fe89dab1c6fa9887daf922e88cf.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ihn4ZKhgQDe%2BRP3mFHN60Ptx0YA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/e1cbcd584a85073703fef4b7ae169d24.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=0oAch6mDa7sqpYJWVEJduF6Gi7E%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/41466cd8d6b0320710698d4d16bd431d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=9yVrQcNcvXkOwNRLJQ1ZhjWLzlQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/a8aa1cb92aaaf93c4f644d51f215fecc.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=g0pb1Mj46DUksVANlSL%2FYWuXyGk%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树/SB树                                                   
	  
	   SB维护树上的结点数，且其收集的key是不可以重复的
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkxMDE5ODA
	  #+flomo_id: MTkxMDE5ODA
	  #+created: 2022-03-21 17:14:11
	  #+updated: 2022-03-21 18:01:56
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/83188fca7867f1771dfebe10d574a7f6.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=J1OxDqk2erAMGTGPtopfBKvbn%2Fg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/a745f74707de5250905222e692e281d4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=stukhxsea6F5mfKGvaiZV%2FIy2ag%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/ed34a5180ebe8f44a350ae579d107f08.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=a02JrSElanqmw9pDQONg8qvcxzM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/46d40b7da8f8b6e2d9eadb0d300f9257.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Zkb3i6CP5j%2BwgQmw1m1ty%2Be%2Bbl0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/ff54b0fbd02e503c22b1c2301b3355b9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=gXJLYQUlsYg%2F%2Bi6mG3jhrFJxr08%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/7d58a2ed66d66225ce69dfb714b8d4a8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=V5WNHbIV9ZftNDeV2A6uzRhDOF0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/5204414d7119fb0f67bd40b2aa92d0db.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=jPNU29vA4JiGq7WtzNd24arU8jo%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/f0fd12031bb78c9d0ad8c1cae1662911.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=cTmXq5p0ubu0YC4Z13PrT9RgW0E%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/5bc823429bf5b170a6aca8e5077a11e3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=A0lCfff67pV%2FzBwCDm4mq7G4npI%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树 TreeMap的底层是平衡二叉搜索树。哈希表的所有操作都是O(1)，而TreeMap的所有操作都是O(logn)复杂度。使用TreeMap必须保证key是可以排序的。
	  
	  *有序表是一种规范，是接口名，必须要求1）key是可以排序的 2）所有操作都是O(logn)复杂度。*AVL、红黑树、SB树都可以完成其规范好的功能，都可以称作有序表，用三者来实现性能指标完全一样，有差别的只是常数时间，细节上有区别。
	  
	  三者的平衡性有区别，AVL中任何一个结点的左右子树高度差的绝对值小于2，有最严格的平衡性；SB（size-balanced）树要求任何一个叔结点所拥有的结点数不少于它的任何一个侄子结点，约束的是结点X即便左子树和右子树的结点数有差异但也不会过于悬殊，从而保证树的高度，进而保证复杂度不超过0（logN）；*红黑树中第四点要求从某个结点到所有叶子结点的路径中最长的路径必然为黑红-黑红-黑红这种交错方式，最短的路径长度必然为全黑，很明显最长路径不会比最短路径长2倍以上，这就保证了平衡性*。
	  
	  三种树三种平衡性的实现都是由基本的左旋和右旋的组合来完成的，三种树对应不同的组合方式和组合细节。可以把它们看做是自我实现的搜索二叉树，它们的增删与普通的搜索二叉树是完全一样的，只是在删除完、增加完之后的重新恢复平衡的方式是不一样的。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkwMzcwMjI
	  #+flomo_id: MTkwMzcwMjI
	  #+created: 2022-03-20 23:52:15
	  #+updated: 2022-03-21 18:02:27
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-20/370015/121d0ce3619b02f2ceac3162e3274d4a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=XPFwXYBnoSaYzpJSoZRKXmphXzc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-20/370015/06a0df0141e64eca324509e9da3891d3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Fx%2FTpkXi8qHzXr1BtPp4MZrqpmQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-20/370015/25636ebbc99dc5cc7f74b7b977630ffa.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=lS%2FgwzmJ7Fn31r273eCNdlxwL%2FY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/453a9c6157afc987a1206d820cd61a37.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=X1WwouUzVEhouB9ZcSN5yIqxJdI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/b6e2f904ca8fd785ec4d492c45fe14aa.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=n5zDeHICxfPPIL5dFWJmWi3ir%2B4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/32abd697dd3381ef941895d5b58a47b2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=qaWNzwByG40PPOvuQSpdmS625Xs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/ad8b0afbdddeb12f578ea941ff34373c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=QNZZpvLHm2brzSxMfTWC3MK9aWo%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/57c65af08331be52a1ca4ff257de2d59.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=P3MB6xF2L3p96BBDUymdIPdzfVU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-21/370015/6d92f0fb2cdf9f2a5de36ebbacf9953d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=NTHJExwkfnVpt0luUnRANEvLGrY%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树
	  
	  不管是什么情况的输入，自平衡机制都能够保证树的复杂度不超过O(logN), 且在每次树进行更新后插入删除查找等操作都能够保持O（logN）。
	  
	  左旋和右旋是两个基本操作，其是关于某个头结点进行的。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTkwMTgxOTg
	  #+flomo_id: MTkwMTgxOTg
	  #+created: 2022-03-20 20:59:43
	  #+updated: 2022-03-20 21:46:02
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-20/370015/3ad4b98c5801c8c1372565598390e28b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=NN7Zr5DJA1UO77dN46Q%2FMLJkPYg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-20/370015/48f1975c662133aa1920227d878133bc.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=u65TA%2FQJKBobCsAT6t2gnM60Reg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-20/370015/295c6266963bb4bca7a75774de23950b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=YecKBcwqIbdN9k4%2BsBNTR9L7tvY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-20/370015/c7fcc94fc65f155d1480f2683b5d94c9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Ho1Jj%2FoI4J%2BCSrW%2FDSstV9zKe%2B4%3D)
		  #+isImg: true
	-
	- #Algorithm/有序表的原理、应用和拓展/搜索二叉树
	  注意删除既有左子树又有右子树结点时，是将右子树的最左结点A替代被删除结点B，与此同时将A的右孩子结点来替代A本身，边界情况是A结点的父亲就是B。
	  
	  其实个人觉得也可以将左子树的最右结点C来替代被删除结点D，与此同时将C的左孩子结点来替代C本身，边界情况是C结点的父亲就是D。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2NzMzNDc
	  #+flomo_id: MTg2NzMzNDc
	  #+created: 2022-03-17 00:36:23
	  #+updated: 2022-03-20 21:18:35
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/75009144751622d3687fed0999720148.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=qUd%2Bp7Tp%2FLIegxR5r738EwEsunY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/486e0cd2d7310d60e28c35777eb06e38.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=A5tKr1Jig%2B1Pku1dGO2irnIxbDA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/2be796476d3a2d8f80072d8bf3e2d07d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=gMJ64OuhRN3x2ysjSk9uQV0nWNY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/76d01fa2a7fedf2f11637561a97f4e5e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=XYWZtPRW4BNPI08e3hsnCDCSCbc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/5a0a88ad0c40df3b9afbe42083f09ebf.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=2TaGfqIaE4NOdH2eMZc8gpqjUv0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/a63fa97ee90f1dd123054ce4d42cb061.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=5hzSC7kP%2FzmhIh%2B9ytn5FA5RG%2F8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/5711bca342ffb00f95fddc8e91cdb76a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ZUYSOVn5%2FH1rIPRUmne7sT4bgEM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/88e40c73c377645d6154eb363c39a474.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=aOddXHKIijtFzMYQMXREMJue0xQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/dbb70a31c3380c211efc6dd4d9f1985e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=OHhJPT6EPzvMg%2FTto%2Bx9BWfJum4%3D)
		  #+isImg: true
	-
	- #Algorithm/资源限制类题目
	  https://blog.51cto.com/u_15054047/4156740 有详细总结.
	  
	  *问题1解答:*
	  通过建立多个子文件来解决. 假设需要建立m个空的子文件, 题目中是32位的无符号整数,但是JAVA中只有有符号整数类, Interger.MAX_VALUE为(2^31 - 1)B/ 10^8 = 21.47亿, 很明显其存储不了32位无符号整数的最大值, 所以子文件中的一条记录( 整数值 - 频数) 需要 8 * 2 = 16 Bytes. 40亿个整数首先通过哈希函数f映射到某个哈希编码code, 然后code % m 决定该数据放在哪一个子文件里, 因为这40亿个整数最坏情况下完全不同, 也就是对应有40亿个种类, 平均放在每个子文件里的种类数就是 40亿/m, 平均存放在每个子文件里的内存大小为 40亿/m * 8B = 320亿/m B, 而1GB约等于10.73 亿 B, 所以要求 320亿/m <= 10.73亿 B, 也就是要求 m >= 320/10.73 = 29.8 = 30, 我们可以之间将m设置为400极大降低内存占用率, 因为电脑中其他程序占用内存的比例也是相当大.
	  
	  整个过程个人理解是: 每次从40亿的文件一次性读取一个无符号整数, 然后哈希、对m取模，将其存放在指定的子文件中，直到文件内容全部读取完毕，同时m个子文件全部生成完毕。将0号子文件加载到内存当中，通过比较找到该子文件中出现次数最多的整数值num0和出现频率freq0，然后再将1号子文件加载到内存当中去，同样计算出子文件中出现次数最多的整数num1和freq1，... 整个过程中可以使用全局变量动态找到最大值。
	  
	  *问题2题意分析：*32位无符号整数的最大值约为42.95亿，文件中含有40亿个无符号整数，就算该文件中这40亿个数都不重复，也有2.95亿个数是没有出现的, 也就说至少是2.95亿个数没有出现. 最暴力的方法是构造数组 int[] arr = new int[2^32 - 1], 遍历文件中的40亿个无符号整数, 每遇到一个数num, 就将 arr[num] = 1, 最后数组中未被标记为1的下标就是没有出现的数, 但是需要内存空间 42.95亿 * 4B = 171.8亿B / 10.8亿B(1G) = 15.9G, 1G内存显然是不够的.
	  
	  问题2回答: *使用位图,* 需要内存是 (2^32 - 1) / 8 / 10^ 8 = 5.36 G, 每个位0或1表示该index对应的值是否出现.
	  
	  问题2拓展问题的回答: 
	  1）10MB和3KB的问题解决方法是一致的，只是内存空间的量级不太一样。整体思想可以被概括为“利用区间计数来判断某个区间内是否存在未出现的数”。拿3K举例，3KB/4B = 3000B/4B= 750, 我们选取离750最近的2的整数次幂512， 无符号整数的数值范围是 0 - 2^32 - 1，将其划分为512个相等的区间则每个区间的大小为 2^32 / 2^9 = 2^23 = 8388608， 则这512个区间分别为【0, 8388608 - 1】, 【8388608， 8388608 * 2 - 1】，【8388608 * 2，8388608 * 3 - 1】，..., 【8388608 * 511, 8388608 * 512 - 1】, 创建数组count_int_num[512] 来分别存储这512个区间内的整数的个数，如果count_int_num[index] < 8388608, 则说明index区间存在没有出现在文件中的无符号整数，那就需要继续在【8388608 * index, 8388608 * (index + 1) - 1】这个区间内搜索下去，继续将这个区间等分为512个子区间，8388608 / 512 = 2^23 / 2^9 = 2^14 = 16384，即【8388608 * index， 8388608 * index + 16384 - 1】，【 8388608 * index + 16384， 8388608 + 16384 * 2 - 1】...。 2^14 / 2^9 = 2^5, 再划分成512个子区间则每个区间只有32个数；32个数不用继续划分子区间了，直接遍历一遍就可以找到1个未出现的无符号整数。*可以对上述过程进行总结: 假设无符号整数为 Y Bytes = 8Y bits, 给定的内存空间为 X Bytes， 我们能够构造的 整数数组（int型 4 Bytes， long int型 8 Bytes）最长为 2 ^ max_len = 2 ^ ( floor（log2（X / Y））)（向下取整），长度要求为2的某个整数次幂是为了保证每个区间上的数值范围是一样长的，方便代码的编写。无符号整数的数值范围为【0, 2^(8Y) - 1】 , 数值范围的长度为 2^(8Y)， 2^(8Y) 不断划分2^max_len个区间块，直到这个区间块的数值范围小于等于 2^max_len, 总的划分次数为 floor（8Y / max_len）。在给出的例子中，Y=4, max_len=9, floor(4 * 8 / 9) = 3, 即只需要划分3次就可以。*
	  2） 使用三个变量：*使用二分法来解决，二分法如果直接作用在待操作的数组本身必然要求这个数据是有序的，但是如果作用在索引数组等辅助数组（包含待操作数组的相关信息）上并不需要待操作数组是有序的。*这里我们实际需要4个变量L, R, mid，left_num, 因为mid = （L + R）/ 2，可以做为L和R的中间变量，所以也就说只用使用三个变量了。在本问题中辅助数组是【0, 1, 2, ..., 2^32-1】,  L = 0, R = 2^32 - 1, mid = 2^31， 遍历一遍40亿个整数，使用left_num统计其中在【L， mid】间的个数，如果left_num >= mid - L + 1, 说明【mid+1， R】必有未出现的无符号整数, L = mid + 1；如果 left_num < mid - L + 1,  说明【L，mid】中必然有未出现的无符号整数，人= mid - 1.  *究其原因， 是因为【0, 1, 2, ..., 2^32-1】一共有42亿个整数取值，而文件中只有40亿个整数，所以可能是左半区域满但是右半区域不满、右半区域满但是左半区域不满，左半区域和右半区域都是不满的（这里只需要找出一个数值，所以这种情况选择哪边区域进行递归查看都是可以的）*
	  
	  题目4的回答：使用位图，但是使用两位来表示一个无符号整数出现的次数，初始化为00，表示没有出现过，出现1次设置为01，出现2次设置为10，出现3次及3次以上统统设置为11.
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2NTIzMzc
	  #+flomo_id: MTg2NTIzMzc
	  #+created: 2022-03-16 20:50:15
	  #+updated: 2022-03-20 00:22:24
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/14475d6744d11b4e29acbc96c0dd303b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=NSViLLWfyxaNy4QLQ06AJTIDBNU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/6e236843c9717006b085cd88f8a67180.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=OaD93V%2F5fB1c9sDBL6N9X2D8dVI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/7c01117b7fed3216ec18f3f2ecd333ee.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=vheFc3Wi0FFkqRiwom0v%2F%2FqEhX4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/af0b988e0a49c94d4112c5ba6452971b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=sFtyxw4tmpRocyCBcA8NxVt1VZ8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/b36ac98e7baa5cb08663f88cf53898ec.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=PjHJq0eRXdTvYRGC5iVoOs%2BiltI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/8f05b7928b83886bd5f168b836f55d59.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=fNuKDFkzCOMomQ7VGYa2f%2FqN2Ws%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/e5047926f942fd4858cf9d28e1d7f448.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=R7eqAWBD9jB6pbpb6fWte2U5Dhg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/d310378e1bc4122f5346c4dd10406666.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ZKfmCtKSI%2ByQKPjOPoY1gYpTOMk%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/680d1c866ed32471c7d399dba6a69df3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=KfZRin7PpwfKJk9sXDX1nAD4l94%3D)
		  #+isImg: true
		- 2022-03-16 21:08:22
		   #Algorithm/资源限制类题目 
		  https://flomoapp.com/mine/?memo_id=MTg2NTIzMzc
		  
		  *设空间原长为len，当len为奇数时，二分法每次划分的左空间长度比右空间长度都要大 2，因为此时左半空间占了所有数中最中间的那个数，左空间长floor（len/2） +1，右空间长 floor(len/2) - 1；当len为偶数时，二分法每次划分的左空间和右空间长度相等，均为len/2。*
		  
		  因为L=0， R=2^32-1，二分一次，左右空间大小均为2^31； 很明显左右空间长度均为偶数，所以不断划分下去也都是偶数。
		  
		  此问题中二分法结束的标志是划分的子空间长度为1。*当子空间长度为2时，此时L=x，R=x+1，此时进行再进行最后一次二分，mid=L=x，*若【x，x】区间内的计数结果大于等于1，而【L,R】区间内的计数结果必然是小于2的，这就意味着R是一个未出现过的无符号整数，而若【x，x】区间内的计数结果是小于1（也就是说0），则必然L是一个未出现过的无符号整数。
		  
		  所以其实只需要划分32次就可以找到答案。
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2NTM5NjU
		  #+flomo_id: MTg2NTM5NjU
		  #+created: 2022-03-16 21:08:22
		  #+updated: 2022-03-20 10:45:50
			- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/bb87c460c85bb9907ca7721171bdc49a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=DfDKpyF8nm6tOgWreN9tm2cykrg%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/5e848cab6d04b614cbe7e4eedc6521d8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=TBKvnMNprRsygbJKQ4030z%2BJ1Vc%3D)
			  #+isImg: true
			- 2022-03-16 22:18:45
			   #Algorithm/有序表的原理、应用和拓展
			  https://flomoapp.com/mine/?memo_id=MTg2NTM5NjU
			  1）原问题
			  问题分析：此题的隐藏要求是时效性，所以一般不能使用单CPU。这里遍历100亿个url以及创建对应的哈希表格是不可行的，遍历的时间复杂度和存储表格的空间复杂度都是巨大的。此问题其实很多细节没有说明，这是需要训练面试官去declare的。
			  
			  核心：在url种数上尽量均分
			  
			  问题解决：将每个url通过哈希函数f 隐射 然后对 m 取模 得到计算结果res，m指代的是机器数量，可以向面试官询问机器数量，这里我们假定m=1000。将每个url分别发送到res对应的机器上去，依据哈希函数的机制相同的url必然被发送到相同的机器上。给定的包含100亿url的文件，其对应的url种类最多为100亿，平均发送到每台机器上的url种类数最多为 100亿/m = 100亿/1000 = 0.1亿 = 1000万，构建的 url-频数 的哈希表 最多耗费的空间为 1000万 * ( 64B + 4B) = 68 000 万 B = 6.8 亿B = 0.63GB。但是如果每台机器依据任务这个空间比较大的话（当机器数比较少时会出现，m=1000时并不会），可以使用另外一个哈希函数f2 再取模，将这个文件划分到各个小文件里面去。这多个机器是并行处理的，加快了速度。（这里f2一定需要与f1不同吗？f2 + 取模 一定要与 f1 + 取模 的结果不同，f2和f1可以不同但是此时取模的对象一定要不同， 原因很简单，映射到同一个机器上的url 其 f1 + 取模 计算结果是相同， 第二次隐射到小文件 必须使得 f2 + 取模 结果不同，才能把同一个机器上的url区分开）。在每个小文件上找到重复的url，然后使用mapreduce合并所有小文件得到每台机器上重复的url，再把每台机器上的url进行合并得到总的重复的url。
			  
			  2）拓展问题
			  找到top100有两种方法。
			  
			  第一种是外排。先在同一台机器的各个小文件间进行:每个小文件先按照url的频数由高到低排序; 然后取出每个小文件上的第一行记录, 比较这些记录的频数, 取频数最大值的数得到top1, 然后在对应的小文件里面删除掉top1所在的记录; 再次取出每个小文件的第一行记录, 重复上述过程,得到top2 ; ...; 得到top10后停止。 对每台机器的top10同样适用外排法进行合并排序，最终得到top100。
			  
			  但是外排不够快，我们可以使用二维堆结构来解决。思路很简单，以小文件之间的合并举例，机器之间的合并是类似的。每个小文件各自建立一颗大根堆，根结点对应的是该小文件中频数最大的url。所有小文件所对应的大根堆通过各自的根结点连接起来，连接方式同样是大根堆。从根结点组成的大根堆中取出堆顶，得到top1，然后调整top1所在的小文件大根堆，最后调整根节点之间组成的大根堆并取出堆顶，得到top2，不断重复“取出堆顶后，调整堆顶所在文件的大根堆，将新的最大值放在原来的堆顶位置”以及“调整根节点之间连接成的大根堆”过程。
			  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2NjA3Mzk
			  #+flomo_id: MTg2NjA3Mzk
			  #+created: 2022-03-16 22:18:45
			  #+updated: 2022-03-20 13:04:20
				- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/538cd15ea709b32a8fff9a54cb62e9db.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=tSKuvWaW8jb898tMsVNx3imEGWU%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/8d23d8d540ae6130dfa450e8a435a531.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=kOYY9cCxHUm9pjj9SBpR%2F0YSSjs%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/78b7524cb8ae97fa26fc170ec2909df7.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=udhiyM0n107qfhFT2S2CGoL3KJY%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/c0bbd73d0376c13758e53d6d3df9636a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=u9yW4PTiLxTLkzMGKajdrYd0BeQ%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/f8d57ff3c86289e8969101b6f4248c15.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=qugzSq%2BrNnGhHdFgrLzM8Xh3tBQ%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/7a54c35463ce7e77bbd0cfff07ced796.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=FBlkbv8m4dfc8P6Jsk308oTryU0%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/c2e4895139d2249c2c6c450e36bbdb33.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=mse84GO816hNTWqQPZ0ob1IWyJA%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/7719acb63f105e3f67f55022a1bf55dd.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137934&Signature=hrCEun16wIlkdv27P%2FL6XGuU5vM%3D)
				  #+isImg: true
				- 2022-03-16 23:18:42
				   #Algorithm/有序表的原理、应用和拓展                                        https://flomoapp.com/mine/?memo_id=MTg2NjA3Mzk
				  
				  问题5题目分析：暴力思路是对整个数全部进行排序，找到中间的数即为中位数，但是很明显内存无法价值全部数据，无法进行排序
				  
				  问题5问题解法：还是利用区间划分的思想，划分成512份，构造数组accumulated_number,  accumulated_number[i]表示从0区间到i区间的区间计数的累加和，这里共40亿个数，我们需要找到 满足accumulated_number[i-1] < 20亿，accumulated_number[i] > 20亿 的i，则中位数一定在i所在的区间范围内，再在i这个子区间内寻找 20亿 - accumulated_number[i-1]个数就行。
				  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2NjY2NjA
				  #+flomo_id: MTg2NjY2NjA
				  #+created: 2022-03-16 23:18:42
				  #+updated: 2022-03-20 20:35:38
					- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/6daebf3d88a30147d2b8889da9b4a55c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=ui0c%2Bz1GuREpne%2BsrV3mrTxLpGY%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/f78872c08c5f77e26c4848b92a6ff514.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=Vo7629KI0tGMer16FEqmwuTp5Ck%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/c60a38136b5e5f43a220329493ec987b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=BhKUCEdadUq8VOB2XTcJ%2BcmrCFY%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/9fa7db374dc209df4fe715581890082e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=XDVO%2FxxTg6HNjKRIsOtdhaZe5DU%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/2b59ec5f0496cf00c1d8fb76ba2c3a92.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=cSgpUcS2IzkyuKNajEem9BP%2F5ow%3D)
					  #+isImg: true
					- 2022-03-16 23:33:12
					   #Algorithm/有序表的原理、应用和拓展
					  https://flomoapp.com/mine/?memo_id=MTg2NjY2NjA
					  
					  问题分析：10GB / 4B = 2.5G，也就是使用5G的内存空间对 2. 5G 个int型的整数进行排序，但很显然5G的内存一次性只能装下一半的整数。
					  
					  解决方法：
					  1）需要使用map和小根堆两种数据结构来辅助解决。小根堆里每个结点为（num，frequency），即值为num的数出现的频数，堆的排序是按照num的数值而非频数；而map里面存放的是（num，index）, 指代的是数num出现在小根堆中的index，这里的小根堆数一般不用链表而用数组存储，所以小根堆的根结点index=0。小根堆中的结点数和map中的记录数始终相等，记作m, m表示：利用map和小根堆通过一次性遍历能获取前m个大的不同数值（不考虑重复值，重复值看做相同排名）
					  2）以【3,2,1,4,5,5,6】为例说明整个过程：为简单起见小根堆和map里只存放两个数，3并未出现在map中，(3,1)创建为初始堆顶，map中增加1条记录 (3,0)；2并未出现在map表中，(2,1)先作为(3,1)的左孩子插入堆，后调整为(2,1)为堆顶、(3,1)为左孩子，map中修改原记录并增加一条新记录, 即map = {(2,0), (3, 1)}；1并未出现map表中，1比堆顶的元素要小，无需加入堆中，继而也无需加入map；4并未出现在map表中，但4比堆顶的2要大，(4,1)替换堆顶的(2,1)，堆再进行调整变成(3,1)为堆顶、(4,1)为左孩子，map变为{(3,0), (4,1)}; 5未出现在map表中，但5比堆顶的3要大，(5,1)替换堆顶的(3,1), 堆再进行调整变成(4,1)为堆顶，(5,1)为左孩子，map={(4,0), (5,1)}； 5已经出现在map表中，对应堆中的结点频数加一，变成(5,2), map表不变；6未出现在map表，6比堆顶的4要大，(6,1)替代堆顶的(4,1), 堆重新调整为(5, 2)为堆顶、(6,1)为左孩子，map={(5,0),(6,1)}，至此第一遍遍历结束，我们可以得到前2大的不同数值为(6,1), (5,2), 也就是说从大到小排序的前3个值为6、5、5。将目前的堆顶值5设置为t，第二次重复遍历整个数组时跳过大于等于t的所有值，按照第一遍遍历相似的过程建立小根堆和map表，可以得到(4,1), (3,1)；将堆顶值3设置为t，按照第二遍遍历类似的过程可以得到(2,1)、(1,1)， 至此结束。全过程得到(6,1), (5,2), (4,1), (3,1), (2,1), (1,1), 据此可以很方便得到全部的排序结果。
					  3）注意事项：【1】从第三数开始都要与已经建立的小根堆的堆顶来进行比较，堆顶元素相当于是前K大个元素值的门槛，只有大于该门槛，其才可能是最终所有元素中的前K个最大值。【2】频数统计是必要的，可以减少小根堆树的结点数，方便在一次性遍历中找到更多的前k大值，从而能够减少总共需要遍历的次数，降低时间复杂度 【3】可以使用大根堆来实现从小到大排序，只有小于大根堆的堆顶的门槛值，才有可能是最终所有元素中的前K个最小值 【4】map的一条记录包括 32位无符号整数 和 对应的index，因为java中并不支持unsigned int，所以实际需要long类型存储，占用8 B，index的最大值与小根堆的最大长度有关，4B对应Integer.MAX_VALUE差不多21亿，应该是足够了；小根堆中的一个结点包括 32位无符号整数 和 对应的频数，这里2.5G个数也就是接近25亿个数，所以频数也得使用8 B 的long 型。5GB / ( 8 + 4 + 8 + 8) B == 1.92亿，实际小根堆的大小可以设置为1.5亿，能留有余地。
					  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2NjgxNTU
					  #+flomo_id: MTg2NjgxNTU
					  #+created: 2022-03-16 23:33:12
					  #+updated: 2022-03-20 18:03:36
						- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/df5fbf4e3bdf07bf4c06ae5dfcb30a1e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=DjhIVmatQpxEjuyxfn2ePSzIeSs%3D)
						  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/1c0c7b8da8140509fb61a70c782989d7.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=6L%2B5GntdhnbgOZgXUO3jZ1aHXyM%3D)
						  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/df8254b9af2d1ef0bd289e18909fec6b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=G2XZAhlHIKpvsoCV6AE5lndF87A%3D)
						  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/d7015da333459ed3af117646c88eebc2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=lJs3QiyhFZ1pLaJiDpQVt0QT5S4%3D)
						  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/3a09ac2a4d76dfe861b4169a3eff7db1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=hdHqoYCWjh5JCYj6DRDVW9cUt18%3D)
						  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/651e860c4c3cf00b251cb15c50f6a404.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=i1Oh6qBSQ02XFBhVYl8TXqop3u8%3D)
						  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/451e452c8c3b6d43a61e68408ce06ce1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=ZT6PlgywemDaemLAMr%2FRjinw9sU%3D)
						  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/19a2a655b221578b66df99f69e07a681.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=jR%2FwyNoWLS56xPQR5hnQrzneoUc%3D)
						  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/f48a201a69da0ff98aea562513fb2d85.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137935&Signature=cqOiPd3dGhy29ZEEgm9fKY1mcFw%3D)
						  #+isImg: true
						- 2022-03-17 00:33:50
						   #Algorithm/有序表的原理、应用和拓展https://flomoapp.com/mine/?memo_id=MTg2NjgxNTU
						  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2NzMxOTI
						  #+flomo_id: MTg2NzMxOTI
						  #+created: 2022-03-17 00:33:50
						  #+updated: 2022-03-20 10:56:16
							- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-17/370015/2059fb2af394eb94b8e19389561fe62c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137936&Signature=bNLCYnwDrsnuqoW9X41cdZhEl%2B8%3D)
							  #+isImg: true
						-
					-
				-
			-
		-
	-
	- #Algorithm/资源限制类题目
	  
	  谷歌等公司会大量考查并行算法，但是国内少。
	  
	  分布式系统可以利用哈希函数把不同的数据放到不同的机器上去，从而实现负载均衡。哈希函数的key的选择非常重要，其与哈希函数相互配合使得结果非常均匀。假设按照key出现的频率高低可以分为高频、中频和低频三种，我们希望高频数据经过哈希映射后均匀地分摊到三台机器上，中频和低频也同样是几乎均分到三台机器上，前提是高频、中频和低频其各自所对应的key都足够多，如果高频key只有两个，比如“中国”和“美国”，那么这些数据必然只能映射到0-1或者1-2或者0-2两台机器上，另外一台机器必然是分不到数据，必然导致负载不均衡。
	  
	  不同机器上数据的merge使用的是MapReduce技术。
	  
	  * *传统负载均衡的底层数据服务器有什么问题？*
	  根据哈希函数的均匀性，其负载是特别均衡的，但是增加或者减少机器时会特别麻烦。假设原来有0,1,2三台机器存储了1亿数据，现在数据量激增至10亿，需要再扩充3,4,5三台机器，这时候迁移的代价就特别高，因为你必须把0,1,2这三台机器上的所有数据的key重新对6取模，因为key对3取模和key对6取模的结果是没有关系的，比如key=9，9mod3=0，9mod6=3，再比如key=4, 4mod3=1，4mod6=4，所以这整个过程就是全量迁移，也就是所有的数据都要重新计算并迁移到指定位置。同样当移除机器时，也是需要重新计算取模结果的，也是全量迁移。而现实生活中动态迁移数据的需求是非常强烈的，比如双11、过年的数据量会非常大，但是一旦活动结束、年结束数据量迅速下降，所以全量迁移的高频次代价必然不可接受。*一致性哈希就是为了解决此问题的，其既可以做到迁移代价低，也可以做到负载均衡。*
	  
	  
	  * *环形哈希空间是怎么解决问题的？*
	  传统的code是通过哈希函数f将key隐射再进行取模得到的。
	  以md5的哈希函数为例来说明环形是怎么工作的。md5能将key映射到0-2^64-1的空间范围，将这个空间想象成一个环，在环形上0位置和最后一个位置2^64 - 1是相邻的。假设现在我们有3台机器m1,m2,m3, 因为它们可以被区别，所以它们的ip或者mac地址或者hostname是不同的，反正有专属于不同机器的信息。我们假定这三台机器的hostname字符串分别为h1, h2, h3, h1，h2和h3通过md5分别映射到code1, code2, code3，这三个code都是裸哈希值，在一致性哈希里面并没有取模的概念了。code1, code2, code3并不能保证把返回值的环形空间进行均分，哈希函数的均匀性指的是任意相同大小的区域内都有数量相近的数据点，均分是建立在大量数据点上的统计学意义。我们在这里假设code1, code2, code3能将环空间进行均分，有个数据（key=“abc”，value=“25”），将“abc”通过哈希函数f映射到某个code，在【code1, code2, code3】中找到离code顺时针最近的那个，其对应的机器即为该数据应该存放的物理设备。如果【code1, code2, code3】可以把整个【0,2^64 - 1】的哈希域均分，全体数据也能够均分到三个机器上，从而负载均衡。
	  
	  * *环形哈希怎么快速找到一个给定key对应的机器呢？*
	  先把所有主机的hostname映射到对应的code，得到一个code列表T1，比如m1、m2、m3的哈希code列表为【100亿，200亿，4】，很明显我们能够得到一个路由表T2（排序好的哈希code =》对应的机器），其能根据给定哈希code返回对应的机器代号，【4,100亿，200亿】=》【m3, m1, m2】。我们的逻辑端有多个逻辑实例，在每个实例上都保存T1和T2，给定一个key=“abc”，其必然被分配到某个逻辑端的实例上，假设key经过哈希函数计算得到code=8，而 4 < 8 < 100亿，其应该被放在机器m1上。
	  因为这里的有序哈希code表长度为3所以很好找，对于任意长度的表我们采用二分法来查找，其与问题一致：*给定一个有序数组，在数组中找到大于等于给定数num的最左端的元素或者说找到数组中第一个大于等于给定数num的数组元素 *。解法：比较给定数num与arr[mid]的关系：若arr[mid] > num, right = mid - 1，flag[mid]=1；若arr[mid] < num, left = mid + 1, flag[mid] = 0；若arr[mid] == num, 则直接返回 machine[mid]。flag数组中最早标记为1的位置记作index, 则返回machine[index]。
	  这样查找有个问题：当code > 200亿的时候，数组中是找不到大于等于这个值的位 置的，这时候会循环回去，应该放在m3机器上。这在代码实现上还有待研究。
	  
	  * *其仍然存在局限性吗？*
	  存在，1）当开始的机器很少时，不会很离散， 比如2个机器可能会把整个环空间分成了20%和80%这种 2）增加或者删除结点后瞬间都变得不离散了
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg1NjI3MzA
	  #+flomo_id: MTg1NjI3MzA
	  #+created: 2022-03-15 22:03:34
	  #+updated: 2022-03-16 16:54:58
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/81642228a4e76c4d76102fc79f581afb.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ENJScWYyaSmDRs5MmpthYtWvZI8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/14f7e95f32168230548729fa65b2a13f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=A9mom%2BMMLh49eR%2BWQF%2F3OppH3wQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/78ed49933fcc8b846d697655115b39ff.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=J3lW61LuYcRKbTnJidQ4Iaf8D0U%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/05cc0b276a4cae1ef13fde49e95088ca.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=H7EaZnQwPDgt%2Bj%2FarY5Xq8383ts%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/8b473ce2a9ee412c515651484a589dd8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=wiR3QsZRbMqiw5oBRE3tRLlC7zQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/1eb6aca6b0993652034c4a71ed93febb.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=%2BHC2qKaRsiTwhqwPlrMNzuhB2X0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/4b41c98825c6942bf015ba1dd2e85187.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=QY0dGu6gxEki7yqMLbav5%2B5xf1s%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/0c24a27edea48f7c4208176f7e8b54aa.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ZyRJ10FacmzvNA4j8azwEcI2%2F44%3D)
		  #+isImg: true
		- 2022-03-16 00:46:16
		   #Algorithm/资源限制类题目
		  https://flomoapp.com/mine/?memo_id=MTg1NjI3MzA
		  * *虚拟结点技术是怎么工作的，是怎么解决增加或者移除结点时的负载均衡问题的。*
		  之前每台机器是通过主机名或者ip地址映射的code来划分整个哈希编码空间的，虚拟结点技术是针对每个机器使用固定数量num的字符串的哈希code来划分整个空间，比如m1对应a1,a2, ..., a1000共1000个字符串的哈希code空间，m2对应b1, b2, ..., b1000共1000个字符串的哈希code空间，m3对应c1,c2, ..., c1000共1000个字符串的哈希code空间，这3000个字符是互不相同的。
		  
		  *好处：*1）因为每个机器都占据了1/3的环空间，所以均衡，且这个固定数量num越大，就越均衡。2）当添加一台机器，就增加1000个虚拟结点，每个机器占据的空间都变成了1/4，直接就是均匀的 3）删除一台机器，整个空间的结点数变成了2000，瞬间变成了1/2，但是依旧是均匀的。
		  
		  *理解：机器对应的每个字符串占用的环空间都属于这个机器的空间*
		  
		  *答疑：1）*数据不超过4千亿或者说达到万亿级别都不要考虑哈希碰撞， 碰撞了也只是说明这个数据在多个机器里都有。2）虚拟结点之间的迁移怎么对应到实际机器的迁移，这对应于简单的后台路由程序而已。3）机器宕机了数据就没了，但是一般每台机器都会带一个从机来帮助恢复。4）*这种方式同时还可以实现负载管理，假设m1的机器性能比m2,m3都要好，那么可以给m1分配2000个字符串*
		  
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg1Nzc1NjQ
		  #+flomo_id: MTg1Nzc1NjQ
		  #+created: 2022-03-16 00:46:16
		  #+updated: 2022-03-20 10:51:54
			- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/3291152a0a3fb4049dd3e205a1f19e2a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=57nPp6fsqqef2T2KL1M%2BsWxYSuU%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/a516e869df79e3dc4780fa73300f4018.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=FbVK9UFEd8Jhx%2BkFRGvZCFaRcyw%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/0ab6d01f6ae3799899ec177900849760.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=yXHCBsXARB8AeXy87Gso%2FzoVrMw%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/e65131cdc79c93e65bac5db63992a0b3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=rH5hSqQ1k%2BILB6HZABq2uSYeHIM%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/5a3c307ad12f5248b88b0fe46eec684b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=ss8Riyxhe7%2Fn9MCLCc9Ur9MNyYc%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/d242bb0f6eec4ce59e0da4a10bf82a6c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=Dt9Vcc%2FPrC%2BVzT%2Fr%2B%2B2bRiN9HmU%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/913f5a5762083c734fea9d0c9967fa8a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=N3sOTagmE3a2NfgprNAMoQOSGz0%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/885aceb8f5bcd559c42d18085d97cb49.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=c9GAKrlnZp1GuLZ1urw%2BrVi%2FQA4%3D)
			  #+isImg: true
			- 2022-03-16 17:19:52
			   #Algorithm/资源限制类题目 
			  https://flomoapp.com/mine/?memo_id=MTg1Nzc1NjQ
			  应用1：亚马逊的货物摆放不是一个货架很多货物，而是一个货架上各种类型的货物都有，这样无论取货员站在哪个位置都能够快速找到需要的货物。
			  
			  应用2：问题如图2所示，解法是以天安门广场为中心，将整个北京地区进行网格化，原来的每个商家根据其经纬度计算出一个代表其地理信息的标签loc = （row， col）来表示其在网格中的位置，这样我们根据商家的这个方格标签就很容易知道其周围的方格范围，根据邻居范围先定位到周围的方格，再对方格内商家的距离进行精确计算。
			  
			  
			  应用3：岛问题的单cpu算法非常简单，遍历整个方格位置，如果方格=1，则将其标记为2，并递归找到其周围所在的其他的岛的方块，如果方格=2或者0，则直接跳过。总的复杂度为O(N + M)。
			  
			  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2MzY1NjY
			  #+flomo_id: MTg2MzY1NjY
			  #+created: 2022-03-16 17:19:52
			  #+updated: 2022-03-20 10:52:03
				- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/08845bef1d192d64f5ce21f1c40fde87.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=BRYnInln0H7Eq1uE%2BtaQyV1ItHE%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/c8c986c8d6fa7620da7cdc914cad01e3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=c2KGJTLTx30erSbdgGK%2BdRsI220%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/07a0e764e64177f5faabb3ea80e43c61.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=R%2BOFpFBkV9IbTaFQqLSC0GAjvFY%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/1b58a145d12c71f7ecbeb5b2198d5091.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=bGKmeohaxK4f9FtUbVf6WVlLuSA%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/6f89579760e2a0d957a9a9880cf25817.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=%2FNJgLVn1N2m21jCaou%2BMQg9ltiM%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/2c9aa4adba984963377f07341624bce0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=zE7sSWmJBovKyuWYoQwOBgGecSc%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/e3d73c1e887aa7cfb2970306992f5471.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=BLMAEfUVCS%2FR4Q%2BtzqhgzJdABwI%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/a0b08769fa98f825d79ace35094d846f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=jQfjHEZRgQ81Sw37WrbhYNY7MsY%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/10e0f034b24659115ee6c6b2af5fb552.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137937&Signature=KZArN52uRAIelWFtHoKf0ZmHx3M%3D)
				  #+isImg: true
				- 2022-03-16 19:13:21
				   #Algorithm/资源限制类题目 #岛问题 #并行算法
				  https://flomoapp.com/mine/?memo_id=MTg2MzY1NjY
				  还是岛问题，整个矩阵中只有1个大的岛，如果将矩阵分为左右两部分分别交给两个CPU分别进行计算，这时候左侧数据cpu会计算出来2个岛，右侧数据cpu也会计算出两个岛，很明显直接汇总两个cpu的结果是不正确的。
				  
				  怎么合并呢？我们关注两个矩阵的中间分割线。我们使用一个表格来记录分割边界两端中岛结点（是某个岛的一部分）的信息，（所在岛的编号，（i，j））。如此，左边矩阵中有 【A, (0,5)】，【A, (6,5)】，【B, (2,5)】, 【B, (4, 5)】, 右边矩阵中有【C, (0,6)】，【C, (2, 6)】, 【D, (4,6)】, 【D, (6,6) 】。然后我们只对出现在同一条水平线上的两个端点进行合并，不然只有1个端点是岛结点，两边必然不可能属于同一个大的岛。初始总岛数=4，合并时使用并查集策略，最先开始四个集合为{A}， {B}， {C}，{D}，【A， (0,5)】和【C, (0,6)】会合并{A}{C}得到{A，C}，总岛数-1；【B,(2,5)】和【C, (2,6)】会合并{A, C}与{B}得到{A, C, B}， 总岛数-1；【B, (4,5)】和【D, (4,6)】会合并{A, C, B}和{D}得到{A, C, B, D}, 总岛数-1；【A, (6,5)】和【D, (6,6)】发现A和D已经在一个集合里面了。
				  
				  如果有4 * 4 = 16个CPU对应的16个区域数据需要进行合并，我们可以先合并1-1得到2，然后合并2-2得到4，然后合并4-4得到8，最后合并8-8得到16。也可以不这么做，16个区域一次性合并，因为任意两个区域之间的边界是不重叠的，其关联的并查集也不同。
				  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg2NDQ4MzA
				  #+flomo_id: MTg2NDQ4MzA
				  #+created: 2022-03-16 19:13:21
				  #+updated: 2022-03-20 10:53:31
					- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/2afdbe603275b4b2df544c9adf1af6e8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137938&Signature=LaPMOgDjjcrLwyS5Tht7FZnmtWc%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/d8051207a4120bd1f80eecb91cd9de60.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137938&Signature=7Lew5utxLoRHyb71Q7N7JcBE5V4%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/0026e071125ce660a54134a54611d7b9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137938&Signature=ytLpYStd0R4Yh37H%2BYHMsWisNFY%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/991ef3529f952777722ecc1f14d516ef.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137938&Signature=HG4h3WqZGgfKrZcdNXblf%2B%2Fjkq8%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/2132da9c8814ef9d0f61aa8c50d7537e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137938&Signature=Ajs8Aaw%2Fur%2BIo%2BkaLqqcGEo6K2I%3D)
					  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-16/370015/cfd10a5e3bc7d575afaa74d89decf855.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137938&Signature=%2FZ2SSt0in9w2HeSQJmGNg2QMPn4%3D)
					  #+isImg: true
				-
			-
		-
	-
	- #Algorithm/布隆过滤器
	  
	  你有一个爬虫程序在网上进行深度优先搜索，假设这个爬虫有多个线程同时在运行，每个线程会通过一个域名地址不断向下链接下去。当一个爬虫线程发现一个含有病毒或者不良内容或者其他线程已经访问过的url的时候，就会主动把该url加入到黑名单表格当中，当其他线程访问到某个url的时候先判断是否在黑名单里，如果在就不继续下去了。*实现这个黑名单机制就可以使用哈希表。假设网络上最多有100亿个url，每个url约占用64个字节，那么总共需要6400亿个字节的空间，我们粗略认为1G内存可以存放10亿个字节（2 ** 30 / ( 10 ** 8 ) ~= 10.73741824），那我们需要640G。*
	  
	  布隆过滤器可以实现黑名单，但是很大幅度节省内存空间，在这个例子中布隆过滤器大概只需要30G的内存。
	  
	  *1）需要了解位图的概念*
	  位图将一个int数组的每个bit位的0/1都给存储起来。需要注意对每个int值的bit存储顺序，比如数组 arr = [2, 4], 其bit表示为 arr = [ 00000000 00000000 00000000 00000010, 00000000 00000000 00000000 00000100], 但是*其位图不是bit表示的直接拼接，而是 2的bit位表示 的颠倒 + 4的bit位表示 的颠倒。 也就是说位图的存储是从低位到高位的，而不是计算机组成原理进行运算的通常的高位-低位的表示方法。*
	  
	  *2）关于位图的操作*
	  包括获取或者更改指定位置pos的bit值。pos/32可以定位到该pos对应的arr数组中某个整数元素的index，pos%32可以定位到该pos在该整数元素的bit表示中的位置index_in_int, *（arr[pos/32] >> arr[pos % 32] ）& 1 能够获取bit值（>>或者<<运算都是int的高位-低位表示法在进行移动）。*
	  
	  *3）关于位图的存储*
	  若使用int类型的数组来存储，因为int型一般默认是有符号的整型，其含有的最大正整数为 （2^31 - 1）B / 1G B = 21.47，所以int类型的数组最长能够有21亿，int[] arr = new int[MAX_INT_VALUE] 那么其对应的位图长是 21亿 * 8 = 168亿。如果相要存储更多的位图，可以使用long类型的数组。
	  
	  可以使用二维数组来存储。
	  
	  *4）布隆过滤器(bloom filter)*
	  一个长度为m的位图数组arr（m指代m个bit），初始时全部为0，如果把0变成1就称作这个位置被描黑了。给定一个数num，先用一个哈希函数f1映射到out1, out1再对m取模得到值index1，将arr的index1位置描黑；再用另外一个独立的哈希函数f2映射到out2，out2同样对m取模得到值index2，将arr的index2位置描黑；这个过程不断继续下去，一共使用了k个独立的哈希函数，显然这k个被描黑的位置有可能重复，重复的概率取决于m的大小。用于url黑名单的时候，给定一个url，对其使用布隆过滤器，如果过滤出的k个位置在表中都被描黑了，才说明这个url出现过了。布隆过滤器存在失误率，但其失误情况不会是：这个url是已经被拉黑的，但是预测结果是没有被拉黑，*其失误情况会是：这个url实际没有被拉黑但是预测被拉黑了，原因就是布隆过滤器是用同一个存储空间来存储所有url被过滤后的结果的，比如url1描黑了1,5,18，url2描黑了2,16,30，而url3还没有遇到过，但是其通过过滤器计算出来是1,16,18，很明显按照算法url3也会被标记已经拉黑过。之所以不用不同的空间来存储过滤结果，是因为能最小化存储空间，且通过设置好位图数组的大小m和哈希函数的个数k，能极大地降低失误率。*
	  
	  *5）布隆过滤器的m和k的选择*
	  m的大小与样本的数量有关，*样本数量越大为了减少重复率相应的m也要设置得更大，但是与单个样本的大小无关，*即与32个字节、64个字节样本率无关，单样本容量只是限制了每个哈希函数的输入，需要确保设计的哈希函数能够实现相应大小的输入的映射。
	  
	  要不要使用布隆过滤器，怎么配置？我们需要知道预期的失误率。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg0ODMzMTE
	  #+flomo_id: MTg0ODMzMTE
	  #+created: 2022-03-15 00:50:01
	  #+updated: 2022-03-15 16:11:38
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/44dab36d31b2365ecc1751cac6886b48.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=ARcRFoTiZzZXIx8GtgM6MGBg%2FnE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/20dcea3306a62ddbc0dde280024638bf.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=qlU3cgZu7NxttQJ7jsNMZy6RKMk%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/8660bbc5ee7944a39d57126b8c8cdfc3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=gkBntHufA7Ia1UMhiLi7dc4B5Ro%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/965018e8a5be546e7f2dfe924613e284.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=qg0nOrqSzeNzcely9k8ZIRb%2FTHw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/19569c6c0fa44fa319e793dc618ef0dd.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=B3agfy6KKtZk8EUhsnyJBz6URUw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/a16566f1d64a8de602dd16dfbc8dc670.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=y0xdJ%2BAGmTPCxE9Skm%2F%2Fqdzb%2BuE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/c2309b7596351c54a387c7ae58e3863f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=IxHW9zSwQmkwXQJCdsrcIJ1HB%2BU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/be4d508346ea75c3bb26617049dad3fe.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=xG3dNGZ8h0X8mclCnzjruwllcnI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/c69d9f223f63ed86e316236a28657547.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=d4lDKx1wT06QJfoe2g3Rtf%2BCNzU%3D)
		  #+isImg: true
		- 2022-03-15 16:11:06
		   #Algorithm/布隆过滤器
		  https://flomoapp.com/mine/?memo_id=MTg0ODMzMTE
		  5）通过公式来选择k和m
		  P与k的关系：当k过小时，布隆过滤器不能产生足够的特征，取模的结果更容易重复，拿k=1和k=5做比较，不同的url出现5个相同的描黑位置比出现1个相同的描黑位置更难，就越不容易误判；当k过大时，比特数组空间会很快被占满，会间接导致重复率变高。*两者的区别是一个是特征表达自身丰富性的限制，另一个是特征存储空间的限制。*
		  
		  *对公式运用的注意事项：*公式1和2直接计算得到的m和k称作理想m和理想k，且通常不是整数，我们将其向上取整甚至放宽至更多，得到的称作实际m和实际k。需要注意理想k在计算时使用的m是理想m，而不是实际m。公式3重新计算误判率的m和k都是实际值，因为m和k都向上进行了放缩，所以毫无疑问最后算得的误判率比预期误判率还要低。
		  
		  6）怎么构造k个相互独立的哈希函数
		  只需要首先找到两个独立的哈希函数f 和 g就可以了, 将 f + 1 * g 作为第1个哈希函数，f + 2 * g 作为第二个哈希函数，不断重复这种方式。
		  
		  7）经典布隆过滤器不支持删除表中的元素，但是如果使用2个bit位来表示0/1的话，在特定场景下可以表示删除操作，在这两个bit位描黑一次00变成01, 再描黑一次01变成10，如果删除的话是从10变成01再变成00，见图6.
		  
		  8）布隆过滤器的应用
		  在一个分布式系统里，有很多的小文件，要在这些小文件里面查找某个字符串str。做法是每个小文件会有一个布隆过滤器，判断str是否在某个小文件里先判断这个小文件的布隆过滤器是否为全0，如果是全0，则肯定不在该小文件里，str只需要在布隆过滤器不全为0的小文件里面来进行查找。
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTg1MzQ1NzA
		  #+flomo_id: MTg1MzQ1NzA
		  #+created: 2022-03-15 16:11:06
		  #+updated: 2022-03-20 10:49:04
			- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/f4697545d5d15756646d2e7e2f57b1ae.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=VIXEpVy5CELSW%2BpMcVrDKT8Ras0%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/151d6922d9bd11f06bfb8bb77781e09b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=o81vfQ1LhJ3IvzmIwRmnu1J4GXM%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/8df70814c1791a405364f5571153cf2c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=n2ZVMrkGkc5u1mp03PTsbXgxw9k%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/a34e60ae86deea2fc1d0c28cae2abcaf.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=YJ3O%2FqMift1Q9O9jIWid%2Fm8CTvY%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/be3c56ede9bb48e0d6cb01d89ca821fa.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=GOsbgsv8%2F1eqGbcWGreJPTi7e6M%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-15/370015/38e9c1889255e81d0ec21743e65e7340.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=o1Qc8xl8J5Rdwukdl89rnfo%2Fl8w%3D)
			  #+isImg: true
		-
	-
	- #Algorithm/哈希函数 
	  * JAVA中的hashcode是很简单的，一般哈希函数可以认为结果是正数。
	  
	  * 哈希函数的离散性和均匀性其实是一个意思。
	  
	  * 若对哈希函数（输入为in）的输出out再进行取模，如果取模的结果是比较均匀的，那么证明这个输出out也是比较均匀的。
	  
	  * 哈希函数不是一个随机函数，因为对于同样的输入有相同的输出！随机函数应该是每次对于相同的输入输出可能都是不同的！
	  
	  
	  *问题1：哈希函数的各种操作都被视作是O(1)，是真的达到这么低的复杂度了吗？如果不是，哈希函数具体有哪些降低操作复杂度的方法呢？*
	  解答1：
	  哈希函数的复杂度如果具体计算的话并不等于O(1),但是因为有很多优化策略其复杂度降低为了小常数，所以被视作O(1)。
	  
	  举例来说明这个过程，若要从40亿个正整数组成（每个整数4字节）的文件中构造一个哈希表，若这里的哈希表为 正整数值-出现的频次，因为出现的频次也是整数，所以哈希表中一条记录共需要8字节，因为4字节即32位的最大正整数为 2^32 - 1 = 42 94967295 > 40亿 = 40 0000 0000，所以这40亿个整数完全有可能都不相同，所以需要的最大的哈希表的空间为 40亿 * 8 B = 160亿 B，毫无疑问这个空间远超一般的内存大小，1GB的内存 = 2^30 B = 1073741824 B， 160亿B 大概需要的内存空间是 160 * 10^8 / 1073741824 = 14.901161193847656, 也就是约15GB大的内存才勉强可以满足，但是考虑电脑中其他基础软件必然占用不少内存，实际需要的内存要远远大于15GB。如果只有1GB的内存大小用于加载哈希表，要怎么做呢？1GB / 4B = 2^28 个整数 = 2. 68亿整数，为了计算方便以及留有余地，我们假设1GB内存可以存放1亿个整数，所以我们只需要将该哈希表记录中含有的整数个数降低为1亿即可。*我们的做法：将数字num经过哈希函数f映射后的结果out再对40取模，这样0-39这40个数每个数分别对应长度约为1亿的链表，再加载到内存时只需要加载0-39其中一个链里面的就可以了。*
	  
	  实际问题中，为了保证每个余数对应的链表访问时间不会太长，我们希望每个链表的长度不超过6，如果数组num很多导致现在每个链表长度几乎都达到了最大值6，我们将取模的数值扩大一倍，在这里就是对40 * 2 = 80取模，把原来0-39链表上的结点对80取模然后挂到0-79这80个链表上，*这个过程叫做扩容，每条链的长度又降低为3个。*
	  
	  *链表应该为有序表，这个顺序根据具体的语境来判断，如果没有规定的排序方式，可以采用 num结点的内存地址、num结点的值、num经过哈希函数映射的结果out这三种方式来排序，最推荐最后一种方式。扩容的次数为O(Log2N），扩容一次的时间复杂度是O(N），分摊到每个结点上的扩容复杂度为O(Nlog2N）/N = O(Log2N），但是因为使用的数据量不会无限大，扩容的实际频次肯定是不高的，所以可以看做是O(1）。*
	  
	  *其实这样理解O(1)是错误的！因为扩容一次的复杂度不能笼统地都算作是O(N)。*当初始只有1个链表（挂上1个结点）时，再加上1个结点就需要扩容，此时扩容代价为 2； 当扩容为2个链表（各自挂上1个结点）时，每个链表再加上1个结点就需要扩容，此时扩容代价为4；当扩容为4个链表（各自挂上1个结点）时，每个链表再加上1个结点就需要扩容，此时扩容代价为8；当扩容为8个链表（各自挂上1个结点）时，每个链表再加上8个结点就需要扩容，此时扩容代价为16; ...; 当扩容至N/4个链表（各自挂上1个结点）时，每个链表再加上N/4个结点就需要扩容，此时扩容代价为N/2；后面不会再从N/2个链表扩容至N个链表了，因为这样跟没有取模没有任何区别，N太大同样无法存储，实际可能都不会扩容至N/2个链表，可能是N/4, N/8等。*这个总复杂度为 2 + 4 + 8 + 16 + ... + N/4 ，其可以被证明能够收敛到O(N), 再均摊到N个样本上就变成了 O(N) / N = O(1) 了。*
	  
	  可以通过离线扩容的方式来改善用户感受到的速度， 也就是完全扩容完成之后用户才能感受得到。JVM中可能会有相应的实现机制。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTgxNTM1MDY
	  #+flomo_id: MTgxNTM1MDY
	  #+created: 2022-03-11 11:47:02
	  #+updated: 2022-03-16 17:24:17
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/1208808c6d27db2fea98fb5dac5cd7ff.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=UVxq%2BV5uz6oD2WVcMUyXOXupndk%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/27fd89e76393c8d3b1a8aa4d271be5c6.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=g1YLqAS3ZzUWg8nmCV2TuWv70b0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/fa4f99754e742ee57f19648488050aa0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=GRXP6I3pvdYzDFA3H6Ti8GurRag%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/32c2869cfbc4f0273ab6f9ca883ae3d3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=cvU5uGG3b4yNMrUjhtGAPN3x70o%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/be2f496646a25a6606d9593d5ee6f919.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=zHVT9akTuSgynKwFwr8G%2FSXtDEQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/3c1be23e1a575ca9710d9d9459672635.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=KfyOrG17rWlzET8J3%2BaY1DOVtUI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/d8ca14e97181a7891b4f8b868d2a78f1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=T%2BT9f5GtEsQaYdRRPYD5BbqPCsg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/4f6abb78e4d0a8acc4bf7160f4a39e30.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Wsb7F85ZPdn%2FdQ8MzmONplcYvU4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/bf3b28c2b2615dd728950ef51d55a581.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=sUlY7ew9CelQ1ejqZ2nmuLAjClI%3D)
		  #+isImg: true
		- 2022-03-11 18:08:39
		   #Algorithm/哈希函数                                                                          https://flomoapp.com/mine/?memo_id=MTgxNTM1MDY
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTgxODU1NTA
		  #+flomo_id: MTgxODU1NTA
		  #+created: 2022-03-11 18:08:39
		  #+updated: 2022-03-20 10:49:41
			- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/d99ffbd21bff24ed5ec75532a3062290.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=rw%2F7Xdl%2FlSp%2Bnz5eHGHgkZN2HLg%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/7ad0679e32d1e7d69e7b03c6802cf7c4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=nimIOruHXPy%2BBPw9mHygakCespg%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/1bece2d87754696c8f4749447d2c4a4a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=yVQ8K0PXtZTZsB8lknKqIM4FZHo%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/0d9e6e592b3d741e64f978b62e45f21e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=s9NLGn8Kov8XqjrEwljyOaYBLr8%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/d2685321a472f323eda7291c7f6c7384.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=CV7tZN2843g6r7L7C3%2Flc5WFZgg%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/ee50c09905ae82fb728e62d8911db25a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=KP%2FaQ%2F0pxCF4kX5F5Fg874U%2FOEI%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/dbe6c10c3646eb4102216a07df4fcd0a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137939&Signature=vtdzFSif14wbb540x2yxIURXF3Y%3D)
			  #+isImg: true
		-
	-
	- #Algorithm/数组累加
	  *解答4：最硬核的累加问题*
	  
	  直接给出复杂度为O(N)的解法：
	  1）*首先需要从后遍历一遍原数组，得到两个预处理信息，数组minSum和数组minSumEnd。*假设原数组为arr[L, R], 则minSum[i]表示以i为起点的所有子数组中和的最小值，也就是arr[i, i] , arr[i, i + 1], arr[i, i + 2], ..., arr[i, R]中的最小的数组元素和，minSumEnd[i]表示与minSum[i]相对应的子数组的右端点（闭的）。
	  
	  实际计算过程中对于每一个位置i，不可能罗列以i为起点的所有可能的子数组，这样导致的时间复杂度必然为 O(N^2)。*实际上minSum[i]依赖于minSum[i+1]：若minSum[i+1] < 0, 则有minSum[i] = minSum[i+1] + arr[i] ； minSumEnd[i] = minSumEnd[i+1]；若minSum[i+1] > 0, 则有 minSum[i] = arr[i], minSumEnd[i] = i；若minSumEnd[i+1] == 0, 则有minSum[i] = arr[i], minSumEnd[i] = i 或者 i+1 ，推荐使用 i +1, 因为这样对于同样小的sum值子数组对应的长度更长。初始时有minSum[R]=arr[R], minSumEnd[R] = R， *这整个过程其实就是dp的思想。
	  
	  2）先说明未被优化的解法。*从左到右顺利遍历整个数组，遍历到每个位置i，查找并计算以i为起点的满足数组元素和小于等于k的子数组的最大长度Li，最后比较每个位置处的Li即可。说明一下如何利用预处理信息来计算Li：判断i位置的minSum[i] 是否 <= k,*
	  *如果满足则跳到minSum[i]所对应子数组的下一个位置即j = minSumEnd[i] + 1处，判断 minSum[i] + minSum[j] 是否 <= k, 如果满足继续跳到minSum[j]所对应子数组的下一个位置即t = minSumEnd[j] + 1处，然后继续判断 minSum[i] + minSum[j] + minSum[t] 是否 <= k, 如此反复进行下去，直到 子数组的sum值的和大于k，设这最后一个子数组的起点为 End， 则 得到一个可行解的长度为（End - i）。*计算Li的时间复杂度为O(N), 总的复杂度为O(N^2)。
	  
	  3）再说明优化的算法。2）中算法复杂度高的原因是必须对每个位置i重新进行判断，优化的关键是怎么利用位置i和位置i+1之间的关系。
	  
	  假设minSum[i] = sum0, minSumEnd[i] + 1 = end0, 也就是说从i开始一直加到end0位置arr数组的元素和刚好开始大于k， *很明显对于i位置开始的子数组空间考察完毕*。
	  
	  *让我们开始考虑i+1位置*，但是这时候从i+1位置开始的子数组空间的右端点我们不再从i+1位置开始考虑，而是直接从end0位置开始考虑。为什么呢？因为我们问题的目标是要找到满足条件的子数组的最大长度，如果[i+1, end0]这个区间（该区间长度刚好等于i位置的子数组长度最大值）都不能满足条件，那么以i+1为起点的子数组空间不可能有更大的目标解，就无需继续考虑了，如果[i+1, end0]这个区间能满足条件，则可以继续按照位置i处的方式不断向后延伸，这时候的end必然会更新，设更新的值为end_update。
	  
	  *然后我们考虑i+2位置*，这时候从[i+2, end_update]这个区间开始判断（arr[i+2, end_update - 1] + minSum[end_update] <= k）, 展开类似于i+1处的过程。
	  
	  需要注意一个比较特殊的情况，当从i+1到end0 - 1位置的每个位置都不更新end值时，也就是这些位置都找不到比i位置处更长的满足条件的子数组了，这时候我们就会需要考虑i = end0 位置了，如果 minSum[ end0 ] > k, 那么 此时end0 = end0 + 1，即必须右移。这是因为minSum[ end0 ] > k 说明当前 i = end0位置无需考虑了，需要开始考虑 end0 + 1位置，很明显前面一个位置的end0信息不再具有参考价值，不再能够缩短子数组的候选范围了。
	  
	  *4）容易总结出，整个过程就是下一个位置从当前位置的不满足条件的右端点end开始判断，并且这个右端点end是不断右移的，并不会向前折返，所以左端点i和右端点end的移动都只是O(N)复杂度，总复杂度也是O(N)。*
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTgxMTA1NjI
	  #+flomo_id: MTgxMTA1NjI
	  #+created: 2022-03-10 22:36:09
	  #+updated: 2022-03-15 00:12:58
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/2f2728702972311ac893157975d4e6d1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=dT5aUFQUOPf0Oth3nlBpY6U7zMg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/5465d2fa9a3203968838a9e65926cffd.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=GXM7RAE2MFaVWX3hVUbhXbZaTDw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/928f387f284e09ef2ace3c1cb7e2cedf.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=5joofNhb9HAqJ2mxyDsv%2BgUvqoE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/8005af1cd418a0fe14702e18e9918872.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=0j7ZEgKMHvCvMAslWR0IVqVEKGY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/1c1e9d5045fdfe4fbdbf0182269ba1f3.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=PNRZ3dztGyqTVsXiNaHKtEY9T7s%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-11/370015/3406606fd47bb71cc457a29f71d14a5a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=9uKmJMY8J%2B3XdXRoSlFt4O9a9g0%3D)
		  #+isImg: true
	-
	- #Algorithm/数组累加
	  
	  问题1：数组内元素都是整数，求*累加和为k的*子数组的最大长度
	  问题2：数组内元素有正负0，求*累加和为k的*子数组的最大长度
	  问题3：数组内元素有正负0，求*满足1和2数量相等的*子数组的最大长度
	  问题4：数组内元素有正负0，求*满足累加和小于等于k*的子数组的最大长度
	  
	  *解答1：*
	  通过滑动窗口的方式一边找到累加和为k的子数组，一边统计其长度并更新最大值。设滑动窗口为[L, R]，如果sum_window < k, 则 R++， 窗口右边界向右移动一个单位；如果sum_window > k, 则L++， 窗口左边界向右移动一个单位；如果sum_window == k, 则找到一个满足条件的子数组，其长度为 ( R - L +1) ，接下来窗口左边界或者右边界右移一个单位都是可以的，这是因为如果右边界右移，那么sum_window > k, L++, 如果左边界右移，那么sum_window < k , R++, 这两种选择最终导致的结果都是窗口的左边界和右边界都向右移动了1个单位。初始时L = 0, R = 0， sum_window = 0, 然后遍历数组的过程中窗口不断变换，时间复杂度为O(N)。具体到代码实现的时候R可以是闭区间，也可以是开区间，看哪种实现方式方便。
	  
	  *解答2：*
	  如果有正负0，那么子窗口之间的sum值不具备单调性，移动窗口的左边界或者右边界的sum值都是不确定的。那么哪里能满足单调性条件呢？
	  
	  这里我们不采用左右边界同时滑动的窗口机制，我们采用先固定一边再滑动另一边的单边窗口滑动机制，很明显这分为两类，*固定左边界的右滑窗口机制1，固定右边界的左滑窗口机制2，*这里的固定左边界或者右边界不是说这个方向的边界是永久固定的，而是说通过先固定一边来限定一个子空间。只不过固定右边界的左滑窗口机制是右边界依次从数组的最左端滑动到最右端（每滑到一个位置，左边界从数组最左端滑动到右边界所在的位置）；而固定左边界的右滑窗口机制是左边界依次从数组的最右端滑动到最左端（每滑动到一个位置，右边界自从数组最右端滑动到左边界所在的位置）。
	  
	  在此问题中，*采用机制1的过程是*：从左向右遍历数组元素【L, R】，每遍历到一个位置i时做3件事：1）计算从数组左端到当前位置的累加和sum，很明显这只需在全局变量sum上加上当前位置的元素值即可；2）构建一张表，每条记录代表【累计sum值-累计到sum值的最小/最左的index】，每条记录对应的【累计sum值】是不同的，或者说【累计sum值】相当于是这张表的key值，如果当前累加和sum已经在表格中出现了，不更新其对应的index值，如果是第一次出现，直接添加新记录；3）判断 sum - k 是否在表中有对应的key，若没有，则说明 [L, i], [L+1, i], ..., [i-1, i], [i, i] 的子区间和都不可能等于k，也就是说以i为子空间的终点找不到满足条件的任何子区间；如有，查找该key对应的index值key_i, 则[key_i + 1, i]的子区间和 = sum - [L, key_i] = sum - （sum - k）= k, 且因为key_i对应的是累计和为key值的最早的index，[key_i + 1, i] 是以i为子空间终点且累加和为k的最长的子数组，记录其长度 i - key_i 并更新max_len。*注意事项：创建表格之后，初始化的时候要加上一条 [sum=0, index=-1]的记录，这是因为sum=0除了对应正负数之和抵消的情况，还可能对应空的子数组这一情况。*
	  
	  *采用机制2的方式左程云算法课并没有讲到，按照个人理解其过程应该是*：从右向左遍历数组元素[L, R]， 每遍历到一个位置j的时候做3件事：1）计算从j到数组末端R的数组累加和sum，很明显这个只需要在全局变量sum上加上当前位置的元素值即可；2）构建一张表，每条记录为【累计sum值，累计到sum值的最大/最右的index】，如果当前sum值已经出现了，无需更新index，否则直接增加一条新的记录；3）判断 sum - k在表中是否有对应的key，如果没有，说明以j为起点的任何子数组 [j, j], [j, j +1], ..., [j, R]都不满足和为k， 如果有，查找 sum - k 对应的value值为key_j, 则[j, key_j - 1] 是以j为起点的子数组中满足累加和k且长度最长的，计算其长度为 key_j - j 并更新max_len. *注意事项：创建表格之后，初始化的时候要加上一条 [sum=0, index=R+1]的记录，这是因为sum=0除了对应正负数之和抵消的情况，还可能对应空的子数组这一情况。*
	  
	  无论是机制1还是机制2，整个过程都是进行了一次对数组的遍历，遍历到每个位置都通过key对表进行查询（类似于哈希表查询，时间复杂度为O(1)），并不断更新整张表，*所以时间复杂度为O(N).*
	  
	  *解答3：*
	  解法见图片7，但是存在疑问：连续累计和等于0并不一定意味着连续的1和2，中间可能有很多值是0，所以应该是遇到累加和为0的子数组，如果子数组中含有元素0则直接排除。
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTgwODMzNzQ
	  #+flomo_id: MTgwODMzNzQ
	  #+created: 2022-03-10 17:22:06
	  #+updated: 2022-03-14 21:27:45
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/67f26c61a18b99847c9c51698c388efb.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=fQTBeiQqCrFOmIX5q7IIaaJWoJA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/5b639835f4cb26c6ccbac6a2307464af.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=OPDN5HCvkeTvYwwp7YxB%2B8OBpWM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/933f7090aeeba6fb593c052893565669.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=C11oE2e6d6ph%2Be9IzRYSIgIXsn4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/562a45b5e56ea47621bd47d9d695831a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=L4eOXOg9KH6n%2BVq5E9K7P1exTrM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/b343e6e16d6dd1249815b8409b1eb669.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=dXRlXSwp6IA38Z%2FNWA4BSlUCggk%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/b5764a44ad4930037663b971c7847800.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=VzXrUtQ0a2D%2Ft77yUBgVLUSxcAQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/df678aecae0731e20d1700310c6603da.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=DZ4pk3zhT0v%2FykMMYASimFQBai8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/979988eff7ceccc22898255408159df2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=dyGO52%2FQe%2FXZ3sOtjBNHGaQvAbs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/3286232c500f6d5ed5f1e202a1694d64.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=70ZZur5JtAaIL4oeFZ2rYTyeqKc%3D)
		  #+isImg: true
	-
	- #Algorithm
	  
	  子数组、子串都是连续的，子序列是不连续的。
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTgwODI5NjM
	  #+flomo_id: MTgwODI5NjM
	  #+created: 2022-03-10 17:17:55
	  #+updated: 2022-03-10 17:17:55
	-
	- #Algorithm/矩阵处理技巧
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTgwNjY4ODk
	  #+flomo_id: MTgwNjY4ODk
	  #+created: 2022-03-10 14:40:45
	  #+updated: 2022-03-10 15:42:37
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/aaeffdfab3345b407584a8e094b65125.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=dyJrqrO%2FUhNWywfFcH91hkKUoW8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/235902060419fb559c817f47b0c1c074.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=qxsE1Oh0Ysoymhp9%2BeE4KtVzaPQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/4b8b00ab8e35a70578fc5e18d4b541c7.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=sub7Z6EaR3zwIcAlq7zkZ1sossQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/67e14792c7bc1b41b8014ca549dc944b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=1KBHOKL%2FwVDocmqSHXZdjOF%2F5%2Bc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/b76f4cb9cafb7b35e641764d578b46c0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=DLby6xPrzDT6f06y0qCj1qdfbZc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/c7774c0e0296d725cfc98ce023b2054a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=O38%2FCpzucj%2BcbQqRv7su%2FvQEjP0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/13cf2e29c6b5dd4e0af99662542d0992.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Rh891Gk8wr3SrCxDR7KlC0HdUMU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/a2848ddba46b3a5c14ef44e658fd037c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=Aimiqph1XeO6xvRix%2FK9GzEDUFM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/0778646dc98f96121380e81e98c7bd8f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=dUznZZqqDczydGOH8gWzCwC8UVg%3D)
		  #+isImg: true
		- 2022-03-10 16:01:38
		   #Algorithm/矩阵处理技巧https://flomoapp.com/mine/?memo_id=MTgwNjY4ODk
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTgwNzUzMzk
		  #+flomo_id: MTgwNzUzMzk
		  #+created: 2022-03-10 16:01:38
		  #+updated: 2022-03-20 10:50:15
			- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/50d334ae6f71e39cc70f01b5b81d124c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137940&Signature=Uz7u%2F8RIuOGileFYVmySHmJQysY%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/a47889840522b2361ff6cff16ec618d8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137940&Signature=HWm0JynQyvyCov8GVbm8y45rig0%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/4099203f4025f870948730d2c79c39ff.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137940&Signature=nGv2X7qcUqQf%2BASErKlM4uhJt0o%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/31449b3257438d73083d5bc8301ed680.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137940&Signature=PWxMB60tNuWCQdbAO22fsfdtQYc%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/f560c4018f7fd2a4a67dba68ddbfdcd9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137940&Signature=h0M45yFZsj2qRZdWdELoaYQyXVo%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/2b4c4061416e4dca71a038dbbf3a00c7.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137940&Signature=%2Ftk9qvkmfll4Ud%2Febk0%2FyFSjuCE%3D)
			  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/308a5b753b784f20f0b54c815e9a94c2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137940&Signature=4RTOdR9JhxdzWhwFd5UVDQNo5ro%3D)
			  #+isImg: true
		-
	-
	- #Algorithm/打表
	  * *打表是什么*
	  给定数组arr，求数组中所有元素对应的质数因子的个数总和，比如【4， 12, 16】，4对应1个质数2，12对应2个质数2和3，16对应1个质数2，所以总数是4。
	  常规初始是遍历每个数，然后求每个数的质数因子。假设数组中的最大数为1000，我们只需要建立一个1000以内的数-质数因子数目的表格即可将这个过程的时间复杂度降低为O(N)。
	  
	  * *打表与预处理结构有什么不同*
	  数组的最长前缀和问题中会遇到预处理结构，sum[i] = arr[0] + arr[1] + ... + arr[i], 这个只需要遍历一遍数组就可以得到，这个数组的取值会随着arr数组本身的不同而不同。而打表对应的表格是不会随着arr的变化发生变化的，对应于JAVA类中的static变量。
	  
	  
	  #+memo_url: https://flomoapp.com/mine/?memo_id=MTgwMzU3NTE
	  #+flomo_id: MTgwMzU3NTE
	  #+created: 2022-03-10 09:31:50
	  #+updated: 2022-03-10 14:40:47
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/5806547e5a274511d430a9f05d9c7c72.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=zqoInsjpN9JEauM%2FPJ0LC4ffZ%2FY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/d84277b40bb10531b4502f50ec11a1a0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=UvGTJRklhuDpT2mSwXCcuMHN7CA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/3e58309e3f71b2affc4dc658594fb73f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=MJWaV8sGZZ3K6UbneeIHscbjCeE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/ace149ab8b2cc7aaf06865bf8688d96b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=hgsPJV5Jye%2FMNhfNxbthb441pyI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/a42375eb65c075627e33acbb89daa2d9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=CYax1zau4wPkw7HXOLhZZ8%2F33wc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/fa4086a61645b9743a30026090b55747.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=QePk0XYx%2BTAAsB%2B%2BJf7aOD6SooM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/32606f298dd155bec82815efcb779df9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=z%2BwO%2Bq40QcNfYFGAGSDh%2Bzh3fzY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/c2d8584aeac25befc905c597fff6bf2d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=CIOTr0ezFtn8ifUJE2ElmfOuBzI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-10/370015/add7cf36adbff4ff4ab78aa624cee1c6.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137927&Signature=FXqO8phm%2FSoJ3r1RAB5979PsHts%3D)
		  #+isImg: true
	-