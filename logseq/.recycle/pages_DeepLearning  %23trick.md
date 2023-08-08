title:: DeepLearning  #trick

- totensor是会转化到（0,1）范围内的，所以不用自己手动除以255了
- jpg是有损图像，先读入再写入出现不一致可能是因为用的是jpg，最好用无损格式png