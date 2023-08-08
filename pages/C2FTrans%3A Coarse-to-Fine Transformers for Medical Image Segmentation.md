title:: C2FTrans: Coarse-to-Fine Transformers for Medical Image Segmentation

- ![CF2trans.pdf](../assets/CF2trans_1668998400723_0.pdf)
- 论文整体架构：
	- 跨尺度的全局transformer（CGT）：通过捕获全面的特征，来识别每个类的存在以及它们的粗糙位置
	- 边缘感知的局部transformer（BLT）：为了解决CGT中patch划分方法的四班所造成的边缘分割不准确，其用于准确得定位边缘
	- 普通的卷积操作：用于细化边缘，因为卷积的小感受野更适合捕获细节
	-