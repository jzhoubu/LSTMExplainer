
# DeepLIFT

## 1.Introduction
- List of contribution:
    + calculate importance from difference-from-reference
    + reveal dependencies (?)

## 2.Previous Work
> 介绍了别的一些工作，但里面没提到跟DeepLIFT的关系。
> 到目前为止没看到DeepLIFT是怎么计算的


## 3. The DeepLIFT Method
### 3.1 DeepLIFT Philosophy
主要介绍Eq.1 **summation-to-delta**。后半段阐述了`C△x△t`适用的special case。

### 3.2 Multipliers and the Chain Rule
定义了Multipliers及证明了它的链式推导
**疑惑**：这里已经开始做性质上的证明了，但没感觉到作者深入阐述DeepLift的实质上的东西。作者前面定义了C，以及一些假设的性质，但没有讲C是怎么计算的。只在intro那里讲过difference-from-reference的计算只需要一次反传，所以猜测difference-from-reference的计算其实就是output对于x的导数？ 

### 3.3 Defining the reference
reference input: user choose
reference output: propogate reference input
跟另外几个算法比较，强调reference的作用--需要考虑input在一个范围内波动时对output的影响

### 3.4 3.5 
- 定义C的正负、scale的方法
- 这里讲了**Rules for assigning contribution scores**
- 后面还有个比较重要的细节在3.5.2最后面，提到了DeepLIFT和Shapley values的connection，在“An unexpected unity among methods for interpreting model predictions”这篇论文里，也是UW的。

后面的篇幅主要是针对一些misleading case提出算法上的improvement，以及怎么choose target layer，我这边直接跳过了。


## 疑惑
- 我最大的**疑惑**是关于C的定义，它出现在3.5（？），也就是说文章的结构是先花了较大篇幅讲C的一些性质，然后在3.5点了一下怎么计算C，我觉得这是不合逻辑的。所以我怀疑是自己看的时候miss了很重要的一个部分和细节，想找个人交叉确认一下。

- 关于3.4，我理解的`△x_{i}+`等价于`△x_{i} if △x_{i}>0`。所以3.4的第一个加法公式，有点故弄玄虚的感觉，想确认下我理解的有没有错。

- 对整篇文章，我觉得自己的状态是“看过了”，但没“看懂”。
    + [1] 对于部分片段，比如3.1,3.2，我反复看了很多次，却总觉得缺了一点information，但在上下文却找不到线索。
    + [2] 对于另一些片段，比如3.5.3，我认为不读也不妨碍理解，或者说我认为读了不能帮助我解决目前的疑惑，所以是glance一下就过了的。
    + 作为reading skill来讲，我想了解下我这样读paper是不是一种坏习惯？ 我一直担心[2]导致[1]这种现象，然后我把3.4，3.5读了一遍，还是觉得这里面没有我想找的missing pixel。而缺了这块missing pixel，感觉这些信息连不到在一起。

