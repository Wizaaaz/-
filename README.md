# 排列组合综合复习

## 题型一：特殊元素和特殊位置优先策略
### 【例1】
有七名学生站成一排，某甲不排在首位也不排在末位的排法有多少种？

#### 【解析】
**方法1**（视学生甲为特殊元素，优先处理）  
分两步，先安排甲就位，有\(A_{5}^{1}\)种可能，再安排其他6名学生，有\(A_{6}^{6}\)种可能，由分步计数原理得排法有\(A_{5}^{1}A_{6}^{6}=3600\)种。  

**方法2**（视首位与末位为特殊位置，优先处理）  
分两步，先从其他6名学生中抽出2名学生在首位与末位就位（此时甲不可能坐在首位或末位），有\(A_{6}^{2}\)种可能，再安排剩下的5名学生就位，有\(A_{5}^{5}\)种可能，由分步计数原理得排法有\(A_{6}^{2}A_{5}^{5}=3600\)种。

## 题型二：相邻元素捆绑策略
从1，2，3，…，20中选取4个数组成四元数组\((a_{1},a_{2},a_{3},a_{4})\)，且满足\(a_{2}-a_{1}\geq3\)，\(a_{3}-a_{2}\geq4\)，\(a_{4}-a_{3}\geq5\)，则这样的四元数组\((a_{1},a_{2},a_{3},a_{4})\)的个数是( )  
A. \(C_{8}^{4}\) B. \(C_{11}^{4}\) C. \(C_{14}^{4}\) D. \(C_{16}^{4}\)

#### 解析：
将\(a_{1}\)连同其右边的2个空位捆绑，\(a_{2}\)连同其右边的3个空位捆绑，\(a_{3}\)连同其右边的4个空位捆绑，分别看作一个元素，四元数组\((a_{1},a_{2},a_{3},a_{4})\)的个数相当于从\(20 - 2 - 3 - 4 = 11\)个元素中选取4个，故这样的四元数组的个数是\(C_{11}^{4}\)，故选B。

## 题型三：不相邻问题插空策略
在一张节目表上原有6个节目，如果保持这些节目的相对顺序不变，再添加进去三个节目。  
（1）若三个节目连排，有几种排法？  
（2）若三个节目互不相邻，有几种排法？  
（3）有且仅有两个节目连排，有几种排法？

#### 【解答】
（1）三个节目连排，把这三个节目捆绑在一起，看作一个复合元素，插入原来6个节目所形成的7个空中的一个，有\(C_{7}^{1}A_{3}^{3}=42\)种方法；  
（2）三个节目互不相邻，把这三个节目，插入原来6个节目所形成的7个空中的3个，有\(A_{7}^{3}=210\)种方法；  
（3）有且仅有两个节目连排，先选2个节目相邻，并捆绑在一起，和另外一个节目，插入原来6个节目所形成的7个空中的2个，有\(A_{3}^{2}A_{7}^{2}=252\)种方法。

## 题型四：数字问题
用0，1，2，3，4，5这六个数字组成无重复数字的六位数，要求任意两个偶数数字之间至少有一个奇数数字，则符合要求的六位数的个数有______个。  
【答案】108

## 题型五：相同元素问题隔板策略
将\(n\)个相同的元素分成\(m\)份（\(n,m\)为正整数），每份至少一个元素，可以用\(m - 1\)块隔板，插入\(n\)个元素排成一排的\(n - 1\)个空隙中，所有分法数为\(C_{n - 1}^{m - 1}\)。

### 【例1】
有10个运动员名额，分给7个班，每班至少一个，有多少种分配方案？

#### 【解析】
题中说“10个运动员名额”，说明他们是没有差别的，把它们排成一排，相邻名额之间形成9个空隙。在9个空档中选6个位置插个隔板，可把名额分成7份，对应地分给7个班级，每一种插板方法对应一种分法，共有\(C_{9}^{6}\)种分法。

### 【变式1-1】
将6个相同的小球放入4个编号为1,2,3,4的盒子，求下列方法的种数。  
（1）每个盒子都不空；  
（2）恰有一个空盒子；  
（3）恰有两个空盒子。

