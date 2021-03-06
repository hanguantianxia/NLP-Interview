# NLP面试准备



### 1. 项目 + 竞赛 

（1）数学建模竞赛

题目的背景是：对众包任务定价问题，研究如何给制定一个定价策略，给一个众包任务合适的价格，使得该众包任务可以以一个最可能完成的最低价格；

给的数据有：

- 任务的数据：位置(经度和纬度) + 任务的定价 + 该任务是否完成
- 用户的数据：活跃用户的位置  + 用户的任务配额 + 用户的信誉值

我们当时的思路是：首先训练一个模型进行任务能否完成预测，在这个模型训练测试集下表现较好的情况下，通过搜索的方法获取最好输入价格。

一些具体的细节：如果仅输入任务的位置和定价来判断任务是否完成是不够的，

- 忽略了任务周边的用户情况，一个任务如果处于用户多的地方，它被完成的可能性就大，所以我们引入了**邻近会员数**和**邻近会员的信誉值**两个特征来表征任务周边的用户情况
- 忽略了周围的任务情况，如果一个任务的周围任务多，说明用户可以用较小的路程连续做任务，效率提升，可以更加吸引用户参与任务，因此我们引入了**邻近任务数**和**邻近任务标价均值**两个特征来表示任务特征。

- 模型选择的是LR回归

### 2. 基础知识



#### 2.1 机器学习知识



#### 2.2 NLP知识

##### (1) Transformers与Bert系列

- BERT
- Roberta
- Albert
- Transformer XL 与 XLNET





