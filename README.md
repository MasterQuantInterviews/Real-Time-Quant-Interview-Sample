# Sample

## 指南

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
或者1，3，5，7个head。因为 $P(1)+P(3)+P(5)+P(7) = P(0) + P(2) + P(4) + P(6)$ 那么$P（even）=P（odd)=0.5$. 这个等式成立因为$P(0)$和$P(7)$其实是一回事，如果我们flip 0个head我们其实得到了7个tail，然后$P(7 tail) = P(7 head)$

如果我们 flip even number of times （8），因为每次的flip是independent那么我们可以把这个拆成flip 前7此和最后一次（第八次）， 那么因为coin 是fair的所以得到even或者odd的概率还是同样的（0.5）。
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