#### 解
（1）先把6个相同的小球排成一行，在首尾两球外侧放置一块隔板，然后在小球之间5个空隙中任选3个空隙各插一块隔板，插板有\(C_{5}^{3}=10\)种。  
（2）恰有一个空盒子，插板分两步进行。先在首尾两球外侧放置一块隔板，并在5个空隙中任选2个空隙各插一块隔板，有\(C_{5}^{2}\)种插法，然后将剩下的一块隔板与前面任意一块并放形成空盒，有\(C_{4}^{1}\)种插法，故共有\(C_{5}^{2} \cdot C_{4}^{1}=40\)种。  
（3）共有\(C_{4}^{2} \cdot (C_{5}^{1}+C_{5}^{2})=30\)种。

## 题型六：整数解问题
### 【例1】
求方程\(x_{1}+x_{2}+x_{3}+x_{4}=5\)的非负整数解的个数。

#### 解
设\(y_{i}=x_{i}+1\)（\(i = 1,2,3,4\)），则方程等价于\(y_{1}+y_{2}+y_{3}+y_{4}=9\)（\(y_{1},y_{2},y_{3},y_{4}\)为正整数），则原题等价于将9个相同元素分成4份，每份至少一个，用隔板法可得，不同的分法有\(C_{8}^{3}=56\)种，即方程\(x_{1}+x_{2}+x_{3}+x_{4}=5\)的非负整数解有56个。

将20个无任何区别的小球放入编号为1，2，3的三个盒子中，要求每个盒内的球数不小于它的编号数，则不同的放法有（ ）  
A. 190种 B. 160种 C. 120种 D. 90种

#### 【解答】
先在编号为2，3的盒内分别放入1个，2个球，还剩17个小球，三个盒内每个至少再放入1个，将17个球排成一排，有16个空隙，插入2块挡板分为三堆放入三个盒中，共有\(C_{16}^{2}=120\)种方法。

不等式\(x_{1}+x_{2}+x_{3}\leq12\)，其中\(x_{1},x_{2},x_{3}\)是非负整数，则使不等式成立的三元数组\((x_{1},x_{2},x_{3})\)有多少组（ ）  
A. 560 B. 455 C. 91 D. 55

#### 【解答】
设\(a = x_{1}+1\)，\(b = x_{2}+1\)，\(c = x_{3}+1\)，转化为：\(3\leq a + b + c\leq15\)的正整数解的组数，因为方程：\(a + b + c = 3\)的解的组数为\(C_{2}^{2}\)，\(a + b + c = 4\)的解的组数为\(C_{3}^{2}\)，…，\(a + b + c = 15\)的解的组数为\(C_{14}^{2}\)，所以原不等式解的组数为：\(C_{2}^{2}+C_{3}^{2}+C_{4}^{2}+\cdots + C_{14}^{2}=C_{3}^{3}+C_{3}^{2}+C_{4}^{2}+\cdots + C_{14}^{2}=C_{15}^{3}=455\)。

## 题型七：定序问题
定序：一种是不同元素的顺序确定，另一种是相同元素的顺序（相同元素无排序，只有一种顺序）。  
（1）整体法，即若有\(m\)个元素有排成一顺序是确定的（不一定相邻），先解决这些固定不变的，基本方法有两种：\(m\)个元素排成一列，有\(A_{m}^{m}\)种不同的排法；然后任取一个排列，固定其他\(n\)个元素的位置不动，把这\(m\)个元素交换成一列，有\(A_{m}^{m}\)种不同的排法；然后任取一个排列，固定其他\(n\)个元素的位置不动，把这\(m\)个元素交换顺序，有\(A_{m}^{m}\)种排法，其中只有一个排列是不变的，因此共有\(\frac{A_{n + m}^{n + m}}{A_{m}^{m}}\)种满足条件的不同排法。  
（2）插空法，即\(m\)个元素之间的先后顺序确定不变，因此先排这\(m\)个元素，只有一种排法，然后把剩下的\(n\)个元素分类或分步插入由以上\(m\)个元素形成的空隙中。

### 【例1】
7人排队，其中甲乙丙3人顺序一定共有多少不同的排法？

#### 解析
对7人全排列有\(A_{7}^{7}\)种排法，其中甲乙丙的顺序是随意的，甲乙丙三人排列一共有\(A_{3}^{3}\)种（分别是甲乙丙、甲丙乙、乙甲丙、乙丙甲、丙甲乙、丙乙甲），假设“7人排队，其中甲乙丙3人按甲乙丙顺序”有\(x\)种排法，则后5种情况同理也是有\(x\)种排法，所以\(A_{3}^{3} \cdot x = A_{7}^{7} \Rightarrow x = \frac{A_{7}^{7}}{A_{3}^{3}}\)。

