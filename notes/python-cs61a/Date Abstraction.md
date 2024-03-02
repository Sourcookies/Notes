### Date Abstraction

```python
def rational(n, d):
    def select(name):
        if name == 'n':
            return n
        elif name == 'd':
            return d
    return select	#rational函数返回select函数
					#即x为select函数
    				#传入'n'就返回n,'d'返回d
def numer(x):
    return x('n')
def denom(x):
    return x('d')

x = rational(3, 8)  #主函数，x为3分之8
print(numer(x))		

```

sum：高阶函数的应用，详解见[Higher-Order Functions.md](./Higher-Order Functions.md)

