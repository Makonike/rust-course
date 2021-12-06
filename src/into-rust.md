# 进入Rust编程世界

## 一、Rust发展历程

Rust 最早是 Mozilla 雇员 Graydon Hoare 的一个个人项目，从 2009 年开始，得到了 Mozilla 研究院的支助，2010 年项目对外公布。2010 ～2011 年间实现的自举。从此以后，Rust 经历了巨大的设计变化和反复（历程极其艰辛），终于在 2015 年 5 月 15日发布了 1.0 版。在这个研发过程中，Rust 建立了一个强大活跃的社区，形成了一整套完善稳定的项目贡献机制（Rust能够飞速发展，与这一点密不可分）。Rust 现在由 [Rust项目开发者社区](https://github.com/rust-lang/rust)维护。

大家可能疑惑Rust为啥用了这么久才到1.0版本？与之相比，Go语言2009年发布，却在2012年仅用3年就发布了1.0版本。首先是因为Rust语言特性较为复杂，因此需要全盘考虑的问题非常多；其次，Rust当时的参与者太多了，七嘴八舌的声音也很多，导致了众口难调，而Rust开发团队又非常重视社区的意见 ；最后，一旦1.0快速发布，那么后续大部分语言特性就无法再修改，对于有完美强迫症的Rust开发者团队来说，某种程度上的不完美是不可接受的。因此，Rust语言用了足足6年时间，才发布了尽善尽美的1.0版本。

## 二、使用现状

一般来说，一门编程语言能在某一年成为全世界最受欢迎的语言，那锣鼓喧天、昂首挺胸都是少不了的，没办法，能从全世界这么多编程语言中脱颖而出成为最受欢迎的语言，属实困难。可是有一门语言，它从发布1.0版本开始，连续6年成为了全世界最受欢迎的语言，是的，它就是Rust,这不，2021年又成为最受欢迎的语言了。

你可能会想，既然这么受欢迎，那肯定使用很广吧？可惜现实给了我们重重一击：在国外，Rust尚且还行，在各大公司的基础服务和底层都屡见身影，在github上也算是呼风唤雨，可是到了国内，说句不好听的，能听说过Rust大名的，已经算百里挑一的优秀了，就业环境更是糟糕。

如何改变这一切？这就是[Rust编程学院](https://college.rs)想做的事情，通过大家一起的努力，达成以下目标：
1. 输出**成体系的学习教程**，大幅降低Rust的学习和使用难度
2. 打造**至少一个全民级项目**，提升Rust在国内知名度
3. 建立一个持续活跃的社区，为Rust用户提供一个交流、解惑的平台

其中第一点是尤为重要的，只有一套成体系的学习教程，才能让用户快速上手并且喜欢上Rust语言，一旦粉丝效应形成，那么Rust在国内的影响力就会在大家的自发宣传下迅速提升。

#### 部分主要使用者

- AWS从2017年开始就用Rust实现了它们的无服务器计算平台： AWS Lambda 和 AWS Fargate, 并且用Rust重写了Bottlerocket OS和AWS Nitro系统，这两个是弹性计算云(EC2)的重要服务
- Cloudflare也是Rust的重度用户，DNS、无服务计算、网络包监控等灯
- Dropbox的底层存储服务完全由Rust重写，达到了数万PB的规模
- Google除了在安卓系统的部分模块中使用Rust外，还在它最新的操作系统fuchsia中重度使用Rust
- Facebook使用Rust来增强自己的网页端、移动端和API服务的性能，同时还写了Hack编程语言的虚拟机部分模块
- Microsoft使用Rust为Azure平台实现了一些组件，其中包括IoT服务的安全守护服务
- githu和npmjs.com，使用Rust提供了高达每天13亿次的npm包下载数量
- Rust目前已经成为全世界区块链平台的首选开发语言
- Tidb，国内最有名的开源分布式数据库
- 国内高频交易服务

类似的还有很多，总之Rust的发展态势非常喜人，生态发展也异常迅速，颇有燎原之火之势。


#### Github

Github上的Rust项目可以在这里查看: https://github.com/topics/rust?l=rust，里面的项目是按照star数降序排列。

## 三、适用人群

Rust 因多种原因适用于很多开发者。让我们讨论几个最重要的群体。

### 开发者团队

由于Rust语言拥有异常强大的编译器和语言特性，因此Rust的代码天然就会比其它语言有更少的Bug，同时Rust拥有非常完善的工具链、最好的包管理工具，这些叠加在一起，决定了Rust非常适合大型开发者团队的协作开发。

也许Rust在开发速度上不是最快的，但是从开发 + 维护的角度来看，这个成本绝对是各个语言中最小的之一，当然如果你的公司就追求做出来能用就行，那Rust确实不太适合。

### 学生

Rust的语言特点决定了它天然就跟底层系统很亲和，通过Rust你能学到操作系统、网络等计算机原理，现在不少名校都引入了Rust作为计算机系统课程学习的重要组成部分，例如MIT对Rust的使用就非常广泛。

同时Rust具有一个友善、活跃的社区，社区中的人非常热衷于为大家解答问题，因此也很适合学生学习一门新的恶语言。

### 公司

数以百计的公司，无论规模大小，都在生产中使用Rust来完成各种任务。这些任务包括命令行工具、web 服务、DevOps 工具、嵌入式设备、音视频分析与转码、加密货币（cryptocurrencies）、生物信息学（bioinformatics）、搜索引擎、物联网（internet of things, IOT）程序、机器学习、云计算等，甚至还包括 Firefox 浏览器的大部分内容。

### 开源开发者

Rust连续6年成为全世界最受欢迎的语言，这个就是来自于开源社区的厚爱，在github上，Rust目前各种类型的开源项目都非常火，同时有很多领域还等着大家去填补空白，这些都意味着在开源世界扬名立万的机会。

为一门成熟的语言锦上添花，远不如为一门新语言雪中送炭，你能获得比在其他语言更多的star和名气。


### 重视速度和稳定性的开发者

速度分为两种：运行速度和开发速度。

开发速度方面，Rust拥有和C、C++几乎相当的性能，甚至由于Rust的各种零开销抽象以及安全的编程方式，你能轻松写出和那些优化过后的C++代码一样甚至更高的性能: [ripgrep](https://github.com/BurntSushi/ripgrep)就是很典型的例子。

同时，在你熟悉Rust后，由于强大的编译器、标准库文档、语言高级特性等，Rust能让你拥有不属于其它静态语言的开发速度，同时大幅减少后期维护成本。


最后，Rust语言不仅仅适用于这些人群，这些列出来的只是从Rust中最受益的人群。总的来说Rust的目标是消除数十年来程序员不得不做的权衡：安全 **与** 生产力，速度 **与** 工程性。

请跟随本书的脚步去尝试下Rust，看看这个选择是否适合你。

## 四、Rust语言版本更新

与其它语言相比，Rust的更新迭代较为频繁(得益于精心设计过的发布流程以及Rust语言开发者团队管理)：
- 每6周发布一个迭代版本
- 2-3年发布一个新的大版本：Rust 2018 edition，Rust 2021 edtion

好处在于，可以满足不同的用户群体的需求：
- 对于活跃的Rust用户，他们总是能很快获取到新的语言内容，毕竟，尝鲜是技术爱好者的共同特点:)
- 对于一般的用户，edition的发布会告诉这些用户：Rust语言相比上次大版本发布，有了重大的改进，值得一看
- 对于Rust语言开发者，可以让他们的工作成果更快的被世人所知，不必锦衣夜行


好了，相信大家听了这么多Rust的优点，已经迫不及待想要开始学习旅程，OK，let's go.