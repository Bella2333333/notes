**分清overfitting还是optimization没做好**：56层的network,如果你optimization成功的话,它应该要比20层的network,可以得到更低的loss,但结果在训练集上面没有,这个不是overfitting,这个也不是model bias,因為56层network弹性是够的,这个问题是你的**optimization不给力,optimization做得不够好**

![截屏2021-10-19 上午11.20.27](/Users/liyun/Desktop/截屏2021-10-19 上午11.20.27.png)



如何减少overfitting：1⃣️增加training data=>data augmentation	2⃣️让model弹性不要太大，给它加一些限制



**cross validation**：90%的资料放在Training Set裡面,有10%的资料,会被拿来做Validation Set

**N-fold Cross Validation**：把validation分得更好。N-fold Cross Validation就是你先**把你的训练集切成N等份**,在这个例子裡面我们切成三等份,切完以后,你拿其中**一份当作Validation Set**,**另外两份当Training Set**,然后这件事情你要**重复三次**

![截屏2021-10-19 上午11.48.54](/Users/liyun/Library/Application Support/typora-user-images/截屏2021-10-19 上午11.48.54.png)



**miss match**：训练资料和测试资料的分布不一样，那训练资料再怎么增加也没有什么用

**critical point**：local minima or saddle point 微分为零

<img src="/Users/liyun/Desktop/截屏2021-10-19 下午3.27.04.png" alt="截屏2021-10-19 下午3.27.04" style="zoom:50%;" />



如何区别local minima、local maxima、saddle point：

<img src="/Users/liyun/Desktop/截屏2021-10-19 下午3.42.10.png" alt="截屏2021-10-19 下午3.42.10" style="zoom:50%;" />

矩阵特征值是否全正、全负、有正有负

经验上看，saddle point比local minimal的情况多



small batch vs large batch：

<img src="/Users/liyun/Desktop/截屏2021-10-19 下午4.07.49.png" alt="截屏2021-10-19 下午4.07.49" style="zoom:50%;" />



vanilla gradient descent：单纯按gradient反方向去update参数

gradient descent+momentum：新的update的方向由gradient和前一步update的方向共同决定

<img src="/Users/liyun/Library/Application Support/typora-user-images/截屏2021-10-19 下午4.20.49.png" alt="截屏2021-10-19 下午4.20.49" style="zoom:50%;" />



- Smaller batch size and momentum help escape critical points. 



最常用的optimization方法：Adam：RMSProp+Momentum

warm up：让learning rate,要先变大后变小