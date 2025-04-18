# 为什么 MongoDB 索引选择B-树，而 Mysql 选择B+树

### B-树和B+树的区别

1. B+树查询时间复杂度固定是logn，B-树查询复杂度最好是 O(1)。
2. B+树相邻接点的指针可以大大增加区间访问性，可使用在范围查询等，而B-树每个节点 key 和 data 在一起，则无法区间查找。
3. B+树更适合外部存储，也就是磁盘存储。由于内节点无 data 域，每个节点能索引的范围更大更精确
4. 注意这个区别相当重要，是基于（1）（2）（3）的，B-树每个节点即保存数据又保存索引，所以磁盘IO的次数很少，B+树只有叶子节点保存，磁盘IO多，但是区间访问比较好。

### 原因解释

想要解释原因，我们还必须要了解一下MongoDB和Mysql的基本概念。

MongoDB

* MongoDB: 是文档型的数据库，是一种 nosql，它使用类 Json 格式保存数据。
比如之前我们的表可能有用户表、订单表、购物篮表等等，还要建立他们之间的外键关联关系。
但是类Json就不一样了。

![](../image/c2/b&bplus-1.png)

我们可以看到这种形式更简单，通俗易懂。那为什么 MongoDB 使用B-树呢？

MongoDB使用B-树，所有节点都有Data域，只要找到指定索引就可以进行访问，无疑单次查询平均快于Mysql。

* Mysql： 作为一个关系型数据库，数据的关联性是非常强的，
区间访问是常见的一种情况，B+树由于数据全部存储在叶子节点，
并且通过指针串在一起，这样就很容易的进行区间遍历甚至全部遍历。

这俩区别的核心如果你能看懂B-树和B+树的区别就很容易理解。
