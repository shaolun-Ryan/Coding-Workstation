Js&Algorithm笔记
===
*****
# 什么是数据结构？
在计算机中，存储和组织数据的方式
我们要力求搞高效的组织和存储数据
# 什么是算法？
有限指令集，接受一些输入并且产生输出
在有限的步骤之后结束
**********
# 栈结构
栈是一种常见的数据结构
* 数据是一个线性结构，可以再任意位置插入和删除元素
而栈和队列就是比较常见的线性元素

## 栈结构示意图
![占位文字](../static\8.22.1.png "栈结构示意图")
* 特性
  * 要插入元素，不能直接在栈的顺序中插入，像数组一样，必须要遵循后进先出，只能在栈顶插入
  * 只能在栈的一端进行插入和删除运算，操作的一端叫做栈顶
  * LIFO（last in first out）后进先出
  * 生活中类似的：自助餐的托盘
  * 程序中的实现
    * 函数调用栈
    ![占位文字](../static\8.22.2.png "栈结构示意图")
    * 无限次的递归，就会出现栈溢出的情况
* 一个方便理解的面试题
  * ![占位文字](../static\8.22.3.png "栈结构示意图")
  * 答案：C（6不可能在5前面）

***
## 栈结构的实现
* 基于数组
* 基于链表

构建栈的代码：见 栈的封装.js

# 队列
另外一种受限的线性结构
符合先进先出的原理
在后端添加元素，在前段删除元素
![占位文字](../static\8.23.1.png "栈结构示意图")
生活场景：电影院排队进场
开发：打印队列，线程队列
* 队列的实现
  * 基于数组实现
  * 基于链表实现

## 优先级队列
在插入一个元素时会考虑数据的优先级
在进行比较后的出数据在队列中的正确位置
插入优先级比他还小的元素前面
其他处理方式，和普通队列基本一样

* 应用场景
  * 头等舱和商务舱的优先级
  * 老人和孕妇在公共车上    
  * 看病时，普通和急诊

# 链表
数组的缺点：要申请一端连续的内存空间，并且通常大小是固定的，超出时一般需要扩容
在数组开头或者中间插入数据时，要进行大量的元素的位移

* 链表的优势
  * 链表在内存中不必是连续的空间
  * 链表的每一个元素由元素本身的节点和指向下一个元素的引用（优势成为指针或者连接）组成
  * 方便实现动态管理（due to 1）
  * 链表不必在创建时就确定大小，可以无限延伸下去
  * 链表在插入和删除数据时，时间复杂度可以达到O(1)，效率非常高
* 链表的缺点
  * 链表访问一个元素时，都需要从头开始访问
  * 无法通过下标直接访问元素，需要从头一个一个访问，直接找到对应的元素
* 链表的结构，十分像一个火车