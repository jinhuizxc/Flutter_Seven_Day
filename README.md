#### `多看星空方知何谓渺小，多看细胞方知何谓浩大，我是巨人,也是沙粒，崇高并谦卑着----张风捷特烈`

---

##### 写这个系列主要是出于以下目的：

```
1.给自己一个挑战，并附加时间限制
2.一直想要表达一下：遇到新技术时的态度，借此分析一下我对于一件新事物认知的过程  
3.Flutter对于Android开发者，确实需要去稍微了解一下 
4.作为一个地道的javaer+Androider,希望可以为想入坑Flutter的朋友铺条小路  
5.整个7篇文章贯穿着我学习的心+思，基本上敲一段测试代码，写一段文章。对我的学习方式也是一种记录与沉淀
```

---

##### 七篇文章如下：

- [Flutter第1天--初始分析+Dart方言+Canvas简绘](https://juejin.im/post/5c1637fe6fb9a049d5196438)  
- [Flutter第2天--Animation动画+粒子运动](https://juejin.im/post/5c176700f265da61602cd6ff)
- [Flutter第3天--基础控件(上)](https://juejin.im/post/5c18d181f265da611f07a128)
- [Flutter第4天--基础控件(下)+Flex布局详解](https://juejin.im/post/5c1a34f95188253ff1477cfd)
- [Flutter第5天--布局实例+操作交互](https://juejin.im/post/5c1b7af2518825566d237655)
- [Flutter第6天--异步-IO+网络访问+json](https://juejin.im/post/5c1cd2426fb9a049a711cb75)  
- [Flutter第7天--字体图标+综合小案例+Android代码交互](https://juejin.im/post/5c1df995e51d451611220186)


---

##### 下面是一边学习一边画出来的widget树 
>虽然离完整版还差一大半，不过入门还是够用了，常用的基本涉及  
当你这些用熟练了，其他控件看看属性也就无师自通了(推荐看原图，比较清楚)

![widget树](https://user-gold-cdn.xitu.io/2018/12/23/167db2f654687412?w=2114&h=1371&f=png&s=168516)
---

##### 第一天及体悟：

```
Flutter的环境搭建并没走多少弯路，网上教程一大堆。  
新建了一个工程,发现代码有点不对劲，虽然知道Flutter是跨平台框架，  
但是代码在哪写?不应该有个单独的src吗?以前玩过libgdx,认为应该差不多  
然后全文搜索一下界面上的字，找到在lib包的main.dart里
```

---

```
我要在lib里写代码?不会这么奇葩吧?然后我用面向对象的天眼看了一下main.dart
正如第一篇的分析，果然这么奇葩。而且语法与Java,c++,Python,Js都不一样， 
好吧，又要学方言了，自从JS的Es6玩转了以后,我就不怕语言了，
Kotlin也好，Python也好，这些性格"不羁"一些的和ES6都八九不离十  
只要语法通了，之后就是个人能力的问题了，所以Dart入门很快，半天就基本掌握了
想要熟练，那还必须去实际操练才行
```

---

###### [番外]：分享一些心情-------------

```
我经常把编程当做锻剑，我一直在精炼Java这把剑，用Android这把剑鞘盛放  
Python也好，C++也好，Js也好我只是玩玩，都被我当做光环对Java之剑进行附加
至今在Android中我遇三次瓶颈期，我选择暂时离开Android，去拓展一下视野，
死磕已经作用不大了，记得第二次瓶颈是被网络束缚地无法前进一步，
于是一咬牙，暂停安卓，去专门找后端的书和资料去看，也因此萌生了搭建自己网站的念头  
然后前后并行，两大光环加持，也上线了我的个人网站，两端的基础知识已基本在心中。
```

---


```
由于个人网站的搭建，我对服务端有了些认识，网络请求与上传下载也都知道是怎么回事  
也有了测试的渠道，如果一个对前后端毫不知情的Androider，肯定会卡网络瓶颈上
数据流的概念初步形成，在我的眼中，界面的展示、上传下载、网络上的一切都是字节的流动  
然后重归Android之时，前后端已经像一条线贯穿了,Android顺利和服务器交互时，第二瓶颈已过
有种"断剑重铸之日，骑士归来之时的感觉",具体细节，打算写个2018年终总结来记录一下
```
###### [番外]：截止-------------


```
如何很快地接收一件新事物(新知识)? 用你最擅长的技术去对接新知识，
比如你是个天文迷，如果你想学英语，去看天文方面的读物会更有利，
因为你有这方面的知识储备，即使知识储备是中文又如何?难道英文的地球能出太阳系?
语言和知识本就是两码事，语言表述知识并不会更改知识本身。
所以知识对接上，两种语言之间的交错，会让你更快接受语言的本身，也能强化知识
```

---

```
所以我并没有一开始就上控件，而是基于我最熟悉的Canvas来绘图，熟悉Dart语法，否则后面工作不好开展，
在Android中Canvas的丰富知识储备让我很好的与Flutter中的Canvas对接,这一棋自认为不错
对接之后，以前画网格，坐标系，n角星的东西又能拿出来秀了，旧知识转化成新知识
通过Java代码更改成Dart代码，也让我更清楚了两者的异同点，以后把握起来就轻松写  
```

>总的来说第一天还是蛮轻松好玩的。

---

##### 第二天及体悟：

```
第二天可以说是兵行险招，本打算把基础控件说一下的(依稀听过Flutter的控件超级多) 
但第一天图画好之后，非常想玩动画，如果放在后面，感觉不连贯  
然而并没有把握把动画写好，毕竟才更接触一天而已。挑战一下呗，然后就玩动画了
```


```
第二天可以说是这七天里我感觉最成功的，动画+粒子运动全都复刻到Flutter上了
粒子时钟完成后，挺激动的,然后就拿去分(xian)享(bai),心想，Flutter还是不错的嘛  
这绝对是Flutter的第一个粒子时钟(除了我，也许没有人会这么无聊做这种特效)
```


```
看上去第二天的文章好像一气呵成，其实也遇到了些阻碍，
dart的时间处理和三维数组和Java有些出入，还有就是时钟的粒子运动，
差一点就放弃了，因为效果总是出不来。心想，搞出个时钟就算了吧，不也挺好嘛。
可是真的很不甘心，都到这步了。然后输出小球集合的个数、第一个小球的位置，
数据好好的啊，可为什么出不来效果……最后发现小球半径没有设置……出来才有鬼呢
```



```
有人问我有没有什么心得，心得这东西说出来都懂，做起来却不简单，
如果你觉得一个人的学习方式很好，你应该去观察他，然后取长补短。
每个人的境遇都是不同的，别人的学习方法不一定适合你，你没有必要和别人一样。
比如我大学喜欢写诗，然后通读各大名著，不断思考世界，如果你没有这些基础，
我的心得就不一定适合你。每个人的价值观也是不同的，我是更倾向提升自我境界的那种人，
物质并不多求。心得这东西，别人的都是废话，需要的话，网上鸡汤自己挑，
一般人豪言壮语，大多只是自欺欺人。最近看到八个字挺实在:"生死看淡，不服就干"。
```

>总的来说第二天收获颇丰。

---

##### 第三、四天及体悟：

```
第三天基础控件，感觉应该很枯燥，所以我尽可能让它变得有趣
我喜欢画体系的树状图，因为这样看起来很清晰，也助于整理思路
我喜欢卡片，源于游戏王，对于繁多的事物，感觉用卡片记录一下比较有趣
```


---

```
第三天源码翻得比较多，基本上是进去看控件属性，代码测试
通过Android和html+css的布局经验，基本上套路都是那回事
而且Flutter的Flex布局和css的flex布局不谋而合，所以入手容易很多
遇到margin的时候，有点感触，写了点看到新东西的态度:

新事物往往都与旧事物有联系,学习新事物最好快速找到它与你知识库中旧事物的联系,
联系的多少取决于你知识库中内容的多少，连接得越多，你会越快或越能掌握旧事物 
```

---

```
本以为第四天可以把剩余的控件讲完，再写几个小案例呢，万万没想到:
Flutter的布局如此之多，再加上卡了一点小壳，只勉强把控件了结(实际上还有很多未涉及)
Flutter里面29种叠合模式也是吓到我了，也借此分析了一下这种多情况的分析方式
第三天把我的激情燃烧殆尽，第四天，三个控件一组，一共六组18张，没那么多花哨
最后将Flex布局详细说明了一下
```

---


```
这两天难度不是很大，就是有点麻烦，画图，配卡什么的，
只是敲代码的估计一天就够了，不过那样会及其无聊，不是我想要的
第四天写到最后其实还是有不少控件没涉及到呢，但感觉也就那回事
认识一个控件可就那点套路，属性基本上也就那些，遇到新的看看也就明白了
没有必要全部列出来，这就是"鱼与渔"的区别吧，鱼是抓不完的，你也放不下
```

---


```
两条源码翻得比较勤，有点小感悟：

有问题就去解决，即使牵涉出十个新问题，你就想象成问题栈，
有问题就进栈，解决了就出栈，这样不会乱，你可见的就是栈顶而已，
一个一个来，这样会相对于11个问题摆在你面前更容易接受。
至于什么时候stackover（栈溢出）就看你的决心和耐力了。
当然新手感觉hold不住时，可以深呼吸，咬一下牙坚持一下。
还是不行的话，记录下问题，果断退出。也许你现在等级不够，
这个boss你打不过，那就去刷怪升级吧。短剑重铸之日，骑士归来之时。
现在回头来看以前困扰我的问题，其实也并没有什么，这样你才能感觉成长
```

>总的来说第三、四天挺苦闷，但也是必经之路

---

##### 第五、六、七天及体悟：

```
经过前四天，基本上语法、控件也就熟悉了，接下来统一说一下：
第五天可以说非常有料，网上很少有详细分析Flutter怎么布局的
中文网的例子有点小复杂，我打算循序渐进地由简到难进行陈述
首先是最简单的条目入手一步步递进成掘金的条目，
交互操作看似很多，其实常用的也就那几个，操作也是widget这点非常有趣

```

```
第六天Dart的io,以及网络和json的处理，这是一门语言的基础
Java和Python还有node的io有所接触，所以dart这方面并不麻烦  
但一在Flutter上，路径不好拿，背景是跨平台，还好有三根救命稻草：`path_provider`
然后是权限问题，当然也有相应的依赖库`simple_permissions`，
网络库用起来比较简单,基本上和前端的网络库操作一致
```


```
第七天是前六天的知识整合，并扫一下其他小的知识点
Flutter与安卓的原生交互让我感觉它还是蛮好的，虽然有点麻烦
不过要跨平台，只与Android交互只是有半壁江山，ios那块就不好办了
虽说Flutter可以跨平台，但如果要玩得转，需要一个人兼具Android和ios
这样算来，这个跨平台代价还是有的，你也许会说，有插件包啊
但是插件包只能解决一部分问题，各种业务千差万别，如果只靠插件包，有点牵强
毕竟有些逻辑上的小修小补，具体问题框架无能为力，只能"凑合用"
Flutter是一个很好的UI框架，但可操作性，略有不足
```

---

##### 结束语

```
React玩的好的人入手Flutter可以说会轻松很多，因为思想非常相似
任何人都会有不足，不可能对这个世界全识全知，也就是"术业有专攻"
但并不意味这要闭关锁国，排斥外物。程序员读读诗，看看史也没有什么不可
多看星空方知何谓渺小，多看细胞方知何谓浩大，你是巨人也是沙，崇高并谦卑着
程序源于对这个世界的认知，何为境界，你眼中所视之物，究竟为何? 
学无止境，不要飘，脚踏实地，一步一印，殊途同归，新即远方，思之将至。
```

---

##### 最后插播一段感悟：我经常思考工具与使用者间的关系:  


```
`用工具`和`会用工具`之差异:[良庖岁更刀，割也；族庖月更刀，折也],
工具的使用方法体现了一位`工匠`的技艺  

《庖丁解牛》是我最喜欢的一篇古文，如何在做任何事上:
[以无厚入有间，恢恢乎其于游刃必有余地矣]是我的思考  

文中的八字成为我接触新事物的律典：[依乎天理，因其固然]。
通其理，方用之，是`匠者`与`匠师`的差异   

如果你不懂牛的构造原理，拿一把屠刀固然可杀牛取肉，
但庖丁的[以神遇而不以目视，官知止而神欲行]  
[提刀而立，为之四顾，为之踌躇满志，善刀而藏之]感觉也就与你无缘，
而这是一位匠者的自豪。 

写一个程序就像打造一件艺术品，制造的过程便是`解牛`，
IDE、API、运行环境就是我手中的剑  

普通屠夫遇牛则斩，好肉坏肉在一起切，煮成一大杂烩。
庖丁的匠心独运是我追求的境界:  
[吾生也有涯，而知也无涯,以有涯随无涯] 愿君且行且珍惜。
```

