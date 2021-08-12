## 单例(Singleton)模式

### 定义

一个类只有一个实例，且该类能自行创建这个实例的一种模式。

### 优缺点

优点：

- 内存中只有一个实例，减少内存的开销
- 避免对资源的多重占用
- 设置为全局访问点，可以优化和共享资源的访问

缺点：

- 没有接口，扩展困难，违背了开闭原则
- 不利于调试
- 功能代码通常写在一个类中，如果功能设计不合理，则容易违背单一职责原则

### 应用场景

- 需要频繁创建的类
- 只要求生成一个对象的场景
- 类创建实例时占用资源较多，或实例化耗时较长，且经常使用
- 类需要频繁实例化，同时生成的对象又频繁被销毁
- 频繁访问数据库或文件的对象
- 对象需要被共享的场景

### 实现

1. 懒汉式
   
   ```
   public class LazySingleton {
       private static volatile LazySingleton instance = null;
       private LazySingleton(){}
       public static synchronized LazySingleton getInstance() {
           if(instance == null) {
               instanc = new LazySingleton();
           }
           return instance;
       }
   }
   ```

   优点: 线程安全

   缺点：影响性能、消耗更多的资源

2. 饿汉式
   
   ```
   public class HungrySingleton{
       private static final HungrySingleton instance = new HungrySingleton();
       private HungrySingleton() {}
       public static HungrySingleton getInstance() {
           return instance;
       }
   }
   ```

### 单例模式在JDK和Spring源码中的应用