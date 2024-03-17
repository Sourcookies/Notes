```markdown
class Account:
	def __init__(self, name): #两条下划线
		self.holder = name
		self.balance = 0
		
	def deposit(self, amount):
		self.balance += amount
		return self.balance
a = Account('John')
a.deposit(10) #存款10元
#self类似this
```

