反射面试题:https://blog.csdn.net/qq_37875585/article/details/89340495

netty面试题：https://www.cnblogs.com/duan2/p/8819910.html

kafka如何保证数据的顺序消费、

kafka的数据重复消费怎么处理、

如何保证kafka中数据不丢失？



HashMap的数据结构是设么样的？

hashMap中，hash算法的作用？

描述一下hashMap，put操作的流程？



https://blog.csdn.net/feiBlog/article/details/85397287





# 美团篇（33道）

1. 了解SOA，微服务吗？

2. 分布式系统如何负载均衡？如何确定访问的资源在哪个服务器上？

    负载均衡将请求派发到网络中的一个或多个节点上进行处理。 
    硬件负载均衡，即通过在服务器间安装专门的硬件来进行负载均衡工作 
    软件负载均衡，通过服务器上安装的软件来对请求进行分配派发。

    **负载均衡策略**:轮询/随机/最小响应时间/一致性哈希/粘滞链接

3. 设计一个分布式负载均衡缓冲系统，如何快速定位到是那个服务器？

    使用key分段、一致性hash。

4. 如何保证缓冲区和数据库之间的强一致性？

    https://blog.csdn.net/qianfeng_dashuju/article/details/95348565

5. HashMap高并发情况下会出现什么问题？

    - HashMap死循环，造成CPU100%负载

        1.8已经解决

    - 触发fail-fast

        一个线程利用迭代器迭代时，另一个线程做插入删除操作，造成迭代的fast-fail。

6. 说一说在浏览器中输入一个url后，直到浏览器显示页面的过程中发生了什么？

    1、DNS解析，将域名解析为IP地址；

    2、浏览器与服务器建立TCP连接（三次握手）；

    3、浏览器向服务器发起HTTP请求；

    4、服务器接收请求并响应，返回相应的HTML文件；

    5、浏览器接收从服务器端返回的数据，并进行页面渲染。

7. 字符串中句子的反转（比如ABC DEF，输出DEF ABC）

    split(" ")后i--循环。

8. 给任意二叉树的所有结点加next指针

9. 用过反向代理吗？

10. 进程间共享内存的方式有哪些？

11. linux下如何查看网络端口状态，如何查看内存使用情况？

12. ConcurrentHashMap如何扩容？

13. 知道java的异常吗？

14. 运行时异常如果不处理会怎么样？应该怎么处理运行时异常？

15. 写代码：给你5000万个int，求出前1000个最大的数，有2G内存。

    优先队列实现，一个大小1000的数组，用来维护一个小顶二叉堆。删除最小的元素（下标为1），插入一个新元素如此往复。

16. 给你n个不重复的整数，随机找出m个不重复的整数，要求时间和空间复杂度都是O(m)。

17. 对于SQL慢查询的优化？

18. 用过哪些容器？

19. 用过动态代理吗？

20. 说说深入理解JVM中印象最深刻的章节

21. 堆和栈中存的是什么？static修饰的遍历存在哪里？

22. 说说《Effective Java》中你印象最深的三条和你的理解

23. 你觉得你哪一块只是最熟悉

24. 那你说说HashMap的内部实现；

25. HashMap是线程安全的吗？

26. 那ConcurrentHashMap内部是如何实现的？每个segment是个什么数据结构？

27. 你的项目中用到哪些技术？

28. 说说你用了它的什么？

29. Spring的优点？Spring AOP的原理？Spring如何实现解耦合？

30. 对链表了解吗？说说他们的区别？

31. 会做链表两个结点的交换吗？

32. 再写一个，给你一个链表和一个整数k

33. 说说mybatis配置了xml过后是如何完成数据库操作的？

    ParameterHandler：处理SQL的参数对象

    ResultSetHandler：处理SQL的返回结果集

    StatementHandler：数据库的处理对象，用于执行SQL语句

    Executor：MyBatis的执行器，用于执行增删改查操作

