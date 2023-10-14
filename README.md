# Real Time Quant Interview - Sample

## 指南 Q & A （必读）
这里会为大家介绍这本资料的意义和最佳使用方法。

-Q: 这本资料的意义是什么？

A： 主要是为想从事quant 方面工作的同学提供一个刷题的思路和大纲

Q： 这本资料的受众群体是谁？

A： 受众群体主要是想从事quant 方面工作的本科，研究生，博士以及junior quant们。这本资料的主要针对卖方投行定价quant，hedge fund quant research/trading， 以及market maker trading 及类似的岗位

Q: 这本资料和市面上其他quant 题库例如红皮书绿皮书有什么区别？

A： 这个更多是一个大纲而不是一个题库。 以红绿皮书为代表的quant 题库/书在市面上以及流传很久了，以至于现在任何人面试之前都要刷这几本书。其次这些题库基本都是7，8年前写出来的， 很多题已经过时。 很多同学使用红绿皮书的都反应没有一个clear direction。 这些题库往往有上百道题，对于面试经验较少的同学来说很难去找到侧重点。

使用红绿皮书是希望通过大量刷题从而达到押题的目的， 可以理解为：刷大量的题->面试正好碰到刷过的题或者类似的题型。 这种方法非常耗时并且现在已经不太现实因为现在quant面试的广度越来越大，而且现在很多公司也知道大家都在刷这几本书所以在面试中也会可以去改变题型。庆幸的是不管题型怎么改它们背后的知识点是不变的。

因此我写这本资料的初衷是通过分析这几年（2018年之后）的买卖方面试真题去找所需要的重要知识点以及解题/出题思路。这可以理解为 找到这几年真题背后的知识点/思路 -> 面试中在所掌握的知识点中去寻找最适用的知识点完成答题。这种显然比使用红绿皮书节省时间（以及脑细胞）。

其次，这本资料最大的优势在于所有的题都是近几年买卖方的面试真题，我会附上公司，年份及job/programme title。

Q： 这本资料能取代红绿皮书吗？

A： 不能， 这本资料的最大作用是用实战经验去提供刷题思路和方向，所以每个topic的重点是背后所需要的知识点。大家可以依靠我总结的知识点再去这些题库里找额外相似的题去刷，从而达到巩固知识点的效果。

Q： 这本资料的最佳使用方法是什么？

A： 最佳使用方法是先读本资料的某个topic然后去以下（或其他）题库寻找类似的题去刷：
-

## Probability & Statistics
统计方面的题不管是在卖方还是买方都是很重要的一个环节。在投行Quant面试里统计/概率面试题相对来讲会简单一些。投行的Quant比较注重于数理和编程能力的全面性，因此问的问题也广度大于深度。对于hedge fund来讲概率题的难度方差比较大。而对market maker （例如optiver）来讲概率题+心算能力会是面试的重要考点。因此对于刷概率题的侧重比则需要看申请的是哪种类型的公司。  

这个章节包含了投行，fund，以及market maker这三四年的面试真题并且分析所需要的知识点和出题逻辑等。刷题的数量不等于刷题的效率，从一道真实面试题我们可以分析总结有哪些知识点我们需要背下来，以及不同知识点的重要性和题型的规律。以概率题为例子，近几年的面试题通常为两种， 一种是面试官会形容一个scenario然后要求candidate算某个outcome的probability， 而另外一种是算一种或多种outcome的expected value/time 等等。能够通过分析真实面试题而找出这些出题规律的效率会远远高于从一些题库中大量但没有重点的刷很多可能面试里永远不会出现的题型。  

我会在这个章节给出这几年收集到的概率方面的面试题，也会给出对应的公司和internship/全职工作岗位的名字， 面试流程方面的信息如果有我也会列出。这里给出题的顺序是随机的，并不是以难度的顺序呈现.

---

### 例题1  

Credit Suisse Quant Summer Institue 2022 & 2023 

