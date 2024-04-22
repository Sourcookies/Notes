算术：

```
C: a = b + c
RISCV: add s1, s2, s3	加
a = b - c
sub s1, s2, s3	减
mul div 乘除
addi s1, s2, 3  i为常整数量constant integer
```



数据传输Data Transfer:

```
lw: load word
sw: store word

lw    t0,12(s3)  #t0=A[3]
add   t0,s2,t0   #t0=A[3]+b
sw    t0,40(s3)  #A[10]=A[3]+b

32位中int大小为4，A[3]偏移量为12
```



条件分支：

```
Branch if Equal(beq)
>beq reg1,reg2,label
使用：if reg1 == reg2,跳转到label

Branch if Not Equal(bne)
相反

Jump(j)
>j label

label是else，then

blt(less) bge(greater) 
: reg1 < reg2
```

