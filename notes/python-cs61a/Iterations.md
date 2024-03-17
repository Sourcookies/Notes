```markdown
def countdown(k):
	if k > 0:
		yield k
		yield from countdown(k-1)

>>> t = countdown(3)
>>> next(t)
3
>>> next(t)
2
#yield作用和return很像，每次遇到 yield 时函数会暂停并保存当前所有的运行信息（保留局部变量），返回yield的值, 并在下一次执行next()方法时从当前位置继续运行，直到生成器被全部遍历完.

yield from countdown(k-1)等于
for x in countdown(k-1):
    yield x
```