问: You flip a coin 100 times and observe 99 heads, the probability of a biased coin is 0.95, what is the probability the coin was biased?

答：直接用Bayes rule 算 $P(biased coin|99head) = P(99head|biased coin) P(biased coin) / P(99 head)$

解析：这道题是绿皮书 A Practical guide to quant interview里面的原题， 并且在credit suisse面试里两年出现了两次完全一样的。Credit Suisse quant summer institute是第一轮电话面试+第二轮assessment centre。

第一轮大概一个小时左右并且包含了大概四道数学题。一般是一道统计题+两道stochasic+一道随机出的算法/口述编程题。第一轮有很大概率会从绿皮书里直接抄题。

第二轮AC是四个面试，每个面试一个面试官。形式基本和第一轮差不多，一般每个面试3道题左右，但是topic非常广，覆盖了brain teaser，概率题，随机微积分，和现场编程。编程主要以dynamic progamming为主，这个会在后面系统总结。

对于Credit suisse的quant summer institute的概率面试题 个人给出的意见是刷绿皮书里面74页的All girl world， Unfair coin， 和80页的Coin toss game。

Coin toss game也是原题在2023面试里出现过。

---

### 例题2

Jane Street Quant Trading Internship 2023 

问: You flip a fair coin a large number of times, what is the probability of getting an even number of heads?

答：0.5

解析： 这道题在market maker的面试里算是非常简单的，但是他的核心知识点是symmetry， 也就是说很多时候一个很复杂的情况我们可以用symmetry去把它变成一个简单的情况。比如说我们 flip odd number of times （7） 那么我们可以得到0，2，4，6
或者1，3，5，7个head。因为 $P(1)+P(3)+P(5)+P(7) = P(0) + P(2) + P(4) + P(6)$ 那么 $P(even)=P(odd)=0.5$ . 这个等式成立因为$P(0)$和$P(7)$ 其实是一回事，如果我们flip 0个head我们其实得到了7个tail，然后 $P(7 tail)=P(7 head)$

如果我们 flip even number of times （8），因为每次的flip是independent那么我们可以把这个拆成flip 前7此和最后一次（第八次）， 那么因为coin 是fair的所以得到even或者odd的概率还是同样的（0.5）。

如此可见用symmetry可以把很多复杂的问题简单化。很多market maker问的概率题听着很复杂但其实可以用symmetry换一种方法理解并解答。Symmetry在绿皮书里的题个人推荐61页的Coin toss game。很多时候类似的面试题会比较两个事物或者人然后其中一个比另外一个多出一些东西。那我们首先要做的是问如果两个人/物是完全相等的会不会影响概率，如果不影响那么我们可以只考虑多出来的那一部分，比如一个人比另外一个人多了n个coin其他的都一样那么我们只需要考虑多出来的n个coin的event的概率。

---

### 例题5

JP Morgan Securities Services Quant Research 全职 2022 

问: noodle loop

答：$eigenvalue = n$

---

### 例题4

Capula Investment Management Quant Trading Internship 2021 

问: gamblers ruin

答：$eigenvalue = n$

---

### 例题2

DRW Quant Researcher Internship 2023 

问: You have a fair coin and you toss 8 times and compute the product, what is the expected value of this product? what is the expected and median number of heads?

答：$eigenvalue = n$

---

### 例题2

Man Group Machine Learning Internship 2023 

问: What is the probability of winning a tennis game in two rounds given the probability of winning each round is P? 

答：$eigenvalue = n$

---

### 例题3

JP Morgan Quantitative Analytics Associate Programme – PhD Off-Cycle Internship 2022

问: what is the distribution of the sum of two standard uniform distributions and what is the probability of this random variable being less than 0?

答：$eigenvalue = n$

---

### 例题3

Akuna Capital Graduate Quant Researcher 2023 

问: What is the eigenvalue of an $n \times n$ matrix with all 1s

答：$eigenvalue = n$



解析：


