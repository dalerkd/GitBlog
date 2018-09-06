---
title: Java类的总结-自言自语
date: 2018-09-06 16:32:08
tags:
	- 总结
---
总结Java抽象类,接口和多态的相关语法及其语义
<!--more-->

# Java类的总结-自言自语
## 抽象类
```
abstract public class 类名{

abstract void study(){
//....
}

}
```
## 接口
```
public interface 接口名{
	//变量默认是 public static final 
	//方法默认是 public abstract
}
```

## 多态
```
Coin co;

void CreateBTC(){
co  = new BTC();
}

void CreateETC(){
co = new ETC();
}
void Work(){

co.A类工作();
co.B类工作();
co.C类工作();
}

////////////////////
CreateBTC();
Work();
CreateETC();
Work();


```
好处在保存这个co剩下的逻辑完全可以复用(看`Work()`).

**复用**这个概念很重要,它减少了BUG的产生,减少了加班,因为重复的代码导致理解困难和修改困难.




一个不太明显的例子见:
https://github.com/dalerkd/18.9.6.JavaPolymorphism
CoinManage负责根据不同的名字和需求操作Coin,进行操作.

Coin
|  \
BTC ETC