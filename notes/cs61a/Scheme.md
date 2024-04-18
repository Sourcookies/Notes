cond 和 begin语法:

```scheme
if x > 10:
	print('big')
elif
else
等于
(cond ((> x 10) (print 'big))
	  ((> x 5)  (print 'medium))
	  (else     (print 'small)))



if 
	print()
    print()
else
等于
(cond ((> x 10) (begin (print 'big) (print 'guy)))
      (else     (begin (print     ) (print     ))))

```

定义:

```
a = 3
b = 2 + 2
c = math.sqrt(a*a + b*b)
a and b are still bound down here
等于

(define c (let ((a 3)
				 (b (+ 2 2)))
				 (sqrt (+ (* a a) (* b b)))))
a b 暂时绑定 3 4
```

