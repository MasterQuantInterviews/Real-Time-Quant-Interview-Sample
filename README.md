# Real Time Quant Interview - Sample

## 指南（必读）
这是一本专门为2018年及以后买卖方quant岗位面试刷题所设计的大纲。作者归纳了自2018年以来200+个买卖方（英+美）面试经验，来源包括作者及朋友的面试经历，以及作者现在作为面试官的出题思路。大家可以把这本资料理解为近五年quant英国/美国quant面试的经验汇总。取名Real Time Quant Interview也是代表了这里的题和知识点是与时俱进的，使用大家不需要担心这些题是否过时了的问题。

作者介绍：本硕物理专业+博士计算机专业， 毕业后在美国前三的投行做equity quant research，现在从事futures quant trading。

这本资料主打的方向就是具体。很多同学反应不管是自己刷红绿皮书，还是询问朋友/同学的面试经历，还是找中介咨询都很难得到一个quant面试的具体刷题思路。比如大家都知道要刷dynamic progamming，但具体是要刷 1 dimensional DP 还是 2 dimensional DP 还是都要刷？ 如果都要那比例怎么分配？去解答这些问题我们只需要去分析历年的面试真题就能得到这几年买卖方对于不同topic的侧重比，从而大家可以根据自己的申请方向去定制刷题计划。

这本资料分成三大部分：1. Probability & Statistics, 2. Dynamic Programming, 3. Other Maths and Machine Learning。 每一章只需要一个小时左右就能看完，但效率及结果等同于几十甚至上百个面试经验。看完大家会知道其实大多数的面试题不会很难，大多是可能一两句话就可以给出答案。毕竟平均一场面试只有一个小时左右，每个面试平均3，4道题，所以面试官不可能问一些特别复杂的题类似数学推导等等。这也就是说我们只要能够找到面试官问的题背后所需要的知识点并阐述，即使最后没有百分百答对也能获得所谓的"过程分"。

---

## Q & A（必读）
- 这本资料的意义是什么？
  - 主要是为想从事quant 方面工作的同学提供一个刷题的思路和大纲
- 这本资料的受众群体是谁？
  - 受众群体主要是想从事quant 方面工作的本科，研究生，博士以及junior quant们。这本资料的主要针对卖方投行定价quant，hedge fund quant research/trading， 以及market maker 的trader 及相关的岗位
- 这本资料面对的是哪个国家的岗位？
  - 这里的题主要来自英国和美国的面试
- 这本资料和市面上其他quant 题库例如红皮书绿皮书有什么区别？
  - 这个更多是一个大纲而不是一个题库。 以红绿皮书为代表的quant 题库/书在市面上以及流传很久了，以至于现在任何人面试之前都要刷这几本书。其次这些题库基本都是7，8年前写出来的， 很多题已经过时。 很多同学使用红绿皮书的都反应没有一个clear direction。 这些题库往往有上百道题，对于面试经验较少的同学来说很难去找到侧重点。
  - 使用红绿皮书是希望通过大量刷题从而达到押题的目的， 可以理解为：刷大量的题->面试正好碰到刷过的题或者类似的题型。 这种方法非常耗时并且现在已经不太现实因为现在quant面试的广度越来越大，而且现在很多公司也知道大家都在刷这几本书所以在面试中也会可以去改变题型。庆幸的是不管题型怎么改它们背后的知识点是不变的。
  - 因此我写这本资料的初衷是通过分析这几年（2018年之后）的买卖方面试真题去找所需要的重要知识点以及解题/出题思路。这可以理解为 找到这几年真题背后的知识点/思路 -> 面试中在所掌握的知识点中去寻找最适用的知识点完成答题。这种显然比只使用红绿皮书节省时间（以及脑细胞）。
  - 其次，这本资料最大的优势在于所有的题都是近几年买卖方的面试真题，我会附上公司，年份及job/programme title。
- 这本资料能取代红绿皮书吗？
  - 不能， 这本资料的最大作用是用实战经验去提供刷题思路和方向，所以每个topic的重点是背后所需要的知识点。大家可以依靠我总结的知识点再去这些题库里找额外相似的题去刷，从而达到巩固知识点的效果。
- 这本资料的最佳使用方法是什么？
  - 最佳使用方法是先读本资料的某个topic然后去以下（或其他）题库寻找类似的题去刷：
    - 绿皮书 A Practical guide to quant interviews
    - A collection of dice problems
    - Fifty challenging problems in probability with solutions
      
---

## Probability & Statistics
统计方面的题不管是在卖方还是买方都是很重要的一个环节。在投行Quant面试里统计/概率面试题相对来讲会简单一些。投行的Quant比较注重于数理和编程能力的全面性，因此问的问题也广度大于深度。对于hedge fund来讲概率题的难度方差比较大。而对market maker （例如optiver）来讲概率题+心算能力会是面试的重要考点。因此对于刷概率题的侧重比则需要看申请的是哪种类型的公司。  

