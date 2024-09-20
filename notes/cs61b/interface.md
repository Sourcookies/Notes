Interface: The list of all method signatures

```java
public interface List61B<Item> {
	public void addFirst(Item x);
	public void proo();
}
```

Inheritance: The subclass "inherits" the interface from a superclass

子类必须实现interface的所有方法

default:

```java
default void showDefault(){
		System.out.println("this is showDefaultmethod");
	}
在接口中用default可以写具体的方法，当然它的继承者不用必须实现

两种调用方法：
 1.接口.showDefault()
 2.子类的instance.showDefault()
```

编译时类型和运行类型：

```java
List61B<String> s = new SLList<String>();
x 是 y 的超类，List61B(即为x)是编译时类型
```

