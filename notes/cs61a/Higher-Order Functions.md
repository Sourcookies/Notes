### 高阶函数

```python
def composel(f,g):
    def composed(x):
        return f(g(x))
    return composed

def square(x):
    return x*x
    
def add_one(x):
    return x + 1  

h = composel(square,add_one) #传入函数名
result = h(12)				
>>>13*13
>>>169
调用并返回数值：
composel函数调用composed，
composed函数调用f(g(x))，并返回它的值给composed
再返回值给composel
```



lambda表达式(作用和上面一样)：

```python
def composel(f,g):
    return lambda x:f(g(x))

f = composel(lambda x: x*x,lambda y:y + 1)
result =f(12)
```



```python
res = [original_function(*args) for i in range(trials_count)]

创建一个空列表 res，用于存储每次调用 original_function 的结果。
使用 range(trials_count) 生成一个从0到 trials_count-1 的整数序列，并遍历该序列。
在每次循环中，使用 original_function(*args) 调用函数，并将返回值添加到列表 res 中。
最终，res 列表将包含 trials_count 个元素，每个元素都是一次调用 original_function 的结果。
```



求最大公约数：

辗转相除法：

```c++
nt gcd(int a,int b){
    if(b == 0)
        return a;
    return gcd(b,a%b);
}

int main()
{
    int a = 12,b = 18;
    int res = gcd(a,b);
    cout << a << "和"<< b << "的最大公约数是" << res<<endl;
    return 0;
}
```

```python
2：
def gcd(n, d):
	while n != d:
		n, d = min(n, d), abs(n-d)
	return n
```