毕业十周年校友们重返母校，银杏树下，有五名校友站成一排拍照留念，其中甲不排在乙的右边，且不与乙相邻，则不同的站法共有（ ）  
A. 66种 B. 60种 C. 36种 D. 24种

#### 【详解】
先排甲、乙外的3人，有\(A_{3}^{3}\)种排法，再插入甲、乙两人，有\(A_{4}^{2}\)种方法，共有\(A_{3}^{3} \times A_{4}^{2}\)种方法，又甲排乙的左边和甲排乙的右边各占\(\frac{1}{2}\)，故所求不同和站法有\(\frac{1}{2}A_{3}^{3}A_{4}^{2}=36\)种，故选：C。

## 题型八：不同元素分配问题
### 【例1】
6本不同的书，分给甲、乙、丙3人，在下列条件下各有多少种不同的分配方法？  
（1）甲2本，乙2本，丙2本；  
（2）甲1本，乙2本，丙3本；  
（3）甲4本，乙、丙每人1本；  
（4）每人2本；  
（5）一人1本，一人2本，一人3本；  
（6）一人4本，其余两人每人1本。

#### 解
（1）（2）（3）中，由于每人分的本数固定，属于定向分配问题，由分步乘法计数原理得：  
（1）共有\(C_{6}^{2}C_{4}^{2}C_{2}^{2}=90\)种不同的分配方法；  
（2）共有\(C_{6}^{1}C_{5}^{2}C_{3}^{3}=60\)种不同的分配方法；  
（3）共有\(C_{6}^{4}C_{2}^{1}C_{1}^{1}=30\)种不同的分配方法。  
（4）（5）（6）属于不定向分配问题，是该类题中比较困难的问题。分配给3人，同一本书给不同的人是不同的分法，属于排列问题。实际上可看作两个步骤：先分为3组，再把这3组分给甲、乙、丙3人的全排列数\(A_{3}^{3}\)即可。因此，  
（4）共有\(C_{6}^{2}C_{4}^{2}C_{2}^{2} \div A_{3}^{3} \times A_{3}^{3}=90\)种不同的分配方法；  
（5）共有\(C_{6}^{1}C_{5}^{2}C_{3}^{3} \times A_{3}^{3}=360\)种不同的分配方法；  
（6）共有\(C_{6}^{4}C_{2}^{1}C_{1}^{1} \div A_{2}^{2} \times A_{3}^{3}=90\)种不同的分配方法。

现将《西游记》、《红楼梦》、《水浒传》、《三国演义》、《史记》、《资治通鉴》6本不同的书籍分发给甲乙丙3人，每人至少分得1本，已知《西游记》分发给了甲，则不同的分发方式种数是（ ）  
A. 180 B. 150 C. 120 D. 210

#### 【解答】
解：根据题意，分2步进行分析：  
①将6本不同的书籍分为3组，每组至少1本，  
若分为4、1、1的三组，有\(C_{6}^{4}=15\)种分组方法，  
若分为3，2，1的三组，有\(C_{6}^{3}C_{3}^{2}=60\)种分组方法，  
若分为2，2，2的三组，有\(\frac{C_{6}^{2}C_{4}^{2}C_{2}^{2}}{A_{3}^{3}}=15\)种分组方法，  
共有\(15 + 60 + 15 = 90\)种分组方法，  
②将《西游记》所在的组分发了甲，剩下2组任意分配，有2种情况，  
则有\(90×2=180\)种分发方式。

## 题型九：排列组合混合问题
设集合\(A=\{(a_{1},a_{2},a_{3},a_{4},a_{5},a_{6}) | a_{i} \in \{-1,1\}, i = 1,2,3,4,5,6\}\)，那么集合\(A\)中满足条件“\(-2\leq a_{1}+a_{2}+a_{3}+a_{4}+a_{5}+a_{6}\leq2\)”的元素的个数为（ ）  
A. 35 B. 50 C. 60 D. 180

#### 【解答】
∵集合\(A=\{(a_{1},a_{2},a_{3},a_{4},a_{5},a_{6}) | a_{i} \in \{-1,1\}, i = 1,2,3,4,5,6\}\)，要满足“\(-2\leq a_{1}+a_{2}+a_{3}+a_{4}+a_{5}+a_{6}\leq2\)”，由题可得：\(a_{i}\)中有2个-1，4个1，或3个-1，3个1，或4个-1，2个1，共三类情况符合条件。所以\(A\)中满足条件的元素的个数为：\(C_{6}^{2}+C_{6}^{3}+C_{6}^{4}=50\)。

