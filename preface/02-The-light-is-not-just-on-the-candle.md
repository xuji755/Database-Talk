## 光不止在烛上

王阳明南下平定广西叛乱的途中，遇到了在河岸边静坐的弟子徐越。他见到心学宗师的时候异常激动，向王阳明诉说了他的种种悟道，不过都被王阳明一一否定了。后来王阳明把他唤到自己在江中的座船，指着船中蜡烛上的光芒，问道，“这是光，对吧？”，徐越点点头，王阳明接着指向船舱中空白的地方，“这也是光。”最后，王阳明把手指向江面上为烛光照映的粼波，“这也是光。” 最后王阳明总结说：“你明白了吗？光不仅在烛上！”

看到这里，有些朋友会疑惑了，搞数据库的人也开始开始讲起王阳明心学了吗？答案肯定不是的，我虽然做了三十年技术，不过对哲学并不精通。引用这个王门故事只是为了让读者理解我写这本“杂书”的目的，我并不是想手把手教你一些数据库的技术，而是想通过这些文字，把我对数据库的一些理解和思考传递给大家。数据库技术已经发展了半个多世纪，这些年来面临巨大的变革。从技术上，产业上都呈现出大变革前的乱世景象。商用数据库、开源数据库、分布式数据库、RDBMS、NOSQL、AI4DB、DB4AI等等，层出不穷。而随着世界风云的变化，国产数据库的强势兴起也是必然会发生的。

对于数据库国产化，很多朋友还在观望，觉得信创只是昙花一现，终究还是会回到Oracle称霸天下的时候的。不过从现在的国际国内形势来看，暂时还看不到这么乐观的情况。芯片法案为代表的一系列割裂全球化的举措会一步步的割裂这个世界，信息技术领域是重灾区。前两天，很多搞设计的人突然发现，自己的behance账号被封了，哪怕国籍是老外，只要是用中国ip注册的账号都受到了影响。虽然behance离我们DBA还挺远，不过还是值得我们警惕的。如果有一天我们发现metalink账号或者redhat账号被封了，那种感觉和前两天中国的设计师们的感觉应该是差不多的。

空谈数据库国产化的意义没有意义，大家现在很纠结要不要国产化的最主要原因还是国产数据库“不好用”，比不好用更大的顾虑是怕“用不好”。要想用好国产数据库，大幅提升国产数据库的可观测性能力，以及加速积累国产数据库的运维知识二者都是极其重要的。

在在2022年8月份工信部的一个沙龙上，我参会分享一个关于数据库可观测性的话题。谈到数据库的可观测性，就回到了“光不仅在烛上”这个题目了。按照王阳明的说法，我们在很多地方都可以看到烛光，我们不必来到王阳明的船舱里，盯着那个烛台，才能看到烛光。在船舱的窗棂边，在江中我们都可以看到。

昨天我看到一个PostgreSQL数据库故障诊断的案例，大体的意思是数据库遇到了一个莫名其妙的故障，有时候就会因为break piple导致会话中止。通过多种方法也找不到原因，最后只能使用GDB去跟踪，最终发现是因为SWAP耗尽导致无法分配内存。增加物理内存或者让SQL语句更简化一些，不要使用那么多内存就可以解决这个问题了。

数据库的可观测性提供了多种渠道来了解数据库的运行状态，指标、日志、跟踪与用户体验。就像王阳明所说的烛光一样，只要能够串起这些光的链条，那么看到任何一处光，我们就能找到源头在哪里。数据库可观测性能力提供给运维人员观察的渠道也是多样的，从日志中发现此类严重故障是最佳的方法，其次是指标中获得，实在没办法才会去用跟踪。

只不过我们现在的国产数据库或者开源数据库在这方面做的和国外商用数据库的差距还比较大。比如今天提的这个案例，如果PG数据库能够学习Oracle数据库一样，在报错时不仅仅是列出了当前报错，还把那些与OS相关的报错，收到的OS报错的信息也输出出来，恐怕我们一眼就能够看清楚是内存不足导致了这个问题。也就不需要用GDB这种终极大杀器去分析此类问题了。

此外分析此类问题的方法有很多，直接使用GDB去跟踪代码的行为就好比登上王阳明的小舟，进入他读书的舱室，这并不是任何人都能做到的。看到江中的光影，根据能够收集到的各种信息，通过关联与排除，我们也可以猜测到是王大师夜读，才有了这江上的一点渔火，岂不是更好。

要想实现这种可观测性，首先需要数据库厂商能够把产品做的更好一些，给运维人员更多的信息。其次是数据库厂商也需要更加开放，把这些信息公布出来，让我们的用户都能很方便的获取到这些信息，就像Oracle的METALINK一样。

另外一点就是这些运维知识能够得到充分的总结，如果在书店里能够看到大量的关于国产数据库运维与优化的书籍，那么我们的国产数据库生态才算真正的做好了。我也曾想过去写一本国产数据库优化的书籍，只不过因为资料太过零散，完全无法形成一本书的体系与规模，因此也就只能作罢了。



