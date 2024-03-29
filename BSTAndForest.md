# 二叉树

## 树的定义

    树(tree)是n (n ≥ 0)个结点的有限集。当n = 0时称为空树（递归基始）

## 树的类型

    有向树
    有序树
    无序树

## 基本术语

    结点
    度 ：一个结点拥有的子树数目(分支数)；

    树的度 ： 一棵树上所有结点度的最大值；

    叶子 / 分支结点 ： 度是否为 0 来判断

    孩子结点 ：结点的子树的根称为该结点的孩子结点

    兄弟 / 堂兄弟 / 祖先 / 子孙 ：...

    结点的层次 ：从根结点到该结点所经过的路径长度加 1

    树的深度 ：树中叶子结点具有的最大层次数

    森林 : m(m ≥0)棵互不相交的树的集合。对树中每个结点而言，其子树的集合即为森林

## 二叉树

定义：二叉树是 n (n≥0) 个结点的有限集合，这个集合或是空集，或是由一个根结点以及两棵*互不相交的、被称为根的左子树和右子树*所组成；左子树和右子树分别又是一棵二叉树

<font color= red>注意：序不能任意颠倒，互不相交</font>

### 二叉树的性质

1. 在二叉树的第 i 层上至多有 $ 2^i-1 $ 个结点。(i≥1)
   二叉树是从第一层开始计数的，没有第零层
2. 深度为 k 的二叉树上至多含 $ 2^k-1 $ 个结点（k≥1）。
3. 对任何一棵二叉树，若它含有 n0 个叶子结点、n2 个度为 2 的结点，则必存在关系式：
   $n_0 = n_2+1$。
   （可以从分支的角度入手分析）

### 特殊的二叉树

1. _满二叉树_
   满二叉树：指的是深度为 k 且含有 $2^k-1$ 个结点的二叉树。
   特点: 每一层上的结点数都是<font color = red>最大结点数。</font>

2. _完全二叉树_
   完全二叉树：树中所含的 n 个结点和满二叉树中编号为 1 至 n 的结点一一对应。
   特点 1: 叶子结点只可能在层次最大的两层上出现；
   特点 2: 对任意结点，若其右分支下的子孙的最大层次为 L，则其左分支下的子孙的最大层次必为 L 或 L+1。
   性质 ：具有 n 个结点的完全二叉树的深度为
   $\log_2{n}  +1$ 。
   性质 ：通过角标来判断二叉树的根与左孩子 / 右孩子

## 存储

1. 顺序存储
2. 链式存储
   1. 二叉链表 ；带兄弟结点指针
   2. 三叉链表
   3. 双亲链表 ：存双亲
   4. 线索链表

## 三种遍历

    递归描述
    非递归描述 ： 简而言之就是对于每个结点都要做一遍搜索以及处理

树的计算题小题比较多：
需要注意的是：树的高度和深度是同一个概念，并且都等于节点数量 $\log_2{n}$ + 1;

## 线索二叉树

![Alt text](image-2.png)
tag = 0 为孩子
tag = 1 为前驱/后继
二叉树中序序列中的第一个结点的 lchild 域指针和最后一个结点 rchild 域的指针均指向头结点。

## 森林

用二叉链表把森林表示出来并转化为二叉树
遍历时 ：先序 = 先序，后序 = 中序

## 霍夫曼树

比较简单，做题时常和计算联系，细心一点就好
注意 ： 有 n 个叶子结点的霍夫曼树节点数为 $ 2n - 1 $