一只蚂蚁从正四面体\(ABCD\)的顶点\(A\)出发，沿着正四面体的棱爬行，每秒爬一条棱，每次爬行的方向是随机的，则蚂蚁第1秒后到点\(B\)，第4秒后又回到点\(A\)的不同爬行路线有（ ）  

根据已知，可作出下图。由图知不同的爬行路线有7条，故选B。

一项单人游戏规则如下：先将一棋子放在如图所示正方形\(ABCD\)（边长为2个单位）的顶点\(A\)处，然后通过掷骰子来确定棋子沿正方形的边按逆时针方向行走的单位，如果掷出的点数为\(i\)（\(i = 1,2,\cdots,6\)），则棋子就按逆时针方向行走\(i\)个单位，一直循环下去。某人抛掷了三次骰子，若棋子恰好又回到点\(A\)处，则所有不同走法共有（ ）  
A. 22种 B. 24种 C. 25种 D. 27种

#### （法二）
同法一分析可得三次掷骰的点数之和是8或16。  
若点数之和是8，则相当于把8个相同的点分成3份（每份至少有1个点），只需在这8个点形成的7个空（不包括首尾）中插入2个隔板，有\(C_{7}^{2}=21\)种方法；  
若点数之和是16，则抛掷三次有\(\{4,6,6\}\)，\(\{5,5,6\}\)这2种点数组合，且每种组合包含\(C_{3}^{1}=3\)种走法，故共有\(2×3=6\)种走法。  
所以抛掷三次骰子后棋子恰好又回到点\(A\)处的所有不同走法有\(21 + 6=27\)种，故选D。

一个旅游景区的游览线路如图所示，某人从\(P\)处进，\(Q\)处出，沿图中线路游览\(A\)，\(B\)，\(C\)三个景点及沿途风景，则不重复（除交汇点\(O\)外）的不同游览线路有（ ）  
A. 6种 B. 8种 C. 12种 D. 48种

#### 解析
参观第一个景点，从\(P\)处进入后，参观第一个景点时，有6条路可以选择，从中任选一个，有6种选法；参观完第一个景点，参观第二个景点时，有4条路可以选择，从中任选一个，有4种选法；参观完第二个景点，参观第三个景点时，有2条路可以选择，从中任选一个，有2种选法。由分步乘法计数原理，共有\(6×4×2=48\)种不同的游览路线，故选D。

## 题型十：环排问题
一般地，\(n\)个不同元素作圆形排列，共有\((n - 1)!\)种排法。如果从\(n\)个不同元素中取出\(m\)个元素作圆形排列共有\(C_{n}^{m} \cdot (m - 1)! = \frac{1}{n}A_{n}^{m}\)。  
（1）把\(n\)个不同的元素围成一个环状，排法总数为\(A_{n - 1}^{n - 1}\)。  
（2）\(n\)个不同的元素围成一圈，\(m\)个元素相邻（\(n \geq 2m\)），符合条件的排列数为\(C_{n - m}^{1}A_{m}^{m}A_{n - m - 1}^{n - m - 1}\)。  
（3）\(n\)个不同的元素围成一圈，\(m\)个元素不相邻（\(n \geq 2m\)），符合条件的排列数为\(A_{n - m}^{n - m}A_{n - m - 1}^{m}\)。

有5对夫妇和\(A\)，\(B\)共12人参加一场婚宴，他们被安排在一张有12个座位的圆桌上就餐（旋转之后算相同坐法）。  
（1）若5对夫妇都相邻而坐，其中\(A\)，\(B\)相邻而坐，共有多少种坐法？  
（2）若5对夫妇都相邻而坐，其中\(A\)，\(B\)二人的太太是闺蜜要相邻而坐，\(A\)，\(B\)不相邻，共有多少种坐法？

#### 【解答】
（1）若5对夫妇都相邻，分三步来完成，  
第一步，排\(A\)，\(B\)二人的座位，有2种坐法，  
再将每对夫妇看成1组，\(A\)，\(B\)二人的座位也随之确定；  
再将这6组人围成一圈，  
共有\(A_{5}^{5}\)种坐法，  
由于每一组内两人还有顺序问题，  
所以共有\(A_{5}^{5}×2^{5}=7680\)种坐法；  
（2）第一步，排其余3对夫妇的座位，有\(2^{3}A_{3}^{3}\)种坐法，  
第二步，排\(A\)，\(B\)二人的座位，有\(A_{4}^{2}\)种坐法，  
根据分步乘法计数原理，共有\(2×2^{3}A_{3}^{3}×A_{4}^{2}=1536\)种坐法。

