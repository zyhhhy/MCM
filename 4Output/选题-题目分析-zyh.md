# A

## 背景

藻类对于降解速度有很大的影响，尤其要关注两种特点：藻类的生长速度和对于潮湿的容忍度

一些问题：

1. 不同的藻类是如何处理并降解地面垃圾在不同的环境里？
2. 在不同的环境下，随着时间的变化降解是如何被影响的？
3. 环境改变是如何影响降解？
4. 藻类的竞争是如何影响降解？

## 要求

1. 在不同藻类存在的情况下，地面垃圾和纤维素是如何被降解的？
2. 考虑不同藻类之间交互的影响
3. 描述短期和长期藻类交互的影响
4. 分析不同种类的优势和劣势，也包括不同环境（干旱、半干旱。。）
5. 藻类种群的多样性是如何影响整个系统的讲解效率的

## 分析

主要是看参考资料，要分析的对象是不同藻类（种类、竞争、适应性、讲解能力），其次才是藻类对于环境讲解的影响



# B

## 背景

澳大利亚森林火灾 -> 选择无人机类型，判断火灾情况以及如何援救

手环+SSA无人机

RR无人机

## 要求

1. 选定SSA无人机和RR无人机的组合。尽量经济并且能够随着火情变化实时调整
2. 在接下来的十年里，模型是如何适应极端火情的
3. 根据火情决定无人机出警的位置
4. 一两页的Request

## 分析

看起来不难，但是没什么经验，尤其是不同类别无人机的选择（好像以前也有类似的题目，向一个小岛上运输救援物资之类的）

没有数据，需要自己去找



# C

## 背景

VM大黄蜂被发现

VM捕食欧洲蜜蜂和一些其他害虫

VM的生长周期和许多其他黄蜂类似，在春天受精的蜂后会在秋天离巢并且在大约30km左右建立新的巢穴

问题：

1. 我们如何利用公众提供上来的数据
2. 我们如何在这些报告中找到最有效的报告用来在有限资源的情况下进行额外调查

## 要求

1. 讨论VM随时间传播是否可被预测并且有多少精确度
2. 根据数据集和图片预测**错误分类**的可能性
3. 使用模型来讨论分类结果如何在报告中找到正确的报告
4. 当新报告到来时，模型如何改变？多久改变会发生一次？
5. 使用模型，VM灭绝的证据将会是什么
6. 两页备忘录

## 分析

这是一个**时空**数据处理的模型

还是比较对胃口的，从第二题开始就是图片处理，原则上我们可以给出一个<VM，其他黄蜂>的神经网络，但是这只是图片信息，此外我们还需要提取的是<位置信息，comment>

在位置信息里面涉及到经纬度转换为平面距离

除此以外我觉得可以挖掘的点还是有的，比如

1. VM蜂后会在30km处建造新窝，那如果没有出现就代表那一片的VM死亡
2. 根据时间序列判断哪些地区已死亡，同样送到LSTM？？？（时序数据怎么使用？）

仅仅从数据挖掘的角度我能想到的有：

1. 不同地区出现的情况->地图、散点图
2. 不同时间出现的情况->地图、热力图
3. comment分析？
   1. Notes提取关键词推理习性（颜色、聚集地、出没时间）（但是positive的数量太少14，加上unverified能达到2000+）
   2. Lab Comments用于提取其他黄蜂的种类并打标
4. 根据不同类别黄蜂出现的情况->地图