# Redis

1. redis 和 memcached 什么区别？
2. 为什么高并发下有时单线程的 redis 比多线程的memcached 效率要高？
3. redis 主从复制如何实现的？
4. redis 的集群模式如何实现？
5. redis 的 key 是如何寻址的？
6. 使用 redis 如何设计分布式锁？说一下实现思路？使用 zk 可以吗？如何实现？这两种有什么区别？
7. 知道 redis 的持久化吗？底层如何实现的？有什么优点缺点？
8. redis 过期策略都有哪些？LRU 算法知道吗？写一下 java 代码实现？
9. 缓存穿透、缓存击穿、缓存雪崩解决方案？
10. 在选择缓存时，什么时候选择 redis，什么时候选择 memcached
11. 缓存与数据库不一致怎么办？
12. 主从数据库不一致如何解决
13. Redis 常见的性能问题和解决方案
14. Redis 的数据淘汰策略有哪些？
15. Redis 当中有哪些数据结构？
16. 假如 Redis 里面有 1 亿个 key，其中有 10w 个 key 是以某个固定的已知的前缀开头的，如果将它们全部找出来？

# 拼多多篇（40道）

1. 给一个函数，返回 0 和 1，概率为 p 和 1-p，请你实现一个函数，使得返回 01 概率一样。
2. 10 亿个 url，每个 url 大小小于 56B，要求去重，内存 4G。
3. 把一个 bst 转化成一个双向链表。
4. http 和 https 区别，https 在请求时额外的过程，https 是如何保证数据安全的。
5. IP 地址子网划分。
6. POST 和 GET 区别。
7. 硬链接和软连接区别。
8. DNS 解析过程。
9. kill 用法，某个进程杀不掉的原因（进入内核态，忽略 kill 信号）。
10. linux 用过的命令。
11. 系统管理命令（如查看内存使用、网络情况）。
12. 管道的使用。
13. grep 的使用，一定要掌握，每次都会问在文件中查找。
14. shell 脚本。
15. find 命令。
16. awk 使用。
17. Linux 下的一些指令，（进程id）， （进程 id），（进程id），?（上一条命令退出时状态），怎么查看进程，按照内存大小，CPU 占用排序等等。（大写 M 和大写 P）。
18. http 的 get 和 post 方法。
19. 介绍下你所了解的 epoll。
20. 数据库 sql 的了解程度。
21. 项目中遇到的问题，自己咋解决的等等。
22. 手写一个全排列。
23. B树和B+树。
24. 介绍一下 Hash，怎么解决冲突。
25. 进程间的通信，共享内存方式的优缺点。
26. 说下你平时看的一些技术博客，书籍。
27. linux 下的一些指令。
28. 工作中你觉得最不爽的事情是什么。
29. 说下你的优缺点。
30. 有没有想过去创业公司。
31. 写个 strcpy 函数。
32. 说说你自己的性格。
33. 给你一个系统（面试官好像是无人车部门的），后台的逻辑已经实现了，但是前端加载很慢，怎么检测。
34. 以后可能要学习很多新技术，你怎么看。
35. 项目中遇到的困难（提前想好，并且把实现或者优化方法说清楚）。
36. 系统的量级、pv、uv 等。
37. 应对高并发的解决办法（分布式）。
38. 在项目中主要负责了哪些工作。
39. nginx 的负载均衡。
40. 分布式缓存的一致性，服务器如何扩容（哈希环）。



# 网易篇（72道）

