---
layout:     post
title:      "注定小众的魔法世界红宝石"
subtitle:   ""
date:       2017-04-16 19:22:53
author:     "YingJie"
header-img: "img/newblog.jpg"
header-mask: 0.3
navcolor:   "invert"
catalog:	true
timezone: CN
tags:
    - Ruby
    - 语言
    - 观点
---
### 对Ruby语言浅薄的理解

###### 前言：

Ruby作为一门非常有名的编程语言就不过多的介绍了，有人对她的魔幻着迷，有人对她的晦涩难懂极度厌恶，个人也常常使用Ruby做一些程序设计，可以说对Ruby的情感既有爱也有恨，作为一名千千万万程序员中的无名小卒，说说自己对Ruby的粗陋理解。码下这篇文章时我是瑟瑟发抖，还请大佬打脸轻一些。

###### 伊始

Ruby在松本行弘设计之初，考虑的就是以人为本，从人的角度出发，要符合程序员个人的心理感受。在当时（1993年）这样的思想可以说是相当大胆的，因为那个时候机器的硬件性能普遍低下，内存几个M，CPU主频不到半个G，硬/软盘容量和读写速度低的可怕，虽然现在的年轻一代没有经历过那个环境，但是还是可以想象的。

在大多数程序员都在想着优化程序内存，最大化提升机器效率和速度的时候，Ruby可以说是相当不受待见，不过历史上松本行弘不是第一个这样做的，1958年，约翰·麦卡锡在麻省理工学院发明了Lisp编程语言，自动内存管理和垃圾回收，可想而知，当时Lisp并没有实质性的应用开发价值。时至今日，Lisp依旧不温不火，但是Lisp成了一种思想，个人认为Lisp仅把动作和命令赋予在表格数据上就有了强悍的表现能力。

似乎有些跑题，接着说Ruby。

###### 提炼

松本行弘的创新其实并没有多少，但是他把一些优秀编程语言中的精华提炼出来，糅合成一家，这甚至比创新都有难度，Ruby启发语言来自：Ada、C++、CLU、Dylan、Eiffel、
Lisp、Perl、Python、Smalltalk甚至更多，其中借鉴最多的是Perl和smalltalk，Perl个人没有怎么使用过，不好评价，但是我知道Perl的语言密度极高，用字符指定行为在Perl中非常常见，有人把Perl写成天书，甚至Perl可以简洁到不可多一个字符或少一个字符，smalltalk的IDE非常强大，有人说它是一个自带IDE的编程语言。不熟悉就不过多的评论。Ruby也继承了Perl的这部分特点，所以才会有人说她是一个魔幻的语言，这种风格吸引着一部分人深入了解并学习应用，也挡住了不少的好奇的脚步，总体来说Ruby的学习曲线还是比较平缓的，经常有人建议编程初学者以Python为入门语言，其实Ruby更好，个人认为比Ruby更好的还有scheme，但是scheme毕竟太小众了，而且scheme的实用价值并不大。

###### 风格

接着说Ruby的魔幻

Ruby的魔幻特性注定Ruby只能是一门小众语言，由于Ruby中自由的表达方式，新手入门后看Ruby有关项目的源代码，会发现每个人都有自己的风格，这样并不利于初学者对高级知识的理解，如果这样还能坚持学习Ruby的人，就更是少部分人了，这样形成了Ruby社区的风格，大牛多，小白少，想入门的都徘徊在一个门槛前，少部分人踏过了门槛，大牛的数量提升缓慢。

###### Rails

但是怎么解释Ruby on Rails的热度和人数一直在比较高的地位呢？（Rails一般是创业公司使用，国内只有少部分公司的部分业务使用Rails，统计数据不包含中国地区的Rails使用者，这个年头在中国创业还不如炒房，一套一二线城市的房子价值就赶得上一个创业公司了，国内的环境使得创业只是口号，创业者寥寥）

###### DSL

这就引出Ruby的另一个现象了，Ruby的元编程能力非常强，Ruby诞生之初的语法就是为了嵌入式DSL而优化设计的，Ruby on Rails可以说是用Ruby语言开发的Web DSL，Rails诞生之初，犹如盘古开天辟地，当时，php还是old style，代码混杂html，net还停留在WebfoRms阶段，java还是with or widthout EJB中挣扎，Python还在用Zope这个先进的无法使用的东西，可以毫不夸张的说，Rails的诞生就如Iphone刚问世一样，Web开发有了革命性的创新，之后各种语言的各种Web开放框架或多或少的都在向Rails致敬，甚至影响了微软MVC开发的方式，感兴趣的可以搜索MonoRails，这里就不过多赘述了。

Ruby的DSL特性使得Ruby有了这样一种现象：某大牛写出一种DSL，如果这个DSL特别出色，就有很多人去使用这个DSL，Ruby也就会火一阵。但是并不是每个Ruby开发者都有能力写出优秀的DSL，所以Ruby会随着某些优秀DSL的出现而火一阵，接着热潮就会褪去。在技术圈，尤其是程序员这个特殊的群体，如果不是底层开发，不接受新知识，似乎就是落后，统计学的正态分布数据不会欺骗人群分布，Ruby注定小众，而且真正的Ruby开发者高手居多。

而且近几年前端的大热，JS MVC框架的路越来越广，已经不用太依赖服务端模板，ES语法也在逐渐改进javascRipt这门先天设计不足的语言，微服务，后端提供API方式逐渐流行，Rails的优势也小了一些，但是不可否认，如果还是开发Web项目，Rails依然是最佳选择。

之前在一个Ruby交流群中有人说Ruby将来会一直低迷，Ruby在数据分析，人工智能，科学计算方面根本没有好用的gem。我认为Ruby是否低迷不一定，同样作为图灵完备语言，只要想，都是可以做的（商业公司要考虑成本问题，而且商业公司居多），Ruby在其它方面确实落后Python很多，而且应该没有追赶Python的可能，未来Ruby的应用领域应该是垂直细分地方（有些像创业者的口气），在某些有特殊要求的地方用自己的强大DSL能力给开发者一个简单的解决方案。

从语言的角度也可以这样看，Python在语言密度和语义表达方面做到了一个平衡，才会有这么多的人去使用，而Ruby的语言密度和语义表达都比Python要高一些，受众小也是自然的。

另外Metasploit真好用。

以上是个人浅薄感想，如果有不正确的地方还请提出。