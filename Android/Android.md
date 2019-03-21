# Android

1.equals和hashcode的区别，对象的内存地址会变化吗？equals相等的对象会一直相等吗为什么？
为什么重写equals必须重写hashcode？ == 和equals的区别？int 128 = intenger 128吗？
  > 1，equals是判断两个对象是否相等。
  <br>2，Hashcode返回一个对象的哈希码
  <br>3，对象的内存地址不会发生变化。
  <br>4,equals相等的对象如果没有重写equals方法表示两个对象一直相等。
  <br>5，因为要保证equals和hashcode一致性。
  <br>6，如果没有重写equals方法，和==是一样的，另外==比较基本类型的值。
  <br>7，int 128==Integer 128，因为Integer会自动拆箱
  


2.hashmap的内部结构，他与linkedhashmap的区别，linkedhashmap的实现原理
>1),HashMap内部使用哈希表加上链表实现，最新的加上了红黑树实现。
 <br>2),LinkedHashMap使用哈希表和双向循环链表实现，优势是能保持存储时的顺序。
 <br>3),LinkedHashMap的实现原理是比HashMap的链表中增加了一个before和一个after。


3.java的泛型了解吗？具体怎么使用？extend和super了解吗？ 有什么区别
>1),Java泛型是限定类型用的，具体比如在一个List中加入一个泛型，该List的存储这个类型。
 <br>2),extends表示上届，super表示下届。一般extend用在消费者中，super用在生产者中。



4.安卓的虚拟机是什么？特性是什么？虚拟机怎么把包文件安装到手机，具体怎么操作
>1),Android的虚拟机有art和Dalvik
 <br>2),.....gguyguyguy



5.安卓中虚拟机的回收算法是什么？ 怎么回收的？

6.用过数据库吗？ 怎么用的？假如新版本老的数据库字段删除了，怎么安全升级数据库？
>1),升级数据库需要重写升级数据库方法onUpdate,如果新版本中老的数据库字段被删除了，<br>
可以通过merge数据库的方法来生成新的数据库，重建新的数据库，读取老数据库的内容，插入到新的数据库中。

7.线程同步知道吗？怎么实现的？线程的内存共享是什么？
>1),线程同步使用关键字synchronized<br>
 2),Java同一个进程之间的内存本来就是共享的，所以不存在内存共享的问题，只是要注意<br>
 在共享内存的时候要保证线程的安全性。

8.handler知道吗？message消息怎么排序的？ message怎么取出来？handler会导致内存泄漏吗？ 为什么
>1),Message通过Qenue的方式排序，即先到先得，消息从Looper.loop里面取出来的，因为Handler持有当前类的引用，
生命周期和当前的线程又不是一样的，所以会导致内存泄漏。

9.activity的启动流程知道吗？ activity是new出来的吗？activitythread是具体干啥的？

10.okhttp知道吗，具体源码是怎么样的？取消网络请求做过吗？如果取消的时候，网络请求已经成功了怎么办？网络缓存做过吗？ 缓存什么时候生效？项目中有用过其它的缓存吗？

11.进程间通信知道吗？ aidl的两个重要方法知道是啥？service的startcommoned的返回值了解吗？具体是什么意思？

12.广播有哪几种？ 如果广播做耗时操作怎么办？ 假如子线程处理一个60s的子任务，会有什么影响？

13.8.0 、9.0的适配知道吗？

14.方法重载和重写，假如一个方法的返回值不同，方法名和参数相同，是重载吗？
>1),不是重载。

15.fragment的getactivity方法为空遇到过吗？怎么解决的

16.webview的js调用安卓及安卓调用js方法，具体操作是什么？

17.怎么在手机中设置一个app的可使用内存？

18.热更新用的啥？  源码了解吗？  大致说说

19.http和https的区别？对称加密和非对称加密、加密是在服务端还是客户端？ 怎么确保证书的可靠性？

20.设计模式用过吗？手写单例模式

21.有哪几种动画、那种动画可以在view移动后实现点击事件，具体是怎么实现的

22.window和activity的关系

23.用过反射吗？具体怎么实现的

24.arraymap知道吗  具体怎么实现的？ 为什么intent传值用bundle不用hashmap

25.string和stringbuffer的区别
