## 软件设计原则(Software Design Principle)

降低对象之间的耦合，增加程序的可复用性、可扩展性和可维护性。

|原则|英文名称|内容|目的|
|--|--|--|--|
|开闭原则|Open Closed Principle(OCP)|对扩展开放，对修改关闭|降低维护带来的新风险|
|依赖倒置原则|Dependency Inversion Principle(DIP)|高层不应该依赖低层，要面向接口编程|更利于代码结构的升级扩展|
|单一职责原则|Single Responsibility Principle(SRP)|一个类只干一件事，实现类要单一|便于理解，提高代码的可读性|
|接口隔离原则|Interface Segregation Principle(ISP)|一个接口只干一件事，接口要精简单一|功能解耦，高聚合、低耦合|
|迪米特法则|Law of Demeter(LoD)/Least Knowledge Principle(LKP)|不该知道的不要知道，一个类应该保持对其它对象最少的了解，降低耦合度|只和朋友交流，不和陌生人说话，减少代码臃肿|
|里氏替换原则|Liscov Substitution Principle(LSP)|不要破坏继承体系，子类重写方法功能发生改变，不应该影响父类方法的含义|防止继承泛滥|
|合成复用原则|Don't Repeat Yourself(DRY)|尽量使用组合或者聚合关系实现代码复用，少使用继承|降低代码耦合|