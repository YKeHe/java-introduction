# 方法
## 参数绑定
1. 基本类型参数的绑定
```java
Person p = new Person();
int n = 15; // n的值为15
p.setAge(n); // 传入n的值
System.out.println(p.getAge()); // 15
n = 20; // n的值改为20
System.out.println(p.getAge()); //输出:15
```
2. 引用类型参数的绑定
```java
Person p = new Person();
String[] fullname = new String[] { "Homer", "Simpson" };
p.setName(fullname); // 传入fullname数组(引用类型fullname)
System.out.println(p.getName()); // "Homer Simpson"
fullname[0] = "Bart"; // fullname数组的第一个元素修改为"Bart"
System.out.println(p.getName()); //输出:Bart Simpson
```
结论：引用类型参数的传递，调用方的变量，和接收方的参数变量，指向的是同一个对象。双方任意一方对这个对象的修改，都会影响对方（因为指向同一个对象嘛）。

```java
Person p = new Person();
String bob = "Bob";
p.setName(bob); // 传入bob变量
System.out.println(p.getName()); // "Bob"
bob = "Alice"; // bob改名为Alice
System.out.println(p.getName()); //输出:"Bob"
```
方法参数：  
方法可以包含0个或任意个参数。方法参数用于接收传递给方法的变量值。调用方法时，必须严格按照参数的定义一一传递。  
可变参数：  
相当于数组类型,不同于方法参数

    