这个章节包含了投行，fund，以及market maker这三四年的面试真题并且分析所需要的知识点和出题逻辑等。刷题的数量不等于刷题的效率，从一道真实面试题我们可以分析总结有哪些知识点我们需要背下来，以及不同知识点的重要性和题型的规律。以概率题为例子，近几年的面试题通常为两种， 一种是面试官会形容一个scenario然后要求candidate算某个outcome的probability， 而另外一种是算一种或多种outcome的expected value/time 等等。能够通过分析真实面试题而找出这些出题规律的效率会远远高于从一些题库中大量但没有重点的刷很多可能面试里永远不会出现的题型。  

我会在这个章节给出这几年收集到的20道有代表性的概率方面的面试题，也会给出对应的公司和internship/全职工作岗位的名字， 面试流程方面的信息如果有我也会列出。这里给出题的顺序是随机的，并不是以难度的顺序呈现.

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

以目前情况来看这种基础的bayes formula已经是必问的题目。由于它过于简单基本上是答不上来扣分但答上来不加分的题型。所以大家务必对这种算conditional probability的题非常熟练。

---

### 例题2

Jane Street Quant Trading Internship 2023 

问: You flip a fair coin a large number of times, what is the probability of getting an even number of heads?

答：0.5

解析： 这道题在market maker的面试里算是非常简单的，但是他的核心知识点是symmetry， 也就是说很多时候一个很复杂的情况我们可以用symmetry去把它变成一个简单的情况。比如说我们 flip odd number of times （7） 那么我们可以得到0，2，4，6
或者1，3，5，7个head。因为 $P(1)+P(3)+P(5)+P(7) = P(0) + P(2) + P(4) + P(6)$ 那么 $P(even)=P(odd)=0.5$ . 这个等式成立因为 $P(0)$ 和 $P(7)$ 其实是一回事，如果我们flip 0个head我们其实得到了7个tail，然后 $P(7 tail)=P(7 head)$

如果我们 flip even number of times （8），因为每次的flip是independent那么我们可以把这个拆成flip 前7次和最后一次（第八次）， 那么因为coin 是fair的所以得到even或者odd的概率还是同样的（0.5）。

如此可见用symmetry可以把很多复杂的问题简单化。很多market maker问的概率题听着很复杂但其实可以用symmetry换一种方法理解并解答。Symmetry在绿皮书里的题个人推荐61页的Coin toss game。很多时候类似的面试题会比较两个事物或者人然后其中一个比另外一个多出一些东西。那我们首先要做的是问如果两个人/物是完全相等的会不会影响概率，如果不影响那么我们可以只考虑多出来的那一部分，比如一个人比另外一个人多了n个coin其他的都一样那么我们只需要考虑多出来的n个coin的event的概率。

Jane street 以及其他market maker的面试大多是2-3论的电话/线上面试+最后一轮线下的trading game。trading game主要是mock market making的小游戏。面试里的题目五花八门很难去做专门的准备，不过多数以probability/expected number为主，以及各种order of magnitude估值+快速心算。

以symmetry为基础的概率题在高盛和citadel quant research实习面试里同样出现非常频繁。

---

### 例题3

JP Morgan Securities Services Quant Research 全职 2022 

问: given you have 3 noodles, you pick two ends randomly. if the two ends belong to the same noodle you form a loop, what is the expected number of loops for 3 noodles?

答：这道题其实还涉及到dynamic programming， combinatorics。 假设 $E(1)$ 是expected number of loop from 1 noodle， 我们知道 $E(1)=1$ 因为一根面条的两个end必定形成一个loop。现在我们考虑两根面条 $E(2)$。 两根的情况下有四个end，我们随机抽取两个end的话有 ${4 \choose 2} = 6$ 中抓法。其中两种可能可以让我们形成loop：也就是我们抓了第一根面条的两个end或者第二个面条的两个end。所以我们形成新loop的概率是2/6. 剩下的四种抓法不管怎么都不会有新的loop所以结果还是只有一个loop。 那么 $E(2) = 1/3(E(1) + 1) + 2/3E(1)$. 以此类推我们可以用同样的方法去算任何的n，我们只需要知道 $E(n-1)$ 然后去算形成下一个新loop的概率。

解析：由此可见，大部分算expected number/value的题都可以用dynamic programming 去得到答案。最好的方法是去画一个图，每个node是一个state （比如说一个/两个loop）然后每两个node之间的connection都有相对应的概率。这样可以很容易看到从一个node出发能达到的下一个node有哪些。Dynamic programming的精髓就是每一个问题都有一个base case， 这里则是 $E(1) = 1$。 这种base case的答案普遍非常简单，根据这个简单的base case我们可以一步步往后推到我们想要的n。

