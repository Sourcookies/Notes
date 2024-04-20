```
(cons 1 (cons 2 (cons 3 nil)))
等于
(list 1 (list 2))

例子：
(define lst
  'YOUR-CODE-HERE
  (cons (cons 1 nil)
            (cons 2
                 (cons (cons 3 (cons 4 nil))
                       (cons 5 nil))))

)
list: ((1) 2 (3 4) 5)
```



```scheme
first rest 
等于
car cdr

例子：
scm> (define a (cons 1 (cons 2 (cons 3 nil))))  ; Assign the list to the name a
a
scm> a
(1 2 3)
scm> (car a)
1
scm> (cdr a)
(2 3)
scm> (car (cdr (cdr a)))
3
```

lambda:

```scheme
scm> (lambda (x y) (+ x y))        
(lambda (x y) (+ x y))
scm> ((lambda (x y) (+ x y)) 3 4)  
7
```

