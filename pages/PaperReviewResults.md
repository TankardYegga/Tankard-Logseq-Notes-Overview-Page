- ” achieve high accuracy ultrasound image classification. The 
  results show that the contour of the lesion recognition results obtained 
  by the proposed algorithm is the most complete, and the other regions 
  can maximize the retention of the texture features of the original image, 
  the accuracy value is 85.3, the sensitivity value is 85.6. The proposed 
  algorithm can improve the classification accuracy and enhance the 
  accuracy of diagnosis, and has application value in the field of breast 
  ultrasound diagnosis."
-
- 多处语句的句意重复甚至冗余，不够简练:
	- "improve the classification accuracy and enhance the accuracy of diagnosis"这里的诊断准确率和分类准确率应该是一个概念
	- Rasa Ee H, Rivaz H 的"AI-based classification algorithm"和后面的" improved the convolutional neural network (CNN) using GRAD-CAM and other techniques"属于等价表述，可以进行合并
- 多处语句表达形式单一：
	- introduction中两次使用"At present"
- 多处语句过长：
	- 多处使用and连接三个或者四个动词短句，比如"it can effectively avoid the influence of external factors, improve the sensitivity of breast tumors and other types of lesions, and reduce the probability of misdiagnosis and missed diagnoses"
	- 文献总结部分的用句过长，比如对Rasa Ee H, Rivaz H的文献进行缺点分析的语句"however, the method has low classification accuracy and poor practical effect"完全可以单独成句
- 多处语句表达比较中式：
	- 比如摘要中的"high accuracy ultrasound image classification"，建议改成"high accuracy in the classification of  ultrasound images"
- 字符空格存在不一致：
	- main contibution中的"(1)By"、"(3)Several"中括号和后面的单词之间都没有空格，但是"(2) Image"中却出现了空格
	- "3.4.2Realization of proposed algorithm"中序号和标题之间应该存在空格
- 多处语句的内容杂糅，导致难以理解
	- 贡献3）将评价指标和实验目的混在一起，最好分开表述；
	- "The results show that the contour of the lesion recognition results obtained by the proposed algorithm is the most complete, and the other regions can maximize the retention of the texture features of the original image, the accuracy value is 85.3, the sensitivity value is 85.6." 中最好将定性和定量结果分开描述；
	- 文献综述每篇文献的内容太多，读者容易找不到重点
	- ”Therefore, this paper proposes a quantitative feature classification algorithm for breast ultrasound images based on improved naive Bayes, which further improves the feature classification effect by improved naive Bayes, and provides more basis for the classification research of breast ultrasound images"中模型的整体意义、提升贝叶斯方法的单独作用，算法对整个业务的意义这三者混在一起
	- "this study applied the improved Navie Bayesian algorithm to feature classification and applied it to quantitative feature classification of breast ultrasound imaging" 中有重复内容，可以改成"this study applied the improved Navie Bayesian algorithm to quantitative feature classification of breast ultrasound imaging"
- 存在语法错误
	- "To obtain more accurate and efficient image feature classification results."中的动词不定义不能单独成句
	- "As shown in Figure2."也不能单独成句
- 方法部分
	- 存在描述不一致的地方
		- "3.3. Quantitative Analysis of Feature Parameters"中将roundness记作S，可是又在"The closer the resulting value of circularity"中将S称作circularity
		- " n represents the number of attributes of the data sample"与"B = {b1, b2, ..., bn}"相矛盾，后者中的n倾向于被理解为样本的个数
	- 存在描述不清晰的地方
		- 没有解释公式6中求和的含义，这里求和公式的上标S是公式4中的S吗
		- w1，w2, w3, w4这四个权重到底怎么计算的并没有阐明
		- 提升贝叶斯的两个分析技术是自己提出来的吗，为何不在contribution里面指出其创新点
	- 你这里的方法并非是深度学习模型，而是传统的机器学习模型，为何需要使用pytorch来实现？
- This is an interesting study of breast ultrasound image classification. The paper is generally well written and structured, and I have a basic understanding of your proposed methodology. First, in addition to the qualitative features of the histogram, you also extract the texture features from the grayscale concurrent matrix; then,  shape feature analysis is conducted and then quantified to address the quantization parameters; finally, improved Naïve Bayes which refine and combine the Naïve Bayes and decision tree computing is adopted to classify the features. However, in my opinion, 
  the paper has some shortcomings in regard to method and text, which is detailed described in the attachment. Given these shortcomings the manuscript requires major revisions.
-
- A. About the method section:
- (1) There are inconsistencies in the description:
	- 1) in "3.3. Quantitative Analysis of Feature Parameters", roundness is denoted as S, but in "The closer the resulting value of circularity", S is referred to as circularity;
	- 2) "n represents the number of attributes of the data sample" contradicts "B = {b1, b2, ..., bn}", where n tends to be understood as the number of samples in the later description.
- (2) There are places where the description is not clear:
	- 1) What is the meaning of the summation in Equation 6? Is the upper limit of the summation of Equation 6 the S in Equation 4?
	- 2) How are the four weights w1, w2, w3, and w4 calculated?
	- 3) Are the two analysis techniques for improved Bayesian proposed by you? Why not point out the innovation points in the contribution?
- (3) Your method here is not a deep learning model, but a traditional machine learning model. Why do you need to use PyTorch to implement it?
-
- B. About the text
- (1) Some sentences are written in a style of Chinese language
	- For example, "high accuracy ultrasound image classification" in the abstract is recommended to be changed to "high accuracy in the classification of ultrasound images"
- (2) There is a syntax error
	- "To obtain more accurate and efficient image feature classification results." cannot stand alone as a sentence;
	- "As shown in Figure2." also cannot stand alone as a sentence.
- (3) The meaning of some sentences is repeated or even redundant, which is not concise enough
	- In "improve the classification accuracy and enhance the accuracy of diagnosis",  the diagnosis accuracy and classification accuracy here seem to be the same concept;
	- The sentence "this study applied the improved Navie Bayesian algorithm to feature classification and applied it to quantitative feature classification of breast ultrasound imaging" contains repetition and can be changed to "this study applied the improved Navie Bayesian algorithm to quantitative feature classification of breast ultrasound imaging".
- (4) Several sentences are too long
	- Use "and" in many places to connect three or four verb phrases, such as "it can effectively avoid the influence of external factors, improve the sensitivity of breast tumors and other types of lesions, and reduce the probability of misdiagnosis and missed diagnoses".
- (5) The content of the sentence is mixed, making it difficult to understand
	- Contribution 3) mix the evaluation index and the experimental purpose together, preferably separately;
	- In the sentence "The results show that the contour of the lesion recognition results obtained by the proposed algorithm is the most complete, and the other regions can maximize the retention of the texture features of the original image, the accuracy value is 85.3, the sensitivity value is 85.6.", it is better to separate qualitative and quantitative results;
	- In the literature review, there are too many contents of each literature, and it is difficult for readers to find the key points;
	-
-
-