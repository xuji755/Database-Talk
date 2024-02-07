## 打榜的意义

今天我终于把用了块一年的百度输入法删除换回微软输入法了，主要的原因是我把一大堆花里胡哨的云功能关闭后，词组和短语输入的能力就很弱了，而云功能在网络不好的情况下经常不WORD等搞得很卡顿，甚至进入假死状态，让我的辛勤工作付之东流。一个输入法不把自己的本职工作做好，非得弄些华而不实的副业，我也不知道这个产品的产品经理的脑回路是怎么长的。微软输入法很好用，以前被换掉的主要原因是因为shift切换中英文太容易误触，让我在vi编辑的时候总出问题。其实我现在发现习惯了自定义用ctrl-空格切换输入语言后，用起来也很爽，今后不会再安装其他的输入法了。

今天要谈的话题和删除百度输入法有些关系，不过其中关系可能要细品才能体会到。今天要聊的是前段时间十分热门的TDSQL创造新纪录的事情。

TDSQL打榜TPC-C是一个很有意义的事件，腾讯云数据库TDSQL以8.14亿的tpmC（每分钟处理事务数）和每tpmC成本1.27元人民币的评测成绩，实现了tpmC和性价比双榜世界第一。这是国产数据库在TPC-C榜单上的一次突破，也是对TDSQL在分布式架构设计和资源调度能力的一次全面验证。

上面这段话十分官方，不过应该是可以得到业内共识的，这一点不容置疑。TPC-C打榜是一家企业综合优化能力的体现，这不仅仅是单一数据库产品的成功，更体现了腾讯在超大并发量数据计算领域的技术能力。TDSQL打榜说明了TDSQL在类似BENCHMARK计算场景上的能力可以达到世界一流的水平了，类似的应用场景在我国也广泛存在，证券交易、银行核心交易、IOT实时处理，等等等等，目前这些领域也是国产化替代需求比较旺盛的领域。我想TDSQL的打榜成功，一定会为其在这些领域的销售带来利好。

最近朋友和我讨论的比较多的另外一个话题是，TDSQL登顶TPC-C，是不是意味着TDSQL已经成为国际上顶级的数据库产品了呢？对于这个问题没有一个确定的答案，不同的人可能有不同的看法。在这个语境下，有人可能会说，TDSQL在TPC-C榜单上的成绩是一个重要的里程碑，证明了它在OLTP场景下的优秀性能和可靠性，也展现了国产数据库的技术实力和创新能力。但是，要成为国际一流的商用数据库产品，还需要考虑其他方面，比如市场占有率、客户满意度、应用场景的多样性、生态系统的完善度等。TDSQL在这些方面还有很大的发展空间和潜力。

我们就以数据库领域最成功的商业公司Oracle来做个参考吧，Oracle在全球商用数据库占有率上超过30%，其17万全球员工中，售后服务支撑人员1.5万人，以29种语言提供服务。仅仅在中国，以Oracle数据库服务为业的技术人员就高达数千人。这才是我们应该对标的最主要的数字，没有完善的周边生态，一个数据库产品仅仅能够服务于有限的重点客户，那么很难说它是一款成功的商用数据库产品。

应用场景多样性覆盖也是衡量一款商用数据库产品是否优秀的关键评估指标，作为通用商用数据库产品，面对各种复杂的用户场景都能游刃有余，是一个最为基本的要求，也是最难做到的。还是以Oracle为对标对象，Oracle是一种传统的关系型数据库，具有成熟的技术和丰富的功能，支持多种操作系统和开发语言，拥有广泛的市场占有率和客户满意度。ORACLE在OLAP场景下也有较强的数据分析能力，支持多维数据模型和复杂的查询语法。ORACLE在安全性、稳定性、可维护性等方面也有较高的水准，可以适应各种复杂的业务需求和数据处理场景。而TDSQL目前主要针对简单的OLTP场景进行优化，对于复杂SQL的运行能力和OLAP场景还有待进一步提升。

