public:: true

	- [[ResNeXt]]
	  collapsed:: true
		- https://blog.csdn.net/u014380165/article/details/71667916
		- https://zhuanlan.zhihu.com/p/51075096
		- ResNeXt旨在对Inception的split-transform-merge结构的transform部分进行改进：
			- inception网络中每个路径对应不同的transform，且在不同的网络层次有不同的超参数设置（过滤器的数量和转化维度），需要确定的超参数数量多；
			- inception系列网络超参数的设定与数据集的针对性比较强，当应用在其他数据集上超参数需要经常修改，因而可拓展性一般；
		- ResNeXt的改进目标：
			- 设计一种新的拓扑结构，使之能统一替换inception的不同路径。也就是说，替换之后的整体结构是，多个并行的相同结构。
		- ResNeXt的改进内容：
			- 将相同结构重复的次数或者说路径数称为基数（cardinality），每个路径仍然使用普通的resnet的三层堆叠结构（1 * 1， 3*3， 1*1），但减少中间层的输入维度和输出维度（开始层的输出维度和最后一层的输入维度也对应减少）；
			- 研究了上述改进结构的两种变种：
				- 变种1：每个分支都只包含前两层堆叠结构，然后每个分支的输出结果进行通道方向上的合并，*合并后的特征图再使用最后一层结构进行卷积；
				- 变种2：使用分组卷积来替换多分支*。分组卷积是介于普通卷积和深度可分类卷积之间的（每个通道都使用一个卷积核）卷积方式，源自：由于硬件资源有限不得将Alexnet模型在两块GPU上训练，而两块GPU的参数是不能直接共享的。
				  *变种1和变种2是与上述改进结构等价的。
		- ResNeXt论文的其他贡献：
		  collapsed:: true
			- 证明了增加路径数比增加网络的深度和宽带要更有效
			- 在不明显增加参数总量的情况下提升了网络的效果，但是超参数大大减少了，方便模型进行移植
	- [[超声图像分割]][[综述]]
	  collapsed:: true
		- 超声图像分割方法根据其架构和训练方法分为六大类：
			- 基于FCN
			  collapsed:: true
				- 1）FCN简介：
					- 是像素级的监督学习方法，将分类网络的全连接层替换为FCN得到，跳跃连接（跳跃层和双线性插值）使得应用任务拓展到密集预测任务
				- 2）例子：
					- 多阶段增量学习和多FCN模块--*CSF-FCN用于*淋巴结分割：*两个基于 FCN 的模块组成，第一个是收集原始图像以产生潜在对象的分割，另一个是使用中间结果和原始图像生成最终的淋巴结分割；
					- 级联FCN网络：为避免边界不完整和模糊，将一个由join算子修改的AutoContext方案植入FCN模型中；
					- 注意力深度监督的 FCN 模型：名为 DSN-OB， 训练粗分辨率层以区分对象区域与背景，训练精细分辨率层以定义对象边界。开发了*一个特定的训练方案和融合层，以避免打破边界，*这是一个常见的超声图像分割挑战。该框架最终被批准分别在血液区域和病灶分割方面具有良好的表现。
					- 为了更好地利用 3D 空间信息，同时充分利用 2D 预训练模型：提出了一种名为 Direction-Fused FCN (DF-FCN) 的导管检测方法，该方法通过重新组织的横截面利用 3D 信息来分割导管。
			- 基于编码器-解码器
			  collapsed:: true
				- 1）架构设计的原因
					- 引入了相反操作，包括卷积和反卷积（或转置卷积）、池化和反池化，*目的是恢复在池化操作中丢失的像素位置信息*
					- *编码器是收集像素位置特征，然后解码器是恢复空间维度和像素位置特征*，可以充分保留和分析特征和像素位置的信息。
				- 2）案例：
					- 2015 年一种完全对称的架构 DeconvNet：它具有反卷积和反池化层，其应用于颈部肌肉的超声分割，比较了与指数线性单元 (ELU) 和 Maxout 集成以解决“垂死 ReLU”问题的性能；
					  动态卷积神经网络，用于超声中的外膜和内腔内膜分割
					- Grouped-Resaunet (GRA U-net) 用于乳房超声上的逐层乳头分割和定位。 使用残差块解决梯度消失问题，使用组卷积提高计算效率，并使用注意力门关注输入的相关区域；
					  提出了一种具有多尺度输入和混合多标签损失函数*的网络，用于在*血管内超声图像中分割冠状动脉；
					- 基于 U-net 的结构将神经架构搜索 (NAS) 应用于语义分割网络，并将其应用于神经超声数据集
					- 与 3D 卷积和残差块集成的V-net：
						- 多向深度监督的 V-net应用于超声中的前列腺分割 ，该网络从解码器部分的每个阶段预测不同分辨率的分割，使用多向轮廓细化处理进行分割融合，并应用逐级混合损失函数来减少收敛时间。
			- 强化学习
			  collapsed:: true
				- 1）介绍：
					- 深度强化学习 (DRL) 是一类*使用神经网络作为价值函数估计器*的方法
					  主要优点是使用深度神经网络自动提取状态特征，避免手动定义状态特征波段。这种不准确性使代理在更原始的状态下学习
				- 2）案例：
					- 基于 Q 学习的超声图像分割方法：
						- 一种多目标医学图像分割框架：每个强化代理都经过训练以找到每个对象的最佳值。每个状态都与定义的动作相关联，并计算惩罚/奖励函数。
						  2013 年提出了一个特定于上下文的医学图像分割框架和在线强化学习。为了使模型适应先验知识/用户的交互，提出了一种适用于大状态-动作空间的通用强化学习
						- GAN
							- 1）介绍：
							       依赖于解决众所周知且具有挑战性的医学图像分析问题（如分割、重建、分类或数据模拟）的能力
							- 2）案例：
								- 可以检测和纠正分割结果和地面实况分割图之间的高阶不一致，在不增加模型复杂性的情况下*强制执行远程空间标签连续性*；
								- 具有*多尺度 L1 损失函数*的新型端到端对抗神经网络：segmentor 和critic 网络被训练来学习全局和局部特征，这可以捕捉像素之间的长距离和短距离空间关系
								  新颖的投影对抗网络“PAN”，它通过 2D 投影表示高级 3D 信息
								- 使用一种新颖的在线对抗性外观转换方法来解决：*对于自动超声图像分割，当遇到外观差异时，即使在对象具有相似结构但外观略有不同的同类语料库上，深度模型也往往表现不佳*
			- 基于RNN的
			- 用于分割的弱监督学习
			- Images:
			  collapsed:: true
				- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-18/370015/1c74322c21944bd2444d6c02637b699b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=zQIBYjHk0J6Xpbo70Jn92KhEYu4%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-18/370015/024f442afe7d8f43faa17c095fcfed84.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=9pUiMWfqZIvzRpzuD%2Bobhe%2FpIrA%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-18/370015/a3ab41258548acc7517950c01b10d2ff.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=6weYRDbiZlOd5iIEpHD9c7NHZhQ%3D)
				  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-18/370015/3cfb85d62faec4300aa54ad2075c3e0a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=WTFzqcwb4RHRo3fRgNTnc2jtmjQ%3D)
				  #+isImg: true
	- [[超声]]
	  collapsed:: true
		- Global guidance network for breast lesion segmentation in ultrasound images
		- 一、从超声波准确分割乳房区域的三个难点：
		  * 由于固有的散斑伪影
		  * 模糊的乳房病变边界
		  * 乳房病变区域内的均匀强度分布
		- 二、本文2创新点：
		- * *提出了全局引导块 (GGB，Global Guidance Block)来提取全局信息：*
		  *让从ASPP提取的多层集成特征 指导 从空间域和通道域中对远程非局部依赖关系的学习过程*
		  * 提出乳房病变边界检测 (BD，Boundary Detection) 模块
		  学习额外的乳腺病变边界图，以提高分割结果的边界细化程度
		  * 补充：
		  * SPP全称为Spatial Pyramid Pooling（空间金字塔池化结构）
		  * Atrous Spatial Pyramid Pooling（可以理解为空洞空间卷积池化金字塔或者多孔空间金字塔池化）
		  
		  
		  三、开始的多层CNN模块
		  * *架构设计：*连续四层CNN下采样
		  * 
		  * 不同尺寸层级的CNN模块的输出结果是resize到同样尺寸（第二个CNN输出特征图的大小）然后拼接在一起得到一个集成后的feature map，然后集成的这个feature map才送入GGB模块中来指导分割的；*这个集成的feature map才是后文中的引导图G*
		  
		  
		  四、GCB模块：
		  【1】设计的目的：堆叠卷积来获取全局信息的方式耗时且不好优化；*乳腺超声图像有很多易于识别的斑点和阴影，在感受野有限的情况下容易被误识别成乳腺肿块*
		  【2】设计的内容：包含基于空间的全局引导块和基于通道的全局引导块。
		  1）前者的本质是在图片的空间大小上运用注意力机制，但是本论文使用的注意力机制在计算权重方面做出了创新，原本的注意力机制是直接使用从原图获取的Q和K内积计算得到的权重W，但是这里是 还引入了一个*称作引导图（GuidanceMap）的输入GM，从GM获取Q'和K'得到一个新权重W’，W'*W再进行softmax作为最终的全局注意力权重；*
		  *2）后者是在图片的通道方向上运用注意力机制，这里权重的计算同样是 原图和引导图上计算的权重乘积再softmax。原图上的权重计算并没有使用经典的QK法，而是将每个通道方向上的所有像素点展开成对应的一个向量，向量之间直接使用内积来得到权重（毫无疑问这样得到的权重矩阵一定是对称的）；引导图上的权重计算相比于原图就多了一次特征图的更新，更新之后的特征图采取与原图完全相同的步骤来计算权重，更新的操作是先对每个通道方向上的特征图进行全局平均池化得到一个一维向量，再对这个一维向量进行两次fc转化得到每个通道上的一个比例权重ratio_w, ratio_w再与引导图相乘就得到了更新后的引导图。*
		  3）空间全局引导模块的原图是：ASPP之后的特征图；通道引导模块的原图是：空间全局引导模块的输出特征图
		  4）通道引导模块 接在 空间全局引导模块 之后 对其特征进行微调
		  
		  
		  *五、BD检测模块：*
		  【1】模块的设计：
		  * BD模块的输入是某一层CNN输出的特征图，这层特征图首先经过1*1卷积得到一个通道数为1的新特征图F， *F与F的3*3最大池化结果相减（论文中是这么写的，但是理论上相减的顺序存疑；这里池化时补充padding=1，stride=1来保持最大池化后的特征图图片大小与原图一致）*就得到乳腺肿块边缘图E；边缘图E与F进行相加就得到了乳腺肿块的分割结果
		  
		  * 是双输出：既输出了边缘分割结果，也输出了整个肿块的分割结果
		  
		  【2】*一些思考和疑问：*
		  * 为啥两个相减就得到边缘曲线了？这里的F和F的最大池化结果到底有什么意义呢？
		  如果按照正常的逻辑去推测的话，因为 F + E = 完整分割结果，所以两种推测：1）F是乳腺肿块去除了边缘的内部部分，但是此时 F - F的最大池化 = 边缘图 就不成立，F - F的最大池化的结果在这种推测下就会是乳腺肿块内部部分的边缘了 2）*F是乳腺肿块整个区域的粗略分割结果，F - F的最大池化 = 乳腺肿块的边缘预测结果 E，F + E 就是粗略结果和预测边缘的一个叠加（对边缘的细化结果），预测的边缘和原始的边缘进行并运算而非二选一*
		  
		  * 问题是这里BD模块的输出是*不直接参与到最终分割的吗？*：
		  是的，从BD模块输出边缘图和分割结果是为了使得初始的四层CNN训练学习到对于最终分割有利的特征
		  
		  【3】注意事项：
		  * *padding是默认全部补0，而不是双线性插值*，且需要注意有时候看到的padding不为0是由于bias导致的：https://blog.csdn.net/g11d111/article/details/82665265
		  
		  *六、损失函数的设计：*
		  * 边缘图的GT的获取：使用*canny边缘检测*算法 https://zhuanlan.zhihu.com/p/42122107
		  
		  * 损失函数的组成部分：
		  一是所有BD模块的边缘图预测损失和分割结果预测损失
		  边缘图损失使用MSE（ （预测结果 - GT）的平方 ）；分割损失使用的是 二元交叉熵损失 + 1 - dice socore；两个损失通过加权来求和，*但是这里没有使用0-1之间的权重，这里是直接让边缘图损失 × 10，分割损失 × 1。这里需要注意：边缘和分割的GT缩小到对应BD的尺寸来计算损失，而不是将BD的输出结果上采样到统一尺寸再计算损失，后面这种计算方式可能误差会更大*
		  二是最终分割结果的损失
		  1 - 二元交叉熵损失 - dice score
		  
		  * *疑点：这里为什么给边缘损失以更高的权重？个人理解这里边缘预测如果因为过拟合或者欠拟合等原因导致预测结果不好的话，会对最后的分割结果有很大影响，而设置成10这样的高比例，会使得边缘不至于跑偏太严重。*
		  
		  *七、其他*
		  GGB中引导图的作用到底是什么？不要这个引导图产生的权重行不行？为什么选择前面CNN卷积模块的特征图堆叠结果来作为此引导图？还可以使用其他的引导图来进行引导吗？为什么空间GGB和通道GGB模块的引导图是同一个呢，前面引导了为啥后面还需要再次进行引导？引导图中到底含有什么信息？GGB模块的参数量是否太大了呢？空间GCB和通道GCB能进行数学上的统一吗？
		  
		  通道GCB里G为什么事先要用通道的权重进行更新呢？利用QKV计算权重和利用内积计算权重各有什么优点呢？为什么这里要分开使用？
		  
		  这里的两处直接上采样都是上采样4倍，这样的倍数是否过大？
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-03/370015/2556ca047520519b4a57e57d5afd2f4b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=lUZqNJ0%2FwrBQhNHi%2BO%2B5TjV2xG0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-03/370015/8bf0039f6b48f048a7d86663183849fc.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=deCtTFBf9Ca41afUyrI6ob84x%2Bw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-03/370015/0072d49451b0d15e0b8b5299e536387d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=ps8eIDI8JnS%2Bt1TEWSRoB99W4zA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-04/370015/41bc2db58491ae5b50a36fcaaa685938.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=0mCCV29ZQpqQBfW5HfW95fN5t8s%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-04/370015/06a1b26e46f42b5f24903d2b4495a40a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=moa0MjBkOY3VKgBoYP8SgKUqB%2BM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-04/370015/84bc480661b764fc9ee495f438b11b40.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=JveP4Bcy5HskvhtTVRPS0RvlZ80%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-09/370015/e50c941b358796af94ef77304b60d368.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=ICeLXwbsKCSRd9FSXmGaW4p3i1s%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-11/370015/bd0780d19aa3bd29bf14840275fd4071.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=EeYYyYbbpx5iB7YErxQf4pUYf2U%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-06-11/370015/b9950ab61df32005bde785e79c55497f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=wTlwKxX7wf1sBF6p%2F9L5GZCK0vI%3D)
		  #+isImg: true
	- [[脂肪肝 ]]
	  collapsed:: true
		- https://arxiv.org/abs/2104.05570
		  
		  * *现有的问题*
		  
		  脂肪活检是脂肪肝变性的金标准，但是执行该步骤导致的风险和代价阻碍了大规模数据集的收集；超声图像-诊断结果 可以从医院的PACS系统中轻松获取，但是由于超声诊断的主观性，诊断结果容易受到诊断者自身或者诊断者之间变化性的影响。
		  
		  * *现有的解决方法*
		  
		  1）包括expectation- maximization(EM)、multi-rater consensus modeling (MRCM)、STAPLE，但是*都需要对于同一个样本有多个诊断者（rater）的诊断数据，而我们数据通常只有一个诊断者*。
		  2）针对1）的现有方法提出了评估标注者混淆矩阵、为每个独立的个体或者群组诊断者训练单独模型等方法，但是存在 *假设并不一定成立、计算开销大等问题*
		  
		  * *本论文模型*
		  
		  *核心思想*：使用一组可学习的潜在嵌入来表示不同诊断者（rater），将这些潜在嵌入进行维度转化和复制操作后，就可以插入到任意主干网络的任意卷积层或者全连接层之后。整个网络关于潜在嵌入没有显式的编码层，而是通过损失函数的约束来自动学习的，所以被认为是基于自动解码器的网络结构。整个网络的损失函数由两个子部分组成，其中一部分是各个诊断者关于每个样本预测的损失值之和，另一部分是各个诊断者潜在嵌入的参数平方和（类似于L2正则项），对该损失函数的求解可以使用梯度下降法。
		  
		  *two insights:*
		  1) 为什么对潜在嵌入进行维度转化和复制操作？
		  【1】因为不同模型的不同卷积层、全连接层对应的维度千差万别，潜在嵌入的维度也可以按照需要人为规定，*为了使得潜在嵌入与传统模型的集成更加灵活，也为了能够不改变传统模型结构进而能直接使用预训练权重*，我们*只对潜在嵌入进行转化操作，并将转化后的潜在嵌入与传统模型的不同子结构的输出进行相加*。
		  【2】注意重复操作是将一个向量重复*总像素数 次数，相当于是把每个评价者的个人评价倾向注入到了每个像素点对应的token里面。*
		  【3】论文中是只注入一次，是否可以在不同子结构处注入多次值得进一步研究。
		  【4】复制、拼接、线性转化是另一种注入方式。哪一种效果好需要实验来证明。
		  
		  2) 损失函数这样设计是为什么？
		  【1】是基于后验概率最大化的统计学原理。论文中的后验概率指的是在已知图像的条件下得到目前潜在嵌入Z的概率，其等于 各个评价者【对应的潜在嵌入的先验概率分布（均值为0的高斯分布）* 在该概率分布下预测正确每个样本的主观标签值的概率】的乘积。
		  【2】具体计算样本预测的损失值时可以采用与任务适配的任何相关函数，包括分割、分类、检测等任务。
		  
		  *训练和测试的trick：*
		  [1] 训练时先对所有的潜在嵌入Z进行训练；然后固定主干网络、其他所有评价者对应的潜在嵌入，在数据集上来fine-tune当前评价者对应的潜在嵌入
		  
		  *优点：*
		  【1】避免像EM算法那样复杂，可以使用梯度下降法
		  【2】算法虽然仍然针对的样本数据是：一个样本有多个评价者的主观标签值，但是在一个样本只有1个主管标签值这样的极端情形下也能够正常工作。保证了应用上的泛化性。
		  【3】可以应用于多任务。
		  
		  
		  *具体实现的相关思考：*
		  【1】 每个潜在嵌入用高斯分布初始化时的方差要怎么设置？
		  【2】这里针对dcm数据要怎么来处理模型呢？把dcm数据变成JPG图片？是使用连续的dcm还是单张的dcm？
		  【3】这里面预训练权重是不加潜在嵌入然后直接用模型训练吗？
		  【4】训练潜在嵌入的时候需要冻结传统模型吗？感觉是不用
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-05-19/370015/cf0ece25f3631fa9973e7304e7f47f63.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=vs86FqI2%2BDdKZ5%2Bs%2F1HTtoHp2mI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-05-19/370015/7a6c87913815b64d62cecf83af4815ce.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=2hIGbyFeZlfaD7KvqvTEtCFV9ZI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-05-19/370015/1e58782a979b552d0ee55c1f7d672cb2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Y9xcNpEcAfupgvrW3AZAhER5A5Q%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-05-19/370015/7409526faf0fbd59b9dbd3ec8bc8e61b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=6RSgoSi0KhJUciFLKf1L%2FbQ1fXk%3D)
		  #+isImg: true
	- [[速记]]
	  collapsed:: true
		- 1. *模型训练的问题：*
		  
		  
		  * *模型在训练集上的结果很差，可能的原因有*：模型参数量过多而数据集过小，模型无法得到充分的训练；自己手动添加的模块导致模型自身所代表的数学函数无法收敛或者说很难收敛。
		  
		  * *模型的预训练权重：除了加快训练，对于最终的结果有着很大影响：*迁移学习也有着很多待学习的知识点，权重的迁移可能是来自不同任务的不同模型。
		  
		  * *模型训练的稳定性（待学习和研究）*：一直以为如果模型中没有随机参数的话模型的反向传播应该是固定的，但是在训练模型时发现貌似是经典模型同一epoch的重复次运行结果不一致，暂未理解原因，有时候模型在不同的设备比如谷歌的colab和服务器上的运行结果也有所差别。如果某个模型某次结果跑的很好，需要重复进行实验来验证。
		  
		  * *样本量小：关注少样本或者零样本数据学习、*医学图像中由于缺乏大量数据导致很多最先进的模型无法使用，意思是效果不佳，所以一方面得提高数据的质量，另一方面得学会让模型减少对数据的依赖，保证模型能够在已有的数据集上达到最优。
		  
		  * *模型过于复杂或者太大：数据少但是模型大并不一定不能训练，可以通过一些训练技巧解决；可以通过模型压缩蒸馏等方式来减小模型的大小。*
		  
		  
		  
		  1. *设计模型的技巧：*因为深度学习本质就是对数学函数的优化求解，组合、拼接其实都是数学表达式的改变，要想真正提高效果，*需要把巧妙的数学关系表达在模型中*。
		  
		  
		  * *通过模块设计来模拟现实世界的语义关系，并尽可能地在增大解空间*（备注：增加参数并不一定能够增加解空间来达到增强模型表达能力的目的【比如自注意力机制的设计为Q、K、V而不是K、V或者Q、V，前者两个向量会由于位置关系不同而计算出不同的权重，也就是说向量1对向量2的权重和向量2对向量1的权重是不同的】，很可能带来冗余参数；*模型语义关系不能够想当然，比如设计一个全部为参数、与图片等大的attention map*来让模型自己学习应该关注图像的哪些部分是不靠谱的）
		  
		  * *注意模型复杂度和数据集的复杂度匹配*。调参，一些重点模块的层数、维度数对结果很可能产生很大影响，这就是与模型复杂度有关。
		  
		  
		  
		  1. *深度学习与其他方法的结合：*
		  
		  * *一般都是在深度学习模型的输入端用其他方向的方法创新，很少直接结合的，目前看到的只有deep random foreast. *深度学习存在比较强的局限性，只用于具有较强规律和较好数据集的情况，对于本身规律性不强、需要很多人工经验的难度很大。
		  
		  
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MjMyNzYwNTM
		  #+flomo_id: MjMyNzYwNTM
		  #+created: 2022-05-06 09:16:17
		  #+updated: 2022-05-06 20:38:02
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-05-06/370015/d3f96f350da4a92230e1b28e11ec1e9e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=QzP8xRJZiZ%2F6BvqnO4x9LOrLza0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-05-06/370015/6d332d8573d1ad28feb1dac1946ed405.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=nrUt0eV%2Bml5kLlzBUt%2BMoxaQS%2FU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-05-06/370015/cba79aab4fdd6ee53398afaf768d4b82.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=%2Fhp7vUSa9hFOJKRT4Nxm6P5Yhbk%3D)
		  #+isImg: true
	- [[速记]]
	  collapsed:: true
		- 因为很多时候不同实验我得出来的是完全相反的结论所以我会陷入不停验证同一猜想的陷阱主要是你在尝试对这个猜想进行实验时设计的实验环节、实验过程是不合理的最基本的是没有控制好变量（原因是实验变量太多、代码改动太大，可能是漏掉了某个变量，也可能是没有改动相应的代码，或者是两者都有、上一次改动的代码没有重置而导致在上一次错误的代码上继续改动）
	- [[Transfomer]][[ACmix]]
	  collapsed:: true
		- *Self-Attention：全部使用自注意力机制进行堆叠*
		  
		  *Attention enhanced Convolution：使用注意力机制来克服卷积局部性的缺陷。主要是通过“连接attention与卷积模块”、“引入关系信息来提供类似注意力的info”的方式*
		  
		  *Convolution enhanced Attention：使用卷积来为transformer补充局部归纳偏置。主要通过“在训练早期使用卷积来保证更稳定的训练”、“增加基于卷积的位置编码信息”、“利用stride卷积来减小注意力所需的参数”。*
		  
		  缺点是：*都只是将卷积核和注意力作为单独的模块，并没有深入的研究它们底层的关系，*导致目前两者的结合都是拼接、并行、替换等简单模式。
		  
		  本文通过研究卷积和注意力的底层数学关系，来得到一个两者融合的新范式。
		  1）对一张特征图进行传统的3 * 3的卷积 等价于：对原特征图进行9种 1* 1的卷积 得到 9个卷积后的特征图，将9个特征图相同位置的特征向量进行相加求和最终得到1个特征图；但是具体计算时为了方便进行向量化，经历了*“对9个特征图分别进行depthwise卷积，一个特征图对应一类位置卷积核” *---》 *“对9个特征图按照维度方向进行拼接，然后按照通道方向分成C/N组，每组都与相同的卷积核（9个位置卷积核拼接组成）进行卷积，每组卷积的结果是单通道的特征图，所有组堆叠起来构成完整的最终的特征图”*---》 *“与上一种方式几乎一样，只是组卷积对应的卷积核变成了可变的参数”* ---》*“为了保持输入的通道数仍然为C，对上一种方式重复了N次，也就是不再是只有1个组卷积核了，而是有N个组卷积核，但是每次组卷积只使用其中的一个组卷积核”*
		  
		  2）对原始特征图进行自注意力操作 等价于：对原始特征图进行三种1*1的卷积，得到三个特征图，分别代表每个像素token对应的query token、key token、value token。然后*在局部范围而不是整张图像上*进行权重计算和加权求和。特别需要注重这里的代码实现（Unfold函数是理解关键），求权重时对于q还加上了不同位置之间的位置编码的差。
		  
		  3）对两种进行结合：
		  *对于给定的特征图 H * W * C，先将其按照多头自注意力方式进行处理，使用N个head，每个head的key、query、value都对应对应H * W * C/N， 一共有3N个H * W * C/N的特征图，然后分出两条路径：*
		  
		  *一条路径继续按照自注意力的方式进行，*每个head通过加权求和得到 H * W * C/N的特征图，N个head对应的特征图按照通道方向进行连接就得到 H * W * C的特征图；
		  
		  *另一条路径是按照卷积的方式进行，*其先是将3N个H * W * C/N的特征图转化成了k^2 N 个 H * W * C/N的特征图，可以理解为N个head中的每个head现在有k^2个（原来是三个）对应的H * W * C/N的特征图了；*对于每个head来说，将这k^2个特征图按照通道方向连接起来得到 H * W * (k^2 * C/N)的大特征图*，*对这个大特征图进行分组卷积，分组的个数为C/N，则每组对应的特征图大小为 H * W * k^2, 每组特征图进行组卷积得到的特征图大小是 H * W * 1，然后所有组得到的特征图拼接得到 H * W * C/N大小的特征图*；对N个head各自得到的 H * W * C/N的特征图进行拼接，得到 H * W * C/N * N = H* W * C的特征图。
		  
		  *但是代码实现与这里的图描述得有所不同，代码实现中是直接把 H * W * C/N * 3N转化成了 H * W * C/N * k^2的特征图了，然后对这个特征图同样进行组卷积，组的个数仍然为 C/N，每组对应的特征图大小仍然为 H * W * k^2, 但是每组对应的卷积输出变成了 H * W * N，则所有组得到的特征图拼接得到 H * W * N * C/N = H* W * C了。*
		  
		  将resnet中的bottleneck的第二个3*3的卷积替换成 ACmin结构，得到resnet_ACmix模型。
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/a00bcbd81aced9f7532d0e5f37bb1de1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=gIMnAbci3GI%2FwjOQvDYor9yfUrQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/d2fa7fa53864ca1baac9d25014ae95b4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=31kv0lSwd%2BVl9ErjNAyAs2%2BcShg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/9a8d4cdf1a0cbb424d1fa8ff4c6f222f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=HR6%2BdZUmhvCNaR5Hlv8z2NXJp68%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/a92432d97c773f535efb8596d31b55e1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=BRpVVNGJWHLvkc1lkydBsfHMLHs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/c80387768b44b9d11fed65837fd4d602.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=deQeNVXXFT5wa1prrRRzyZI2hKo%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/f42b1fef116e010c428356ef352ae78d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=CNWuXiHFIIc4eeRw0Jshhy68phA%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/7ecb1400743d5ec7f6236fe3822d5a6e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=BamqvkuO61qXlAWIOjaxIPloXTg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/7bff5575483f3da0c651fa4e5dc7009a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Ay%2BWqVvKxjY7TgxkKy%2Fr7%2FVwnBo%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-22/370015/6aa5c3f19f237b407469f5a72a49aad5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=xELPnoKzDGvKpTizbR7utAraT%2F0%3D)
		  #+isImg: true
	- [[数据集]]
	  collapsed:: true
		- Dynamic Sampling Approach to Training Neural Networks for Multiclass Imbalance Classification
		  
		  每个epoch在所有的样本上进行训练，这种训练模式存在的问题：1. 如果数据集标签不平衡，那么学习过程会倾向于标签数量多的类而忽视标签数量少的类2. 对于模型f学习作用有限的样本，其会浪费训练时间*3. 如果数据集存在冗余，可能会发生过拟合导致泛化性能差*
		  
		  希望在每个epoch训练时，不选取所有的样本，而是对每个样本按照以下规则来判断是否保留：
		  * 首先从整个训练集中选择一个样本x;
		  
		  * 评估x被选中用于训练的概率p;
		  
		  * 产生一个在[0,1]范围内的均匀随机数u;
		  
		  * 如果 u < p, 则该样本选中用于训练；
		  
		  * 对训练集中的其余样本都采取上述的选择过程
		  
		  
		  
		  
		  
		  
		  https://users.cs.fiu.edu/~chens/PDF/MIPR18_CNN.pdf
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MjAxNzIwMjE
		  #+flomo_id: MjAxNzIwMjE
		  #+created: 2022-04-01 22:25:16
		  #+updated: 2022-04-01 22:49:32
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-01/370015/78dd6bc66260359d7b3cbeb1c0b77595.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=GkA4%2FM2QRPzx%2FP%2BP2QgnzP5b1MQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-01/370015/678c1fbb591d9baec0b2cbe4eda39070.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=LcXCML7JGDbJx2QvKzxtWEGrOws%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-01/370015/64010875633b6499eabdb76fcd7d9f23.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=vDsYAOKDpjwOTJchspZtLd3xGrY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-01/370015/3d5860002050a6674318f23b545d51d1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=I3sxKpB0t6YzGKE9gicbu6OiYtE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-04-01/370015/c26027493f57baeeb2efdf01051a7cce.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=%2Fx7Anum77%2FtpAMfRvyk9kL9j71Q%3D)
		  #+isImg: true
	- [[Code]]
	  collapsed:: true
		- 测试和训练的函数可以分别写在两个子文件里，但是调用他们两者的地方最好写在同一个地方，这是因为可以训练完就直接测试，可以把训练完保存的检查点路径直接拿来进行测试，而不用手动地一个一个复制粘贴路径了。
		  
		  在训练和测试之间的接口细节有：1）训练的时候需要传递回保存最佳检查点文件的路径变量，然后测试可以直接拿此变量加载模型; 或者说训练直接传回最佳model 2）训练时经常需要改变一些参数（包括学习率初始值、加权损失的权重、weight decay的大小、加载的文件路径）、以及实验的对象（使用什么模型做实验、使用什么数据做实验），每做一个实验都需要重新手动改动代码，极易造成混乱。
	- [[速记]]
	  collapsed:: true
		- Dropout对于张量、网络分别是什么意思呢？如何理解其在训练和测试里面的区别？
	- [[Transfomer]]
	  collapsed:: true
		- 位置编码有哪几种？分别有什么作用？要怎么区分使用？是可训练的还是不可训练的？
	- [[Transfomer]][[VisionTransfomer ]]
	  collapsed:: true
		- 这里的class token为何要如此设计？到底是怎么起作用的？
	- [[速记]]
	  collapsed:: true
		- 使用torch.cuda("cuda:0")时最好把 “cuda:0”设置为全局变量，这样能随时切换显卡。
	- [[Transfomer]]
	  collapsed:: true
		- *ViT*
		  * 数据量少难以泛化，JFT-300M是有300百万张图片
		  * 为了解决不同分辨率图片的位置编码一致性，使用了2D插值法
		  
		  
		  *Transformer Enhanced CNN：*
		  利用transformer来增强CNN架构的长距离依赖，transformer强调全局性
		  * may possess a strong inductive bias towards “token uniformity” without skip connection and FFN
		  
		  * 将transformer插入到CNN主干网络或者替代某些卷积块
		  
		  * 在浅层具有高昂计算代价
		  
		  * VTs类型网络：将输入图片的语义概念解耦到不同的通道上去，然后通过编码层将这些语义密集联系起来。包含三个核心步骤：利用缩放注意力层将视觉token解耦成不同的语义集；编码层将这些视觉token的语义信息进行聚合；通过令牌-图片的跨注意力层将原始的图片像素特征空间进行重新集成。*VT-Resnet替换了resnet的最后一个卷积层*
		  
		  * BoTNet：不进行结构性替换，而是进行了概念的重定义，带有自注意力机制的连续Bottleneck块可以被看做是Bottleneck Transformer，其残差链接的实现方式不同。
		  
		  
		  *CNN Enhanced Transformer：*
		  1）引入CNN中的*局部性归纳偏置*，不一定需要显示增加CNN块，可以通过改进Transformer本身的局部性来实现
		  2）These applications can be summarized as follows: s*oft approximation, direct locality processing, direct replacements of the positional encoding, and structural combinations*
		  * DeiT: 通过使用现有的数据增强和正则化策略来提升在小数据集上的应用性
		  
		  * ConViT：将一个并行的卷积分支加到Transformer分支上
		  
		  * CeiT & LocalViT: 在FFN处使用*Depthwise Convolution*
		  
		  * CPVT & ResT：使用卷积内置的位置信息来泛化不同分辨率的输入
		  
		  * Early Conv. & CoAtNet：将ViT的不同结构块显示结合起来，而不是内部的隐形融合；在浅层堆叠卷积层比堆叠transformer层更有效；depth-wise convolution可以被直接整合进注意力块结构中去
		  
		  
		  
		  *Local Attention Enhanced Transformer*
		  通过局部自注意力机制来增强局部特征的提取能力并且同时保证没有卷积子结构
		  * Transformer-iN-Transformer (TNT)：试图聚合patch级别和像素级别的信息，分别对应TNT连续的两个不同块。
		  
		  * Twins & ViL：局部和全局分开的*Transformer结构*
		  
		  * Vision Outlooker (VOLO)：使用outlook注意力机制来关注细粒度特征
		  
		  
		  *Hierarchical Transformer*
		  * Tokens-to-Token ViT (T2T-ViT)：将多个邻居token聚合成一个token
		  
		  * Pyramid Vision Transformer (PVT)：使用了一个spatial-reduction attention (SRA) 层
		  
		  * PiT & CVT: 使用池化或者卷积来获取token的嵌入，不需要位置编码就可以泛化
		  
		  
		  *Deep Transformer*
		  深度transformer的特征代表性比较差，不同patch块的特征难以区分，现有研究进行改进：
		  * CaiT: 提出了有效的类注意力层，控制类-token在不同阶段的出现与否
		  
		  * DeepViT & Refiner： 关注于怎么把不同head的注意力特征图进行整合，以增强其多样性
		  
		  * Diverse Patch: 提出了三种基于Patch的损失函数，分别用于降低patch块之间的相似性、正则化更深层次的patch、让同一图片内的patch块更接近而不同图片的patch更不接近
		  
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTc2OTMwMTE
		  #+flomo_id: MTc2OTMwMTE
		  #+created: 2022-03-06 20:06:27
		  #+updated: 2022-03-06 21:09:52
	- [[Transfomer]] [[PoolTransformer]]
	  collapsed:: true
		- * 代码实现中所有的PatchEmbed最后都是没有经过norm层的，包括stem部分的patchembed层，原因是所有PatchEmbed后面的transformer块结构中一开始就进行了norm
		  
		  * pool（x）需要减去原始的输入x，pool（x）不改变x的大小
		  
		  * 每个stage阶段有多个连续Block，这些Block的通道数是不发生变换的，Block内部经过Pool注意力机制不改变通道数，经过MLP通道数先翻倍然后又变回来了
		  
		  * patchembed负责改变通道数和特征图的大小
		  
		  
		  中间的四个阶段一共7个组件：4个Transformer + 3个PatchEmbed
		  *block 0*
		  Sequential(
		  (0): PoolFormerBlock(
		  (norm1): GroupNorm(1, 64, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 64, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(64, 256, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(256, 64, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  (1): PoolFormerBlock(
		  (norm1): GroupNorm(1, 64, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 64, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(64, 256, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(256, 64, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  )
		  *block 1*
		  PatchEmbed(
		  (proj): Conv2d(64, 128, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
		  (norm): Identity()
		  )
		  *block 2*
		  Sequential(
		  (0): PoolFormerBlock(
		  (norm1): GroupNorm(1, 128, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 128, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(128, 512, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(512, 128, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  (1): PoolFormerBlock(
		  (norm1): GroupNorm(1, 128, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 128, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(128, 512, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(512, 128, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  )
		  *block 3*
		  PatchEmbed(
		  (proj): Conv2d(128, 320, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
		  (norm): Identity()
		  )
		  *block 4*
		  Sequential(
		  (0): PoolFormerBlock(
		  (norm1): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(320, 1280, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(1280, 320, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  (1): PoolFormerBlock(
		  (norm1): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(320, 1280, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(1280, 320, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  (2): PoolFormerBlock(
		  (norm1): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(320, 1280, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(1280, 320, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  (3): PoolFormerBlock(
		  (norm1): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(320, 1280, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(1280, 320, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  (4): PoolFormerBlock(
		  (norm1): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(320, 1280, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(1280, 320, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  (5): PoolFormerBlock(
		  (norm1): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 320, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(320, 1280, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(1280, 320, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  )
		  *block 5*
		  PatchEmbed(
		  (proj): Conv2d(320, 512, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1))
		  (norm): Identity()
		  )
		  *block 6*
		  Sequential(
		  (0): PoolFormerBlock(
		  (norm1): GroupNorm(1, 512, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 512, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(512, 2048, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(2048, 512, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  (1): PoolFormerBlock(
		  (norm1): GroupNorm(1, 512, eps=1e-05, affine=True)
		  (token_mixer): Pooling(
		  (pool): AvgPool2d(kernel_size=3, stride=1, padding=1)
		  )
		  (norm2): GroupNorm(1, 512, eps=1e-05, affine=True)
		  (mlp): Mlp(
		  (fc1): Conv2d(512, 2048, kernel_size=(1, 1), stride=(1, 1))
		  (act): GELU()
		  (fc2): Conv2d(2048, 512, kernel_size=(1, 1), stride=(1, 1))
		  (drop): Dropout(p=0.0, inplace=False)
		  )
		  (drop_path): Identity()
		  )
		  )
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTcyMzAyNzQ
		  #+flomo_id: MTcyMzAyNzQ
		  #+created: 2022-03-01 16:21:55
		  #+updated: 2022-03-01 16:39:17
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-03-01/370015/164612352170794518237FEE48A8C.jpg?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=0noAuCT26%2FNBhjhMX185%2BnO%2BF3U%3D)
		  #+isImg: true
	- [[Code]]
	  collapsed:: true
		- enumerate获取数据加载器的内容很久，可能是因为dataset类里面获取指定index位置数据的函数逻辑过于复杂
	- [[mlp]]
	  collapsed:: true
		- mlp就是线性转化层，有些时候需要加上bias, 有些时候不需要，这个可以通过代码块看出来吗还是说只是隐藏在学习的参数里面了？
		  
		  mlp层的数量以及mlp层之间通道数比例关系是怎么影响模型的结果的？
	- [[stem]]
	  collapsed:: true
		- 获取图片初始嵌入的方法手段: patch嵌入方式和其他嵌入方式有什么区别呢？我觉得最大的区别是:patch嵌入其实也是用卷积实现的，但是这种卷积的stride是等于卷积核的大小的，而普通卷积嵌入方式其实可以看作是基于可重叠的图像patch块的嵌入方式，patch嵌入可以看作是普通卷积嵌入的一种特殊形式。
	- [[mlp]] [[MLP-like model]]
	  collapsed:: true
		- 有哪些呢？感觉很奇怪，因为所有的model不都是基于mlp来的吗？这里的mlp有什么特殊的地方吗？
		  这个和transformer架构有什么相同之处吗？还是两个不同的体系？还是说两者是融合的？
	- [[模型压缩与量化]]
	  collapsed:: true
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/1d633a219295a12b1c829e2134cfdea5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=YDUB0S33gxCZVL7430QFJJsA9cQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/140a26f3751a53a63fadc56840b3e21f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=u7k7fA2CkSuZYrD50tHWA9BmCGs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/dfe39275047dc1804718a58e86c8f4d8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=byx59pMiygiX43Skf6%2BZDnY29fc%3D)
		  #+isImg: true
	- [[cautom]]
	  collapsed:: true
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/800de6d90c55b8036606967e3263fde6.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=2gzwzSQJXRj9CiYF4jFB4Ty%2FS2E%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/9db95ebd1ccbc099c33d7368c0d1e7ce.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=9RPsqAON4n%2BhyuLl9JUeU%2BpObk8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/44e27a24d40b352719ed59ebd74a924d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=tl6ga997YnHFg89%2Fim3oiSK5FJU%3D)
		  #+isImg: true
	- [[GAN]]
	  collapsed:: true
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/dec956ca352fe740b5a111425598060d.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=TmL9JYxWFlAKzMYLXdjr9m2ZHUE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/2f635a16ec1bdcff84e4062ed7ad681b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=2Iupn9da4EJ7bxRdIqBVLE4Xr%2FU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/5f19505e3de90a19fdeed801ac3e0cba.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=M10MgczmqxahBXdziqAXq8pXKe4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/d3d2db33f25923cde5e50f4e257fd776.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=tw%2B0b9VbVJY8kcZ2Qa7d2jtFpnQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/76ac567b92ea93927dbc919385b2e953.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=z8JQ00NRrquTmrXnytZExK1QTtI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/7ced9639e57a39c94ff4a525149303d5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=c0nFxa9YEO0nDNElLgRr8oAbpV0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/0a63624f76427a8a51ade75237a1d70c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=GYUBj2D4mgZRju7kb5vBdpxwkek%3D)
		  #+isImg: true
	- [[时序网络 ]]
	  collapsed:: true
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/10f594c04f8616d5b03f29fe9b17b592.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=93PbGQf6w2BoFkiyRPwNOrDeSms%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/2c4e4c09dd5853db22b5f97230ec3399.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=MGE6iwWbUKGywb0mCHjkwmVFCks%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/f9e0deee414b2c5e0f1e301af3ed3a60.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=uN9IzrLJaPmWqZGJqqJNB2Z1vis%3D)
		  #+isImg: true
	- [[非规则网络 ]]
	  collapsed:: true
		- 环形网络是对densenet的改进，可以从后面向前面训练；
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/ea6600f028e28273fe9ddfa7dc53d64a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=6MyCf%2FFAZhl308P29khx9cJjuHU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/01f15d04b91dfadd8ab88cd9bb912eab.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=PPy0BqCHdRrCeBKQxhHTDe38yy8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/411d8ebde7314106eeb2a6347acd0ed7.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=W73Ogg3IBabBULyt5XZ4vXlmaF8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/ee71c003ff19ff54182c9d8b49fe2b3a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=JNVNXcLAlegXc9D4rRd%2B18Puefw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/3276cff8d85f0bcb8e8dca059cf61588.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=4%2B2kcf%2B5QsISc%2BgUugWzkYmmAcE%3D)
		  #+isImg: true
	- [[attention]]
	  collapsed:: true
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/b238109d333d3428b5b3e9952b26cabf.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=UY6IOLRQBiyQf9%2FMiMjD4iQ47Yk%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/92d7baebb71908398f75bdbacc907c2a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=QdZ24djyTXn7Tu5sFPg2r9Ks8VI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/be79a6df1aa86a9ea2e2cd7a0f2526f0.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Yp3OgEmduj86j6AfKknDGHJ1cMU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/c93cfdeb7dc86714cdcaf4c5ad57c821.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=33l5y%2B3K%2Fp3wuRYkrmN9ANwn9mo%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/bfd178c20dccb293905abdf1f1d48936.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=dWyN0PGcbKF8R8kqaUhychuwq%2Fg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/de624fc93e0f65ce2bc5b888513cec9f.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=qFW1Kf2SZ%2FBKDvoVyqfZz5xvOjg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/32d9da21a1de654e0cbdfa001e3b3005.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Nqb4NOxY02HQEAGf2lmje%2BJ3buY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/6fa58d5fa7963fa271b6bd65207cc58c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=U1lCy6ALt6vFA7maPVrbhxwYYr4%3D)
		  #+isImg: true
	- [[多输入网络 ]]
	  collapsed:: true
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/2a29dfde80df2eda0bd2b2106ac636f5.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=wOh0jAuoHLCyDMgm3WmjuOiexos%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/f7213cb2cda1374b53f5950d6fa5bc07.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Bg7lZCteSr8OrSR6av0wsq3dmF4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/8cac248dbc302c3a3f694c928a5a4dd1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=YTegAwt7H3QwhFgACCCiCxOqgxs%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/87bf01b98a27e65ecfccefb702606d79.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=nenl09HvqpxUXpXnhWz1JklVeao%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/cae140d3e9f015c87debd7c73662ba19.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Wx0PkpC16moDhe6jbVdeMNNHJpk%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/befb4019c7a33d5ab869e037770022ca.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=qxx6MkCCdEbV3umYCqJfFgwtEKs%3D)
		  #+isImg: true
	- [[多分支网络]]
	  collapsed:: true
		- 漏掉了Inception截图
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/bbcf5f08eea8d55e159d1009e3811468.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=smLoaDIsd1jb8SGm88buKZKusx8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/c7c2c2541aa12fafdd0304e401d1fd1a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=9SAZ3KMYatTJ%2F9dgH%2BbSTo5cflM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/41165e6c517af26576400813769c0184.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=lTJEpLFKq0xpt%2F%2BSt9g0MYYn7D0%3D)
		  #+isImg: true
	- [[resnet]]  [[卷积方式]]
	  collapsed:: true
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/6efb3af1e7a88135bf3da867234334ff.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=iklJJqhbPBWGLVNoSiWmrLltglQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/de999ec24d261b76c1d7fb3b59afefd7.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=6SIDxK3fVe0fqNyLNlwgrT0Qmqw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/4ce34506cd4d7c71d656214836d2f5bc.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=UarS8LbY9Z83PpnyUY7qUCwKvW8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/544a5083ac430e2163433936fe50df16.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=RBMdwN54dNh61I2KRkXIWVfjMO8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/87c43b3d90ad3631ba7a3cd74dcb08dd.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Mdyfg09du1Ikbkk6IaMGyj6xIp4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/0c7b4187deb25cdffb6c9427202bd441.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=EyWul3uEFRk%2FN8bc8wHHe63XFf4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/ce82e2ceabd173689a4d44fc80aef319.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=zfLuAMKOWVS04LWdyaHjTxuPs%2B4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/833facd68897ee7eca2742351147f4a4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=clq2VXHJb7zHVN0uSiC7Rn8OjEE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/fd31604db59400048f6e4efe3dc21e2c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=kF5vlw5WFn2sElcKeNu9wKDrZFY%3D)
		  #+isImg: true
	- [[resnet]]
	  collapsed:: true
		- 更宽还是更深有效？
		  densenet是通道叠加，而不是直接像resnet一样相加的；
		  增加网络的宽度可能比增加网络深度更有效；
		  DualPath利用了Densenet和Resnet的优点；
		  预激活残差网络；
		  VGG删除一个层性能都会下降得很多；
		  残差网络可以看做多个网络模型的ensemble；
		  改变特征图大小的一些网络层是比较关键的；
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/aa707e3039afb03452a4e09b4bfb1eca.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=xiETo1pcdRikuQrF170ev%2B7b9bU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/f4feb393d554927107d50270660e18f8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=xQyK1Vk8yQ57QLj9PC3wFb2A5Kk%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/203a792a76354d9778e5ff19c8c968af.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=AHCeiEpQe4YetFdgMYnK%2F3ryZu0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/ee5ef37086d68247ea1494aea2cd5300.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Tdsz9JTR03GT1Fn130LVCv8jHWY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/1f9a37a9fe4cb158262a8ef330bf8778.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=RzDA%2BYy%2FVTOre7Bg%2BN2GyAYd0u4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/d21adc4030102799991d1c9588a6d9a9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Y4LS26Tq0jWWpH7NqWns%2FX5OJfM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/5eb9603fc8193c0d15b341f68290ce92.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=f7XgPENUs%2FhiGpfxZz1qgFso%2Fts%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/b7c18099e7e1f5317eddbbef024a8d15.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=ixcHb2RVp%2BtACR9xr8rtPIHiwlw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-25/370015/62c4ba54abfc151336c528ea8fd3ddf9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=TO4Tpe8%2F0MUIcOFuVnnRnc2n6Vs%3D)
		  #+isImg: true
	- [[Transfomer]] [[VisionTransfomer]]
	  collapsed:: true
		- https://www.bilibili.com/video/BV1Jh411Y7WQ/?spm_id_from=333.788
		  * MLP Head和MLP Block的结构不是完全一样的，Head中的激活函数是tanh而Block里面是GELU
		  
		  * patch向量和位置编码是直接进行相加的
		  
		  * 通常【H, W, C】需要转化成【H * W， C】
		  
		  * drop有两种方式，需要按照需要进行选择
		  
		  * CNN和Transf的混合模型效果不一定比纯VIT要好
		  
		  
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTY2MTQzNTE
		  #+flomo_id: MTY2MTQzNTE
		  #+created: 2022-02-22 15:35:53
		  #+updated: 2022-02-22 15:58:43
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-22/370015/f63dcab4387392f9a726f496e0c9775a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=l3tJ%2BFgD5RvTwUuRd55YRhQgdMc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-22/370015/8c6687cfd2103c30a3848cd166633604.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=BkK0aR0gxLc9GGCsoHoHoMNLlVY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-22/370015/ace66e9eb5c30bfb158c4094bcfaa9bb.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=pkQWYlLiKfWDv%2Fus%2F3v%2BfId%2FBiI%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-22/370015/1e270c5258f7854b356fe13c002bdea8.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Q9RBnJkYkE38R6Vxi%2FTd1WCe44c%3D)
		  #+isImg: true
	- [[Code]]
	  collapsed:: true
		- torch.permute使用完成之后要记得使用contiguous来让内存变得连续
	- [[Transfomer]][[Swin-Transformer]]
	  collapsed:: true
		- * 和ViT一样都包含有位置信息，即这里的相对位置偏置，其计算过程首先需要计算出相对位置索引(二维变成一维，用简单的二维和会造成结果重复，不能区分两个距离相似但方向不同的位置)，然后查找相对位置偏置的表格，来查找。
		  * 代码实现里面并不是一个stage作为一层结构的，实际上第0层是patch块的划分和patch向量的线性转化，后面的几层都是由transformer块结构和patch合并的下采样部分组成的。
		  * 注意里面有多个地方用到了drop
		  * patch的划分是基于原始图片来说的，patch的合并是基于特征图来说的，前者使用卷积可以实现，后者自认为也可以用卷积，但是代码中是获取不同窗口的相同位置的像素组成一个单通道的特征图，最后能得到窗口内所有位置组成的特征图，最后通道数减半，即等于窗口面积大小的一半。
		  * 一定需要padding，不管是patch块的划分，还是说窗口的划分，都不一定能整倍造成的，注意F.pad的参数顺序，且通常只是在一边进行填充。
	- [[速记]]
	  collapsed:: true
		- torch.rand是[0，1)均匀分布，而randn是正太分布
		  
		  drop的时候通常是利用随机向量把某些位置上的值全部置为0，而另外位置上的值需要放大。实际操作中，是把另外位置上的原数值除以保留概率。
		  为什么这么做？因为dropout本质上就是保留或者删除这两种操作，可以把这个看作是离散0-1的概率分布过程，其数学期望是( 1-p )* a + p * 0 =(1-p ) a，为了保证和不使用drop策略的期望一致，所以需要除以1-p。这里的a可以理解成原来特征空间中需要进行筛选的任意一个单位的值，也就是说其原本的数学数值就是a，不要把a理解为代表全体所有单位特征值的矩阵。
		  
		  tuple是可以相加和相乘的，只有一个元素的元祖同样是元祖。(5,)+(1,)*2=(5，1，1)
	- [[Transfomer]][[ConvNeXt]]
	  collapsed:: true
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/48800f2629fd66c215da8db84e769bce.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Te6LwcFVLnrVoIjJvZrFE4lT8rQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/3dbb9fd118a24136d5e2fcdaef2c7b2b.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=FFy6oCuFUhdE5cIZtw81n3xsF5k%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/5935a805b8f4cfc51b2e246abc30f25a.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=LdDjxfWG9OzuaYvnGpUg6WujQa0%3D)
		  #+isImg: true
	- [[resnet]]
	  collapsed:: true
		- 残差连接必须保证两个图片的尺寸是一样大小的，一般来说 skip connection中的卷积核大小是1*1，但是stride=2. 而其对应的瓶颈结构中一般是中间卷积核3*3处设置 stride=2来下采样。
		  
		  跳跃了解是通道数相连，还是只是同通道相加呢？
	- [[Trick]]
	  collapsed:: true
		- 训练和推理之间一般存在不同，有什么Trick呢？
		  repvgg训练使用残差，但是推理只用单分支
	- [[归一化]]
	  collapsed:: true
		- LN在网络结构实现时实际上也是全连接层吗？
		  LN是需要进行训练的，还说只用计算就可以了啊？
	- [[瓶颈结构]]
	  collapsed:: true
		- 这种结构一般来说最终的效果不都是进行了一层下采样，然后通道数变化了或者不变，但是降低了计算量。
		  
		  瓶颈结构指的是特征图的通道数是两头大中间小。
		  
		  其能提升模型效果吗？为什么能呢？
	- [[Transfomer]] [[ConvNeXt]]
	  collapsed:: true
		- 宏观设计
		  * 更改每个阶段的计算比例（也就是每个阶段所对应的层数），但同时使得更改后的FLOPS与Swin-T对齐
		  *疑惑：这里的计算复杂度对齐是怎么实现的呢？*
		  * 将网络开头的stem更改为“Patchify”。这里面论文提到Resnet传统的stem是一个7*7，步距为2的卷积层 + 最大池化层，也就是缩小了4倍；然后ViT和Swin-T都是切片化且不重叠卷积，但是ViT的核要比后者大得多
		  
		  *疑惑：这里提到的切片化仅仅是说用对应大小的卷积核提取Patch对应的一个向量，还是说这个向量也要再次进行特征转换呢？*
		  
		  借鉴ResNeXt
		  * 组卷积就是把滤波器分成不同的组。
		  ResNeXt的原则是使用尽可能多的组来拓宽宽度，增加的宽度能够弥补容量的损失。ResNeXt以一种瓶颈结构来使用组卷积。
		  
		  * 这里采用一种比较极端的方式，也就是说让组的数目等于通道数目，把这种方式的组卷积成为层次方向的卷积。
		  
		  
		  倒置瓶颈块：
		  * 每个T块结构中都有1个倒置的瓶颈结构，也就是说MLP的隐藏层维度反而是输入层维度的四倍。
		  
		  * 一些高级卷积网络中也证明了在卷积结构中使用倒置瓶颈块的好处
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/95afde8bf75f4d3a24763dc5cb2b3452.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=mrTla6m06jsnSYtgI8nWFJtHVm0%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/56125f8a7f4b350524e7d7d5c48a36a1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Z6sef6NrcKbzi8sd9zJ6JhTNktc%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/5464c9c6c363b094db4fc9fbaea90e4c.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=3qRgEBg36RaTJi%2BHIbfcb%2F5z8S8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/9b42f647fb90bd4a5f669a09c1ed6927.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=1TwJvBgvl194C7JIj1aafofFqi8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/fea8094ca3dea512923ce5c3006fbeef.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=VQcjHMnxYp%2BbcVntRw7k%2Bb%2FqvRg%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/5a57b9461fd369b2b97ae96a4a0a0564.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=CZBUkGv5ilI8YbpMBjCeDrjP7kQ%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/4a2249aef783737046bd4084a743be16.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=vSu2lw65MFkxrrnISgtDx25MfYw%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/f00f3366d64a003c19717ac023838e76.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=rELSqMdJz6Y5YUYtljwwk7hHitE%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-15/370015/7fd821b07336021df63a1e4428b3afe7.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=o9FhkQJ9%2Bw3m1xIK%2BIvU2yanTAI%3D)
		  #+isImg: true
	- [[Transfomer]] [[Swin-Transformer]]
	  collapsed:: true
		- *架构总体说明：*
		  
		  *知识点：*
		  * Transformer从语言迁移到视觉有两个难点：图片尺寸的变化大；像素点的数目与文本中的单词相比要更多
		  
		  
		  * *创新点：层级结构、偏移窗口*
		  
		  * 偏移窗口既通过把自注意力限制在不重叠的局部窗口内，从而带来计算效率的提升；也允许跨窗口之间的连接
		  
		  * 偏移窗口在实际延时方面也是有效的，因为在同一个窗口内的所有查询patch块都共享着同样一个的key set，这能够促进硬件中的内存共享。而早*期基于滑动窗口的自注意力则保持低延迟*，因为不同的查询像素点对应不同的key集合。
		  
		  * 层次结构具有对各种尺寸数据建模的灵活性和只与图片大小相关的线性计算复杂度
		  
		  * 这两种策略被证明适用于ALL-MLP架构
		  
		  
		  * *MSA计算量包含三个部分：*单头注意力计算量【从每个token（patch）的原始嵌入生成对应的查询、键值、价值三个嵌入 + 查询嵌入与键值嵌入计算权重 + 加权得到每个token的最终嵌入】+ 多头融合的计算量（对于同一个token来说就是把多个头产生的最终嵌入拼接起来，然后再用矩阵进行融合）
		  *W-MSA的计算量：*因为自注意力计算只是在每个窗口内进行，所以等于 窗口总数目 * 一个窗口内的MSA计算量。这里需要理解的是，在Swin-T的Stage1里面一个像素对应于原来图片的1个Patch， Stage2对应4个Patch，Stage3对应16个Patch，Stage4对应64个Patch，但是后面的3个阶段我们不考虑这种层次式关系带来的多尺度Patch，也就是说计算时还是把1个窗口的每个像素点视为1个Patch来计算。
		  https://blog.csdn.net/qq_37541097/article/details/121119988
		  
		  
		  * Transformer-Block包含连续的两层，前面一层用的正常配置的窗口划分，后面一层用的是偏移窗口的划分。疑惑的是为什么两层不都用偏移窗口的划分，感觉是后面一层主要是学习两个不同窗口间的信息，或者说是远距离信息；前面一层是短距离信息。可能先学短，再学远，更有意义。
		  
		  * 这里偏移窗口能计算跨窗口信息不是因为这时候自注意力机制在不同窗口之间开始进行了，而是因为这时候的一个大窗口包含了其他窗口里面的内容。而且很容易发现这种划分配置下周围四个角的窗口信息是减少了，而其他窗口是增加的。
		  
		  
		  * 相对位置偏置是注意力计算里面的一个技巧吧。需要注意它是一个矩阵，而不是单个常数，它是加在对查询和键值向量计算权重后、在权重归一化之前的，猜测可能是为了弥补这种权重计算方式的一些不足，加上后效果更好。
		  
		  * 绝对位置嵌入在这里的效果反而比不加降低。
		  
		  * 预训练中可学习的相对位置偏置可以微调中用作初始化，因为这时候窗口尺寸可能不同，所以需要进行双线性插值。
		  
		  
		  
		  *优点：*
		  *缺点：*
		  #+memo_url: https://flomoapp.com/mine/?memo_id=MTU5MzE3MjQ
		  #+flomo_id: MTU5MzE3MjQ
		  #+created: 2022-02-14 15:52:25
		  #+updated: 2022-02-14 20:59:48
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-14/370015/3fb523b5f31dd9390253e4d252ba65c2.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=uJGrqHpVMOThARbUzWiJFv%2FVBC4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-14/370015/6bfc069559991b00c37488a25aae64ad.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=ZeGASqpEXFNFrUVpUm0EXJvuOT4%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-14/370015/699f04c5e7c4ee8008bb2417b0ccf09e.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=Gv6Fm0o0Ljl%2FAopAAxhGj9sDmwM%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-14/370015/e531fa594f1b7f6a9594fd7c421baed9.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=VwBtmnEDwVvuXS7FaiSa4BdsfAU%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-14/370015/d10a36250dd2c041367c6cc4d4bf5baf.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=q5utCHAQG8Ei7O4u3Xwb3OcRWzY%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-14/370015/8e8ccf5e01f6a875510049ba7c9d64bd.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=ZOzb%2F82%2B7EBHKmNmu4hAfu9%2BIA8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-14/370015/8c060f595b4b164eb88432c51cdfcdf1.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=ChtMr65vkHb6BaU%2F1iN5eRV8Hc8%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-21/370015/5b549ff6a0fbfd5ad2822dc3624edf12.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=ErqrtycdVJmbRwXSzqDN%2FPtDVIo%3D)
		  ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-21/370015/64d9d7921f188100a48486738d1fc2fa.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=LA6eYGmfX2vGSAvQqXAl9GCODIc%3D)
		  #+isImg: true
	- [[Transfomer]] [[VisionTransfomer]] [[ViT]]
	  collapsed:: true
		- *架构简洁描述：*
		  
		  *知识点：*
		  * 位置编码是可学习的，而不是预先给定的
		  
		  * 使用1维的位置编码，而不是高级的2D-aware，因为并没有观察到替换后明显的性能增加
		  
		  
		  * CNN中的归纳偏置包括locality（二维的邻居结构）和平移不变性，但是ViT中只有MLP层是具有局部性和平移不变性的
		  
		  * ViT中的自注意力层是全局的，所以不是归纳偏置！
		  
		  * ViT中对二维邻居结构的归纳偏置利用得很稀疏，只用到了两处：将图片分成不同的Patch块；在fine-tune阶段调整不同分辨率大小图片的位置编码；
		  
		  
		  * CNN和ViT的混合架构：CNN架构提取特征图，然后在特征图上提取Patch再进行ViT。（备注：此时提取的Patch大小可以是1*1的）
		  
		  
		  * 预训练和细调注意事项：通常细调的数据集上图片的分辨率更高；预训练时需要将原本的分类头移除掉，然后增加一个线性转换层，将特征维度转换为下游任务的分类数
		  
		  
		  *创新点：*
		  * 没有像之前的工作那样把与图像具体的归纳偏好直接融入到架构当中去，仅仅是增加了提取图像Patch块的步骤
		  
		  * 利用了在大规模数据集上预训练的方法
		  
		  * 在许多图像分类数据集上能达到或者超过sota方法，但是预训练成本低
		  
		  
		  *缺点或者限制：*
		  * 不能应用于像检测和分割这样的计算机视觉任务
		  
		  * 需要继续探索自监督的预训练方法，目前自监督和大规模监督预训练方法还有较大的差距
		- ![image](https://flomo.oss-cn-shanghai.aliyuncs.com/file/2022-02-14/370015/713a132dcc597b9dcf38e7d2eb65cca4.png?OSSAccessKeyId=LTAI4G9PcaGksWVKCPrE1TVL&Expires=1677137947&Signature=bExnXJ%2FNWmHTKjoW%2BarrG1dk5Jk%3D)
		  #+isImg: true
	-
-