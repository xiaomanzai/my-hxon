
## 区别

 ----|数据结构| 是否重复的元素|是否有序
------| -----  |----- | -----
Treeset | 二叉搜索树  | 不允许|否
 PriorityQueue| 堆|允许|是


## treeset
![image.png](https://s2.loli.net/2023/10/18/J1wz5njAkgsbNY3.png)

treeset 底层其实是调用 treemap，等于放到 treemap 中的 key 部分

而且是无序的，进出时间不确定
但是因为是二叉搜索树，因此在数值上是有序的


可以通过重写 Comparable 或者 comparator 来更改排序
ps：
1. 当比较规则不会发生改变时（比较规则只有1个的时候），可实现 Comparable 接口
2. 如果比较规则有多个，并且需要多个比较规则之间频繁切换，可使用 Comparator 接口


#### 二叉搜索树

**性质**
- 若左子树不为空，则左子树上所有结点的值均小于它的根结点的值
- 若右子树不为空，则右子树上所有结点的值均大于它的根结点的值
- 左、右子树也分别为二叉排序树
小放左，大放又
序列 [7, 3, 10, 12, 5, 1, 9] 以二叉排序树存储的结构如图：

![image.png](https://s2.loli.net/2023/10/18/5Gd419oEDxyi8wH.png)


## PriorityQueue

优先级队列： 队列是先进先出，而优先级队列就是把优先级最高的先出。

![image.png](https://s2.loli.net/2023/10/18/F3cbTYMNpVUGgPi.png)
![image.png](https://s2.loli.net/2023/10/18/ae6bGoVZgrLEp1w.png)
![image.png](https://s2.loli.net/2023/10/18/QR2xh5iyXVEFqbk.png)
## 堆

	
**含义**： 如果有一个关键码的集合 K = {k0 ， k1 ， k2 ， … ， kn-1} ，把它的所有元素按完全二叉树的顺序存储方式存储在一个一维数组中并满足： Ki <= K2i+1 且 Ki<= K2i+2 (Ki >= K2i+1 且 Ki >= K2i+2) i = 0 ， 1 ， 2… ，则称为小堆 ( 或大堆) 。将根节点最大的堆叫做最大堆或大根堆，根节点最小的堆叫做最小堆或小根堆。

 **性质**：堆中某个节点的值总是不大于或不小于其父节点的值；
			堆总是一棵完全二叉树。


![fa2cbc4f683c46758ab4ed2b98bd1f07.png](https://s2.loli.net/2023/10/18/oUgtSRYB2d34Fxu.png)


堆的构建是冒泡构建
 1. 从后遍历每一个树，如果比父节点小（或者大），就和父亲交换，因为是数组储存，因此是 o (n)
2. 调整（o（$log_2(n)$））
    ![heap.png](https://s2.loli.net/2023/10/18/3yBauxApb61sCnE.png)