## 题型十一：分类讨论策略
已知\(a_{1},a_{2},\cdots,a_{5}\)为1，2，3，4，5的任意一个排列，则满足：对于任意\(n \in \{1,2,3,4,5\}\)，都有\(a_{1}+a_{2}+\cdots+a_{n}\leq na_{1}\)的排列\(a_{1},a_{2},\cdots,a_{5}\)有多少个？

#### 【解析】
根据题意，\(a_{1},a_{2},\cdots,a_{5}\)为1，2，3，4，5的任意一个排列，  
则\(a_{1}+a_{2}+\cdots+a_{5}=1 + 2 + 3 + 4 + 5=15\)，  
若\(a_{1}+a_{2}+\cdots+a_{5}\leq5a_{1}\)，必有\(a_{1}\geq3\)，  
当\(a_{1}=5\)时，任意排列都符合题意，此时有\(A_{4}^{4}=24\)个排列，  
当\(a_{1}=4\)时，只要\(a_{2}\neq5\)即符合题意，此时有\(3A_{3}^{3}=18\)个排列，  
当\(a_{1}=3\)时，\(a_{2}=1\)或2，此时有32145、31245、32154、31254、32415、31425、31524，共7个排列符合题意，  
则有\(24 + 18 + 7=49\)个满足题意的排列。

定义“规范01数列”\(\{a_{n}\}\)如下：\(\{a_{n}\}\)共有\(2m\)项，其中\(m\)项为0，\(m\)项为1，且对任意\(k \leq 2m\)，\(a_{1},a_{2},\cdots,a_{k}\)中0的个数不少于1的个数。若\(m = 4\)，则不同的“规范01数列”共有（ ）  
A. 18个 B. 16个 C. 14个 D. 12个

#### 解析
（法一）由题意知，必有\(a_{1}=0\)，\(a_{8}=1\)，具体的排法列表如下：  
通过列表可知，不同的“规范01数列”共有14个，故选C。

## 题型十二：正难则反总体淘汰策略
### 【例1】
6人排成一行，甲不排在最左端，乙不排在最右端，共有多少种排法？

#### 解析
6人全排列，有\(A_{6}^{6}\)种方法；  
甲在最左端，有\(A_{5}^{5}\)种方法；乙在最右端，有\(A_{5}^{5}\)种方法；  
甲在最左端且乙在最右端，有\(A_{4}^{4}\)种方法；  
则一共有\(A_{6}^{6}-A_{5}^{5}-A_{5}^{5}+A_{4}^{4}=720 - 2×120 + 24=504\)种方法。（利用集合中的venn图，更便于理解）

若把英文单词“error”中的字母的拼写顺序写错了，则可能出现错误的种数是（ ）  
A. 20种 B. 19种 C. 10种 D. 9种

#### 【解答】
解：根据题意，英语单词“error”中有5个字母，其中3个“r”，  
先排字母“e”，“o”，在5个位置中任选2个，放置字母“e”，“o”即可，有\(A_{5}^{2}=20\)种不同的排法，  
再安排3个“r”，直接将其放进剩余的3个位置即可，有1种排法，  
则这5个字母有\(20×1=20\)种不同的排法，其中正确的顺序有1种，  
则可能出现的错误的种数是\(20 - 1=19\)种。

## 题型十三：涂色问题
涂色问题，要从“颜色用了几种”，“地图有没有公用区域”方向考虑：  
1. 用了几种颜色，如果颜色没有全部用完，就要有选色的步骤。  
2. 尽量先从公共相邻区域开始，所以要观察“地图”是否可以“拓扑”转化，比如以下这俩图，就是“拓扑”一致的结构。

### 【例1】
将红、黄、蓝、白、黑五种颜色涂在如图所示“田”字形的4个小方格内，每格涂一种颜色，相邻两格涂不同的颜色，如果颜色可以反复使用，共有多少种不同的涂色方法？

