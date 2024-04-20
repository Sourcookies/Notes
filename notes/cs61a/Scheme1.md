```scheme
>(list 'quotient 10 2)
(quotient 10 2)

>(eval (list 'quotient 10 2))
5
```

```scheme
(define b 4)
'(a , (+ b 1)) => (a (unquote (+ b 1)))
`(a , (+ b 1)) => (a 5)
```



两种定义方式：

```
scm> (define foo (lambda (x y) (+ x y)))
foo
scm> (define (foo x y) (+ x y))
foo
```



while statements:

```scheme
x = 2
total = 0
while x < 10:
     total = total + x * x
     x = x + 2
     
     
(begin 
	(define (f x total)
		(if (< x 10)
			(f (+ x 2) (+ total (* x x)))
			total))	 #x>10:return total
	
> (f 2 0)))	
```