1. HashMap的源码，实现原理，JDK8中对HashMap做了怎样的优化。
2. HaspMap扩容是怎样扩容的，为什么都是2的N次幂的大小。
3. HashMap，HashTable，ConcurrentHashMap的区别。
4. 极高并发下HashTable和ConcurrentHashMap哪个性能更好，为什么，如何实现的。
5. HashMap在高并发下如果没有处理线程安全会有怎样的安全隐患，具体表现是什么。
6. java中四种修饰符的限制范围。
7. Object类中的方法。
8. 接口和抽象类的区别，注意JDK8的接口可以有实现。
9. 动态代理的两种方式，以及区别。
10. Java序列化的方式。
11. 传值和传引用的区别，Java是怎么样的，有没有传值引用。
12. 一个ArrayList在循环过程中删除，会不会出问题，为什么。
13. @transactional注解在什么情况下会失效，为什么。
14. B+树
15. 快速排序，堆排序，插入排序（其实八大排序算法都应该了解
16. 一致性Hash算法，一致性Hash算法的应用
17. JVM的内存结构。
18. JVM方法栈的工作过程，方法栈和本地方法栈有什么区别。
19. JVM的栈中引用如何和堆中的对象产生关联。
20. 可以了解一下逃逸分析技术。
21. GC的常见算法，CMS以及G1的垃圾回收过程，CMS的各个阶段哪两个是Stop the world的，CMS会不会产生碎片，G1的优势。
22. 标记清除和标记整理算法的理解以及优缺点。
23. eden survivor区的比例，为什么是这个比例，eden survivor的工作过程。
24. JVM如何判断一个对象是否该被GC，可以视为root的都有哪几种类型。
25. 强软弱虚引用的区别以及GC对他们执行怎样的操作。
26. Java是否可以GC直接内存。
27. Java类加载的过程。
28. 双亲委派模型的过程以及优势。
29. 常用的JVM调优参数。
30. dump文件的分析。
31. Java有没有主动触发GC的方式（没有）。
32. Java实现多线程有哪几种方式。
33. Callable和Future的了解。
34. 线程池的参数有哪些，在线程池创建一个线程的过程。
35. volitile关键字的作用，原理。
36. synchronized关键字的用法，优缺点。
37. Lock接口有哪些实现类，使用场景是什么。
38. 可重入锁的用处及实现原理，写时复制的过程，读写锁，分段锁（ConcurrentHashMap中的segment）。
39. 悲观锁，乐观锁，优缺点，CAS有什么缺陷，该如何解决。
40. ABC三个线程如何保证顺序执行。
41. 线程的状态都有哪些。
42. sleep和wait的区别。
43. notify和notifyall的区别。
44. ThreadLocal的了解，实现原理。
45. 常见的数据库优化手段索引的优缺点，什么字段上建立索引数据库连接池。
46. durid的常用配置。
47. TCP，UDP区别。三次握手，四次挥手，为什么要四次挥手。
48. 长连接和短连接。
49. 连接池适合长连接还是短连接。
50. 观察者模式代理模式单例模式，有五种写法，可以参考文章单例模式的五种实现方式可以考Spring中使用了哪些设计模式
51. 分布式事务的控制。
52. 分布式锁如何设计。
53. 分布式session如何设计。
54. dubbo的组件有哪些，各有什么作用。
55. zookeeper的负载均衡算法有哪些。
56. dubbo是如何利用接口就可以通信的。
57. redis和memcached的区别。
58. redis支持哪些数据结构。
59. redis是单线程的么，所有的工作都是单线程么。
60. redis如何存储一个String的。
61. redis的部署方式，主从，集群。
62. redis的哨兵模式，一个key值如何在redis集群中找到存储在哪里。
63. redis持久化策略。
64. SpringMVC的Controller是如何将参数和前端传来的数据一一对应的。
65. Mybatis如何找到指定的Mapper的，如何完成查询的。
66. Quartz是如何完成定时任务的。
67. 自定义注解的实现。
68. Spring使用了哪些设计模式。
69. Spring的IOC有什么优势。
70. Spring如何维护它拥有的bean。
71. 一些较新的东西JDK8的新特性，流的概念及优势，为什么有这种优势。
72. 区块链了解如何设计双11交易总额面板，要做到高并发高可用

