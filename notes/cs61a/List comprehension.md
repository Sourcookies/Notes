###  List comprehension

~~~python
odds = [1, 3, 5, 7, 9]
[x for x in odds if 25 % x == 0]

>>> [1, 5]  x符合条件，且在odds中
~~~

```python
def divisors(n):
    return [1] + [x for x in range(2, n) if n%x==0]
    
>>>divisors(1)
[1]
>>>divisors(4)
[1, 2]
```

```python
{0:0,1:1,2:4,3:9....9:81}
squares = {x:x*x for x in range(10)}
squares[7]
>>>49
```



