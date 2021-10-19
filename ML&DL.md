**机器学习就是让机器具备找一个函式的能力**。

机器学习的**任务**：Regression Classification跟Structured Learning,

> **机器画一张图 写一篇文章,这种叫机器產生有结构的东西的问题,就叫作Structured Learning**,

**Model：这个东西在机器学习里面,就是一个带有未知的Parameter的Function**,

**Label：**真实的值

**Loss：**

![截屏2021-10-15 下午9.25.35](/Users/liyun/Library/Application Support/typora-user-images/截屏2021-10-15 下午9.25.35.png)



**Error Surface：**试了不同的参数,然后计算它的Loss,画出来的这个等高线图

**learning rate**：另外一个东西会影响步伐大小,这个东西我们这边用来表示,这个叫做learning rate,叫做学习速率,这个learning rate 它是怎麼来的呢,它是你自己设定的,你自己决定这个的大小,如果设大一点,那你每次参数update就会量大,你的学习可能就比较快,如果η设小一点,那你参数的update就很慢,每次只会改变一点点参数的数值,

**hyperparameters**：这种你在做机器学习,需要自己设定的东西,叫做hyperparameters

**gradient descent**：最小化loss

**local minima**和**global minima**：

![image-20210303205623086](https://gitee.com/unclestrong/deep-learning21_note/raw/master/imgbed/image-20210303205623086.png)





machine learning training：

![image-20210303214426647](https://gitee.com/unclestrong/deep-learning21_note/raw/master/imgbed/image-20210303214426647.png)



**Domain Knowledge：**通常一个模型的修改,往往来自於你对这个问题的理解

**Linear model：**feature*weight+bias

—————————————————————————————————————————

**Model的bias**：它指的意思是说,没有办法模拟真实的状况

**Sigmoid Function**：<img src="/Users/liyun/Library/Application Support/typora-user-images/截屏2021-10-15 下午10.10.07.png" alt="截屏2021-10-15 下午10.10.07" style="zoom:50%;" />

y = c * sigmoid(b+wx1)





![截屏2021-10-15 下午10.35.26](/Users/liyun/Library/Application Support/typora-user-images/截屏2021-10-15 下午10.35.26.png)



batch：所有data，分成n个batch

epoch：把所有batch看过一遍

update：每更新一次参数叫update



ReLU：**Rectified Linear Unit**<img src="/Users/liyun/Library/Application Support/typora-user-images/截屏2021-10-15 下午10.43.38.png" alt="截屏2021-10-15 下午10.43.38" style="zoom:50%;" />



ReLU和Sigmoid是激活函数 activation function



用ReLU或者Sigmoid去逼近一个复杂的function