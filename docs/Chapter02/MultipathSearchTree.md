# 多路查找树(N叉树)

树家族是为了实现方便快捷的查找而存在的。
树的高度是命中查找的一个不可抗拒的时间下限。
在一定的数据条件下，树的高度和宽度是互相制约的。
（就像一定面积下，矩形的长和宽是互相制约的）而树家族中最简单的二叉树，尽管易于实现，却不能有实际的价值。
其最最令人发指的是二叉树的高度太高。
n叉树的提出和实现解决了二叉树的不足，

典型的多路查找树有：2-3-4树、红黑树和B树。

#### 定义

二叉树中每个结点有一个数据项,最多有两个子节点,如果允许树的每个节点可以有两个以上的子节点,
那么这个树就称为n阶的多叉树，或者称为n叉树。

#### 性质

* 每个节点有m个子节点和m-1个键值。
* 每个节点中的键值按升序排列。
* 前i个子节点中的键值都小于第i个键值。
* 后m-1个子节点中的键值都大于第i个键值。