JP 的quant 岗位面试的流程不太一样。 Intern的话一般是第一轮hackerrank 两道编程题+录视频解释解题思路。不过这两道编程题不会很难，2020和2023问道过fibonnaci和基础pandas比如给一个csv然后算mean，median然后print出来。个人来看JP的hackerrank相对高盛来讲非常简单，不过有朋友反应做coding的时候有可能也会被要求开摄像头。有的programme 比如说 AI & Data Science 是第一轮过了会有第二轮的background check，也就是一个小时的technical 面试。有的则是过了第一轮直接assessment centre。对于很多quant 实习其实AC就是一个4-6小时的车轮面试，也会涉及到一些machine learning的东西。有意思的是很多投行组喜欢问一些ML的题，虽然他们可能平时不会用到任何的ML。这点和很多fund非常不一样。一般只有会用ml的fund才会问ml方面的面试题。

JP 的QR全职有的是没有第一轮hackerrank。Securities services则是直接4个小时的面试，会涉及到一些option方面的问题，例如black scholes assumptions等。

---

### 例题4

DRW Quant Researcher Internship 2023 

问: what is the expected number of throws to get three consecutive heads using a fair coin?

答：14, 这种类型的题目个人认为可以用一个fair casino 的例子去理解，详情在这个视频：https://www.youtube.com/watch?v=t8xqMxlZz9Y

解析： 这种以骰子或硬币为基础的probabiliy/expected number题是很多market maker 的最爱。这道题算是这种类型的里面比较简单的一道。这种题一旦找到规律非常好答， 最简单的方法就是去找重复的pattern然后把他们的expected number 加到一起。以HHH为例，HHH 的概率是1/8 所以expected number是8，但是我们发现从第二个字母开始的HH也可以作为HHH的开始，HH的概率是1/4所以expected number 是4. 最后一个H 也可以是HHH的开始所以又多了1/（1/2）=2. 把这三个term加到一起就是8+4+2=14. 

个人面试market maker的时候经常被问到某种sequence的expected number， 遇到比较复杂的sequence我们可能一步步的推导。以上视频里有解释算HH的expected number 的逻辑，那么面试的时候如果面试官问HHHHHHH，我们可以先讲一下比如算HH的方法向面试官证明我们懂得背后的逻辑，然后再用我上面写到的找重复pattern的方法去算长sequence的expected number。当问到的sequence特别复杂的时候，比如下一道来自Jane Street的一道题（例题5）， 我们可以用同样的方法很简单的算expected number。

虽然很多market maker 的quant trading 和 quant researcher是分开申请的岗位，但是很多公司会让quant trader去面quant researcher， 也就是说面试的题型可能不会有太大的区别，所以面QR的同学也需要练一下自己的心算能力和提前熟悉各种distribution的properties， 比如mean median mode 的公式都需要背下来。重点要bernouli, binomial, geometric, poisson, exponential, uniform.

---

### 例题5

Jane Street Quant Trading Internship 2020 

问: what is the expected number of keystrokes to type the word ABRACADABRA?

答：26<sup>11</sup> + 26<sup>4</sup> + 26

解析：这道题是例题4的难度加长版。以个人经验来看这几家market maker （optiver， flow traders， jane street， drw等）里面jane street的题普遍难度会高一等。不过用例题4里提到的方法我们只需要找到首位重复的pattern即可。直接打abracadabra的概率是（1/26）<sup>11</sup>所以expected number是26<sup>11</sup>. 可以看到后面的ABRA也可以作为整个sequence的开始，所以要加上26<sup>4</sup>，最后的字母A也可以作为sequence的开始所以最后加上26.   

---

### 例题6

Capula Investment Management Quant Trading Internship 2021 

问: you have £x and you flip a fair coin, every time you land on head you get £1 or -£1 if it lands on tails. you stop playing if you lose all your money or reach £100, what is your probability of winning.

答：p=x/100

解析： 这是一道非常典型的gamlbers ruin题。当我们的expected change是0的时候，我们只需要几下赢的概率是current position/total position就可以。如果coin不是fair的话会复杂的很多，详情可以看各种stats的lecture notes， 不过目前来说作者还没有见到任何公司问unfair coin的情况。Gamblers ruin的题目近几年非常受欢迎所以大家可以多背一些相关的properties。例如面试官还可以问what is the expect time for the gamlber to reacher either 0 or 100？答案是x（100-x）。我们可以提前看一些lecture notes然后几下一些这些很快能答上来的properties。 

Capula的实习面试是一轮behavioural，一轮techinical，一轮head of hr 面试。Technical面试是一个小时5道题，其中只有一道概率题。

---