##  The light is not just on the candle

On his way south to put down the rebellion in Guangxi, Wang Yangming met his disciple Xu Yue who was meditating on the bank of the river. He was extremely excited when he saw the master of mind science and told Wang Yangming about his various enlightenments, but Wang Yangming rejected them all. Later, Wang Yangming called him to his boat in the river, pointed to the light on the candle in the boat, and asked, "This is light, right?" Xu Yue nodded, and Wang Yangming then pointed to an empty space in the cabin, "This is also light." Finally, Wang Yangming pointed to the waves on the river reflected by the candlelight, "This is also light." Finally, Wang Yangming concluded: "Do you understand? The light is not only on the candle!"

Seeing this, some friends will be confused. Have people who work on databases started to talk aboutWang Yangming's Psychology? The answer is definitely not. Although I have been working in technology for thirty years, I am not proficient in philosophy. I quote this Wang Yangming’s story  just to let readers understand my purpose of writing this "miscellaneous book". I don't want to teach you some database technology step by step, but I want to pass on some of my understanding and thinking about databases through these words.  Database technology has been developing for more than half a century and has faced tremendous changes over the years. Technically and industrially, the situation is like the chaotic times before the great changes. Commercial databases, open source databases, distributed databases, RDBMS, NOSQL, AI4DB, DB4AI, etc. emerge in endlessly. As the world changes, the strong rise of domestic databases is inevitable.

Regarding the localization of databases, many friends are still waiting and watching, thinking that  is very difficult to replace Oracle, and many jobs are just a flash in the pan. is just a flash in the pan and will eventually return to the time when Oracle dominated the world. However, judging from the current international and domestic situation, it is not yet possible to see such an optimistic situation. A series of measures to fragment globalization represented by the US government chip bill will fragment the world step by step, with the information technology field being the hardest hit area. Two days ago, many designers suddenly discovered that their behance accounts had been blocked. Even if they were foreigners, accounts registered with Chinese IP addresses were affected. Although behance is still far away from our DBA, it is still worthy of our vigilance. If one day we find that our Metalink account or redhat account has been blocked, the feeling should be similar to that of Chinese designers two days ago.

It is meaningless to talk about the significance of localizing databases. The main reason why everyone is confused about whether to localize databases is that domestic databases are not easy to use. The bigger concern is that they are not easy to use. In order to make good use of domestic databases, it is extremely important to greatly improve the observability capabilities of domestic databases and to accelerate the accumulation of operation and maintenance knowledge of domestic databases.

At a salon held by the Ministry of Industry and Information Technology in August 2022, I participated in the meeting to share a topic about database observability. When it comes to database observability, it comes back to the topic of "light doesn't just shine on a candle". According to Wang Yangming, we can see candlelight in many places. We don't have to come to Wang Yangming's cabin and stare at the candlestick to see candlelight. We can see it from the cabin window and in the river.

Yesterday I saw a case of PostgreSQL database fault diagnosis. The general meaning is that the database encountered an inexplicable fault, and sometimes the session was terminated due to a break piple. The reason could not be found through various methods. In the end, I could only use GDB to track it. Finally, I found that the memory could not be allocated because of SWAP exhaustion. This problem can be solved by increasing physical memory or making the SQL statement simpler and not using so much memory.

Database observability provides multiple channels to understand the running status of the database, indicators, logs, tracking and user experience. Just like the candlelight mentioned by Wang Yangming, as long as we can string together these chains of light, we can find the source of any light we see. The database observability capability provides various observation channels for operation and maintenance personnel. Finding such serious faults from logs is the best way, followed by obtaining them from indicators. Tracking is used only when there is no other way.

It’s just that the gap between our current domestic databases or open source databases and foreign commercial databases is still relatively large in this regard. For example, in the case mentioned today, if the PG database can learn from the Oracle database and not only list the current errors when reporting errors, but also output those OS-related errors and the received OS error information, I am afraid we will It's obvious at a glance that insufficient memory is causing the problem. There is no need to use GDB, the ultimate killer, to analyze such problems.

In addition, there are many ways to analyze such problems. Directly using GDB to track code is like boarding Wang Yangming's boat and entering the cabin where he studies. This is not something that everyone can do. Seeing the light and shadow in the river, based on the various information that can be collected, through correlation and elimination, we can also guess that it was Master Wang who read at night, which led to this little fishing fire on the river. Wouldn't it be better?

To achieve this kind of observability, database vendors first need to make their products better and give operation and maintenance personnel more information. Secondly, database manufacturers also need to be more open and publish this information so that our users can easily obtain this information, just like Oracle's METALINK.

Another point is that these operation and maintenance knowledge can be fully summarized. If you can see a large number of books on domestic database operation, maintenance and optimization in bookstores, then our domestic database ecology will be truly complete. I also thought about writing a book on domestic database optimization in the past, but because the information was too scattered, it was completely unable to form a system and scale of a book, so I had no choice but to give up.