在数据处理能力上，一款成功的商用数据库产品需要能够对数据进行快速的查询、分析、统计、计算等操作，以支持信息系统的功能，如MRP分解计算、APS排程优化、MES质量管理、ERP经营管理等。一款数据库只有能够在这些领域都能够游刃有余才算是成功的通用商用数据库产品，否则只能算是一个领域计算平台的一部分而已。TDSQL在这方面还任重道远，如果必须让用户在SQL编写上谨慎控制，那么将会给某些企业的应用研发带来困难。并不是所有的企业都能够像互联网企业一样开发高质量的应用，有些企业应用的开发商只会通过SQL来描述业务逻辑。

数据集成能力也是考验通用商用数据库的一个重要的方面，数据库需要能够实现不同信息系统之间的数据共享和交换，以提高信息的一致性和准确性，如PLM与ERP、ERP与MES、MES与CAPP等。这些系统很可能是异构的，而不是我们理想状态下，都用一套数据库或者一种数据库来替代。在这方面，我们的国产数据库与国外商用产品相比还有不小的差距。

在前面我们也提到了，生态系统的完善度是评估一款是数据库产品是否成功的关键因素。哪怕你的产品技术水平略低一点，TPMC低一些都不怕。因为TPMC 8.4亿是一种屠龙技，除了全球的少数几个顶级电商，恐怕再也找不到可以屠的龙了。

而相反，Oracle虽然没有那么高的TPMC指标，也没有那么便宜的成本，但是Oracle拥有庞大的生态系统，包括各种工具、中间件、框架、平台等，可以为用户提供全方位的解决方案和服务，再加上大量的第三方开发人员与服务团队，Oracle在这方面的优势是碾压性的。而TDSQL还需要完善自身的生态系统，增加与其他产品和服务的集成和协同能力，同时大力发展第三方生态。前阵子我们准备在D-SMART种对接TDSQL，找人要一些TDSQL的官方文档，最后我很失望。一个连官方文档都不认真去写的数据库产品，就很难谈第三方服务生态了，连最终用户想用好它都会有些费劲。

最后还是回到TDSQL打榜成功这件事，首先肯定这件事的进步意义，但是我们也需要看到商用数据库的成功不是打榜成功就可以了。练好内功，让用户能够低成本的用好这个数据库产品，那才是真正的成功。我想有一天有成千上万人靠着TDSQL吃饭了，那TDSQL真的就成功了。



## The significance of hitting the TPC-C leaderboard

Today I finally deleted the Baidu input method that I used for a year and switched back to the Microsoft input method. The main reason is that after I turned off a bunch of flashy cloud functions, the ability to input phrases and sentences became very weak. And the cloud functions often cause lagging or even freezing when the network is bad, making my hard work go down the drain. An input method that does not do its own job well, but has to do some flashy side businesses, I don’t know how the product manager’s brain circuit is. Microsoft input method is very easy to use, the main reason why it was replaced before was because shift switching between Chinese and English is too easy to misfire, making me always have problems when editing in vi. Actually, I found out that I got used to customizing ctrl-space to switch input languages, and it feels great to use. I will not install any other input methods in the future.

The topic I want to talk about today has something to do with deleting Baidu input method, but the relationship may need to be savored to appreciate. Today I want to talk about the very popular event of TDSQL creating a new record a while ago.

TDSQL hitting the TPC-C leaderboard is a very meaningful event. Tencent Cloud Database TDSQL achieved a test score of 814 million tpmC (transactions per minute) and a cost of 1.27 yuan per tpmC, achieving the world’s first double leaderboard for tpmC and cost performance. This is a breakthrough for domestic databases on the TPC-C leaderboard, and also a comprehensive verification of TDSQL’s distributed architecture design and resource scheduling capabilities.

The above paragraph is very official, but it should be able to get the consensus of the industry, which is unquestionable. TPC-C hitting the leaderboard is a reflection of a company’s comprehensive optimization capabilities, which is not only the success of a single database product, but also reflects Tencent’s technical capabilities in the field of ultra-large concurrent data computing. TDSQL hitting the leaderboard shows that TDSQL’s capabilities in similar BENCHMARK computing scenarios can reach the world-class level, and similar application scenarios are also widely available in China, such as securities trading, bank core trading, IOT real-time processing, etc., and these fields are also areas where domestic substitution demand is strong. I think TDSQL’s hitting the leaderboard success will definitely bring benefits to its sales in these fields.