# 蚂蚁金服篇（39道）

1. HashMap&ConcurrentHashMap
2. 再谈谈一致hash算法？
3. 乐观锁&悲观锁？
4. 可重入锁&Synchronize？
5. 事务四大特性？
6. 事务的二段提交机制?
7. 聚簇索引&非聚簇索引？
8. 用自己的实践经历说一下索引的使用场景(说一个就要举一个例子)？
9. 当前读&快照读？
10. 类加载过程？
11. 双亲委派机制及使用原因？
12. 说说GC算法？
13. Http&Https的区别
14. Https的加密方式
15. 线程池的核心参数和基本原理
16. 线程池的调优策略
17. 说说自己参与的项目，技术难度在哪里？
18. Collections.sort底层排序方式？
19. 排序稳定性？
20. 具体场景的排序策略？
21. Http请求过程，DNS解析过程
22. 三次握手四次挥手
23. 简述线程池和并发工具的使用？
24. 数据库索引原理
25. 频繁老年代回收怎么分析解决
26. Spring IOC、AOP？
27. 讲讲SpringBoot/SpringCloud的一些应用？
28. 阻塞队列不用java提供的自己怎么实现，condition和wait不能用
29. 拥塞窗口讲一讲，为什么要用慢启动算法
30. 负载均衡的原理？
31. Redis的数据一致性问题（分布式多节点环境 & 单机环境）？
32. 讲讲docker容器？
33. 如何实现何高并发下的削峰，限流？
34. 项目中用的中间件的理解(Dubbo、MQ、Redis、kafka、zk)
35. 服务器雪崩是怎么造成的？之前有这样的经历吗？怎么防备？
36. 高并发架构的设计思路
37. 以前项目中遇到的最大问题和解决策略
38. 生活中遇到的最大的挫折
39. 生活中遇到的最大的令你最有成就感的事情

# 多线程

1. 现在有 T1、T2、T3 三个线程，你怎样保证 T2 在 T1 执行完后执行，T3 在 T2 执行完后执行？
2. 在 Java 中 Lock 接口比 synchronized 块的优势是什么？你需要实现一个高效的缓存，它允许多个用户读，但只允许一个用户写，以此来保持它的完整性，你会怎样去实现它？
3. 在 java 中 wait 和 sleep 方法的不同？
4. 用 Java 实现阻塞队列
5. 用 Java 写代码来解决生产者——消费者问题
6. 用 Java 编程一个会导致死锁的程序，你将怎么解决？
7. 什么是原子操作，Java 中的原子操作是什么？
8. Java 中的 volatile 关键是什么作用？怎样使用它？在 Java 中它跟 synchronized 方法有什么不同？
9. 什么是竞争条件？你怎样发现和解决竞争？
10. 你将如何使用 threaddump？你将如何分析 Thread dump？
11. Java 中你怎样唤醒一个阻塞的线程？
12. 为什么我们调用 start()方法时会执行 run()方法，为什么我们不能直接调用 run()方法？
13. 在 Java 中 CycliBarriar 和 CountdownLatch 有什么区别？
14. 什么是不可变对象，它对写并发应用有什么帮助？
15. 你在多线程环境中遇到的常见的问题是什么？你是怎么解决它的？
16. 使用synchronized修饰静态方法和非静态方法有什么区别。
17. 简述ConcurrentLinkedQueue和LinkedBlockingQueue的用处和不同之处。
18. 导致线程死锁的原因？
19. 怎么解除线程死锁。
20. 非常多个线程（可能是不同机器），相互之间需要等待协调，才能完成某种工作，问怎么设计这种协调方案。
21. 用过读写锁吗，原理是什么，一般在什么场景下用。
22. 开启多个线程，如果保证顺序执行，有哪几种实现方式，或者如何保证多个线程都执行完再拿到结果。
23. 延迟队列的实现方式，delayQueue和时间轮算法的异同。

# JVM

