---
layout: post
title: "快速入门Objective-C"
categories:iOS
- 
tags: iOS, Objective-C
- 


---

### 头文件.h

首先是头文件，后缀是以 .h头文件，这个文件定义了class的基本结构，有点类似一个类模板，定义class的结构信息


头文件部分

	#import <目录/头文件.h> //代表只引入系统库的类的头文件
	#import "目录/头文件.h" // 代表默认从当前路径下搜索是否存在对应的头文件，如果不存在，则从系统库里面

---	
### 属性 property
	
类定义以及成员变量定义部分，框架

	
	@property (getter=isFinished) BOOL finished;


+ `property`表示对象所拥有的属性

编译后自动产生Get和Set方法

	NSString *firstName = [somePerson firstName];
	

使用更方便的`Dot syntax`点语法等同于上面

	NSString *firstName = somePerson.firstName;
	

 `property`使用下划线前缀访问实例变量


也可以使用self效果一样

	- (void)someMethod {

 `property`自定义实例变量名称


	@implementation YourClass





>	@synthesize firstName;


 不用`property`定义实例变量








 `property`的属性


**nonatomic** 不是原子操作，不支持多线程访问安全，但是访问性能高，所以nonatomic比atomic访问更快


**readwrite** 默认的属性，表示可以对对象进行读和写，会生成对象相应的setter和getter方法




**unsafe_unretained** 一些 Cocoa and Cocoa Touch类无法使用weak引用时，可以使用`unsafe_unretained`代替











---
参考文献

[Object C初学学习笔记(1)](http://www.cnblogs.com/aigongsi/archive/2012/04/07/2436070.html)

[Programming With ObjectiveC](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/ProgrammingWithObjectiveC.pdf)

[IOS变量的property属性设置和意义总结](http://blog.csdn.net/pingchangtan367/article/details/14000315)

[@property](http://baike.baidu.com/view/5028218.htm)

[retain和copy的区别][retain和copy的区别]

[retain和copy的区别]:http://c.gzl.name/archives/339 "retain和copy的区别"