Another topic that my friends and I have discussed more recently is, does TDSQL topping the TPC-C mean that TDSQL has become a top international database product? There is no definite answer to this question, and different people may have different opinions. In this context, some people may say that TDSQL’s performance on the TPC-C leaderboard is an important milestone, proving its excellent performance and reliability in the OLTP scenario, and also demonstrating the technical strength and innovation ability of domestic databases. But to become an internationally first-class commercial database product, other aspects need to be considered, such as market share, customer satisfaction, application scenario diversity, ecosystem completeness, etc. TDSQL still has a lot of room and potential for development in these aspects.

Let’s take Oracle, the most successful commercial company in the database field, as a reference. Oracle has more than 30% of the global commercial database market share, and among its 170,000 global employees, there are 15,000 after-sales service support personnel, providing services in 29 languages. Just in China, there are thousands of technical personnel who serve Oracle databases. This is the most important number we should benchmark, without a complete peripheral ecosystem, a database product can only serve a limited number of key customers, then it is hard to say that it is a successful commercial database product.

Application scenario diversity coverage is also a key evaluation indicator to measure whether a commercial database product is excellent. As a general-purpose commercial database product, it can cope with various complex user scenarios, which is a basic requirement and also the most difficult to achieve. Still taking Oracle as the benchmark object, Oracle is a traditional relational database, with mature technology and rich functions, supporting multiple operating systems and development languages, and has a wide market share and customer satisfaction. ORACLE also has strong data analysis capabilities in the OLAP scenario, supporting multidimensional data models and complex query syntax. ORACLE also has a high level of security, stability, maintainability, etc., and can adapt to various complex business requirements and data processing scenarios. TDSQL currently mainly optimizes for simple OLTP scenarios, and its running ability and OLAP scenarios for complex SQL need to be further improved.

In terms of data processing capabilities, a successful commercial database product needs to be able to perform fast query, analysis, statistics, calculation and other operations on data, to support the functions of information systems, such as MRP decomposition calculation, APS scheduling optimization, MES quality management, ERP management, etc. A database can only be considered a successful general-purpose commercial database product if it can cope with these fields, otherwise it can only be regarded as a part of a domain computing platform. TDSQL still has a long way to go in this regard. If users have to be careful in SQL writing, it will cause difficulties for some enterprises’ application development. Not all enterprises can develop high-quality applications like Internet enterprises, some enterprise application developers only use SQL to describe business logic.

Data integration capability is also an important aspect to test the general-purpose commercial database. The database needs to be able to achieve data sharing and exchange between different information systems, to improve the consistency and accuracy of information, such as PLM and ERP, ERP and MES, MES and CAPP, etc. These systems are likely to be heterogeneous, rather than our ideal state, using a set of databases or a type of database to replace. In this regard, our domestic databases still have a big gap compared with foreign commercial products.

We also mentioned earlier that the completeness of the ecosystem is a key factor to evaluate whether a database product is successful. Even if your product’s technical level is slightly lower, TPMC is lower, it doesn’t matter. Because TPMC 840 million is a dragon-slaying technique, except for a few top e-commerce companies in the world, I’m afraid there will be no more dragons to slay.

On the contrary, Oracle, although it does not have such a high TPMC indicator, nor such a low cost, but Oracle has a huge ecosystem, including various tools, middleware, frameworks, platforms, etc., which can provide users with a full range of solutions and services, plus a large number of third-party developers and service teams, Oracle’s advantage in this regard is crushing. A while ago we were preparing to dock TDSQL in D-SMART, looking for some official documents of TDSQL, and finally I was disappointed. A database product that doesn’t even bother to write official documents, it’s hard to talk about third-party service ecology, and even the end users will have some trouble using it.

Finally, let’s go back to the success of TDSQL hitting the leaderboard. First of all, we affirm the progressive significance of this matter, but we also need to see that the success of commercial databases is not just hitting the leaderboard. Practice your internal skills, let users use this database product at a low cost, that is the real success. I think one day there will be thousands of people who rely on TDSQL to make a living, then TDSQL will really succeed.
