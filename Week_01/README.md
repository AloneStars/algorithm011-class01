学习笔记

1.如果辅助数据结构里面的数据不用全都存储，有些数据是可以丢弃的，例如斐波拉契数列只需要知道前两项的值，其他值都是可以丢弃的，这个时候可以用滚动数组来优化空间。

2.双指针法可以在一定的程度上将暴力的O(n^2)的复杂度，简化为O(n)的一遍遍历动作，如11.盛水最多的的容器哪一题，通过双指针向中间收敛的形式，就可以优化暴力枚举。

3.而1.两数之和这题而言，就是纯粹的空间换时间的概念，利用hash表结构将O(n)的查询复杂的优化成了O(1)的消耗，所以当我们发现无法优化我们的算法的时候，不如考虑用些高级数据结构，程序=算法+数据结构，需要搭配合理利用。

当算法都是固定套路时，一些小技巧就显得尤为重要了。