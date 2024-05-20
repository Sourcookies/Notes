```java
SLList<Integer> s1 = new SLList<>(5);
s1.insert(10);
```

```java
System.arraycopy(b, 0, x, 3, 2);
x[3:5] = b[0:2] (python)
b数组的0位置复制到从x[3]开始2位
```

泛型数组不被允许：

```java
public class AList<Item>{
	public AList() {
		items = (Item[]) new Object[100];  ✔
		items = new Item[100]; × 
	}
}
```

loitering(徘徊)：

```java
保持对不需要的对象的引用
当remove int数组时，数组只要size--，不需要改变数组中的值，因为add数时会将其覆盖，但为泛型数组时，内存占用太大，需要改变
 /*泛型数组可能更占空间，所以将其置null*/
    public Item removeLast(){
        Item returnItem = getLast();
        items[size - 1] = null;
        size--;
        return returnItem;
    }
```