1. JVM 内存分哪几个区，每个区的作用是什么？
2. 如和判断一个对象是否存活？(或者 GC 对象的判定方法)
3. 简述 Java 垃圾回收机制？
4. Java 中垃圾收集的方法有哪些？
5. Java 内存模型
6. Java 类加载过程？
7. 简述 Java 类加载机制？
8. 类加载器双亲委派模型机制？
9. 什么是类加载器，类加载器有哪些？
10. 简述 Java 内存分配与回收策率以及 Minor GC 和Major GC？

# Spring全家桶（SpringCloud、Docker）

**Spring**

1. 不同版本的 Spring Framework 有哪些主要功能？
2. 什么是 Spring Framework？
3. 列举 Spring Framework 的优点。
4. Spring Framework 有哪些不同的功能？
5. Spring Framework 中有多少个模块，它们分别是什么？
6. 什么是 Spring 配置文件？
7. Spring 应用程序有哪些不同组件？
8. 使用 Spring 有哪些方式？
9. 什么是 Spring IOC 容器？
10. 什么是依赖注入？
11. spring 中有多少种 IOC 容器？
12. 什么是 spring bean？
13. spring 提供了哪些配置方式？
14. spring 支持集中 bean scope？
15. spring bean 容器的生命周期是什么样的？
16. 什么是 spring 的内部 bean？
17. 什么是基于注解的容器配置？
18. 如何在 spring 中启动注解装配？
19. spring DAO 有什么用？
20. spring JDBC API 中存在哪些类？
21. 列举 spring 支持的事务管理类型
22. 什么是 AOP？
23. 什么是 Aspect？
24. AOP 有哪些实现方式？
25. Spring AOP and AspectJ AOP 有什么区别？

**Docker**

1. 什么是Docker？
2. 如何使用Docker构建与环境无关的系统？
3. Dockerfile中的命令COPY和ADD命令有什么区别？
4. 什么是Docker镜像？
5. 什么是Docker容器？
6. 什么是Docker Hub？
7. Docker容器在任何给定时间点可以处于什么状态？
8. 有没有办法识别Docker容器的状态？
9. Dockerfile中最常见的指令是什么？
10. 什么类型的应用程序 - 无状态或有状态更适合Docker容器？
11. Docker Image和Layer有什么区别？
12. 什么是虚拟化？
13. 什么是管理程序？
14. 什么是Docker Swarm？
15. 你将如何监控生产中的Docker？

## 美团-金融

### 一面

JVM

- JVM的结构
- 新生代和老年代的垃圾回收算法
- 虚拟机栈和本地方法栈的区别
- 类信息会加载到JVM哪个区域

JAVA基础

- HashMap 和 ConcurrentHashMap 的区别
- final 的作用，加在变量、方法、类的区别
- 新建一个 string 会创建几个对象
- 哪些类是线程安全的
- 线程池的参数;为什么需要超出最大容量的策略
- ThreadLocal了解吗

Spring

- AOP的实现原理
- @Autowired和@Resource的区别
- 什么情况下会用@Resource

MySQL

- B+树的优势
- 悲观锁和乐观锁了解吗
- 数据库如何实现乐观锁

设计模式

- 工厂模式怎么理解
- 单例模式有哪几种实现方式
- 懒汉和饿汉的区别，懒汉的缺点

算法

- 反转链表

### 二面

JAVA基础

- HashMap 和 ConcurrentHashMap 的区别
- hash 冲撞怎么办？如何 rehash
- HashMap 的遍历方式
- 为什么 HashMap 是线程不安全的
- volatile 和 synchronized 的区别

Spring

- SpringBoot 的优势
- SpringMVC 的 MVC 指什么？好处呢

Redis

- 主从结构了解吗
- 宕机之后如何恢复数据

消息队列

- rabbitmq 和 kafka 的区别
- rabbitmq 如何保证事务
- 消息队列的优势