#### 解
第1个小方格可以从5种颜色中任取一种颜色涂上，有5种不同的涂法。  
①当第2个、第3个小方格涂不同颜色时，有\(4×3=12\)种不同的涂法，第4个小方格有3种不同的涂法，由分步乘法计数原理可知有\(5×12×3=180\)种不同的涂法。  
②当第2个、第3个小方格涂相同颜色时，有4种涂法，由于相邻两格不同色，因此，第4个小方格也有4种不同的涂法，由分步乘法计数原理可知有\(5×4×4=80\)种不同的涂法。  
由分类加法计数原理可得共有\(180 + 80=260\)种不同的涂法。

## 题型十四：与立体几何的涂色
立体型结构，可以“拍扁了”，“拓扑”为平面型涂色，然后转换为平面图形涂色，这是几何体染色的一个小技巧所以注意这类图形之间的互相转化。

### 【例1】
如图所示，将一个四棱锥的每一个顶点染上一种颜色，并使同一条棱上的两个端点异色，如果只有5种颜色可供使用，则不同染色方法的种数为（ ）  
A. 192 B. 420 C. 210 D. 72

## 题型十六：最短路径问题（台阶问题）
李老师从家到学校，可以选择张成路、张西路、张杨路或者张东大道，由于李老师不知道张成路有一段在修路导致某一天迟到了，所以李老师决定以后要绕开那段维修的路，如图，假设李老师家在\(M\)处，学校在\(N\)处，\(AB\)段正在修路要绕开，则李老师从家到学校的最短路径有（ ）条。

#### 【分析】
先求出由\(M\)到\(N\)的最短路径的条数，然后求出由\(M\)到\(N\)且经过\(AB\)的最短路径的条数，最后相减即可。

#### 【详解】
由\(M\)到\(N\)的最短路径需要向右走四段路，向上走三段路，所以有\(C_{7}^{3}=35\)条路。  
由\(M\)到\(A\)的最短路径需要向右走两段路，向上走一段路，所以有\(C_{3}^{1}=3\)条路，  
由\(B\)到\(N\)的最短路径需要向右走一段路，向上走两段路，所以有\(C_{3}^{1}=3\)条路，  
所以由\(M\)到\(N\)不经过\(AB\)的最短路径有\(C_{7}^{3}-C_{3}^{1}C_{3}^{1}=26\)。  
A. 23 B. 24 C. 25 D. 26

某城市街道的平面图如图所示，若每个路口仅能沿右、左上、右上三个方向走，从\(A\)至\(B\)的路径条数有\(n\)条：若\(P\)、\(Q\)两处因故施工，不能通行，从\(A\)至\(B\)的路径条数有\(m\)条，则\(n\)，\(m\)分别为（ ）  
选：A。  
A. 1552；256 B. 1440；256 C. 1552；288 D. 1440；288

## 题型十八：错位排序
若5个人各写一张卡片（每张卡片的形状、大小均相同），现将这5张卡片放入一个不透明的箱子里，并搅拌均匀，再让这5人在箱子里各摸一张，恰有1人摸到自己写的卡片的方法数有（ ）  
A. 20 B. 90 C. 15 D. 45

#### 【解答】
解：根据题意，分2步分析：①先从5个人里选1人，恰好摸到自己写的卡片，有\(C_{5}^{1}\)种选法，②对于剩余的4人，因为每个人都不能拿自己写的卡片，因此第一个人有3种拿法，被拿了自己卡片的那个人也有3种拿法，剩下的2人拿法唯一，所以不同的拿卡片的方法有\(C_{5}^{1} \cdot C_{3}^{1} \cdot C_{3}^{1}=45\)。

现有甲、乙、丙等7位同学，各自写了一封信，然后都投到同一个邮筒里。若甲、乙、丙3位同学分别从邮箱随机抽取一封信，则这3位同学抽到的都不是自己写的信的不同取法种数是______。

#### 【解答】
解：设甲、乙、丙3位同学的信件分别为\(A\)、\(B\)、\(C\)，  
若\(A\)、\(B\)、\(C\)都没取到，则有\(A_{4}^{3}A_{3}^{3}=72\)种不同的取法；  
若\(A\)、\(B\)、\(C\)取到一个，则有\(C_{3}^{1}A_{4}^{2}A_{3}^{3}=36\)种不同的取法；  
若\(A\)、\(B\)、\(C\)取到两个，则有\(C_{3}^{2}(A_{4}^{1}A_{3}^{3}+C_{3}^{2})=2\)种不同的取法；  
综上可得一共有\(72 + 36 + 2=134\)种不同的取法。