算术：

```
C: a = b + c
RISCV: add s1, s2, s3	加
a = b - c
sub s1, s2, s3	减
mul div 乘除
addi s1, s2, 3  i为常整数量constant integer
```

```
一个字(word)是32位(bits)，一个字节(byte)是8位(四分之一字)
half word : 16bits
```



数据传输Data Transfer:

内存按字节寻址，所以下一个字的偏移是4

```
lw: load word
sw: store word

lw    t0,12(s3)  #t0=A[3]
add   t0,s2,t0   #t0=A[3]+b
sw    t0,40(s3)  #A[10]=A[3]+b

32位中int大小为4，s3是a[0],A[3]偏移量为12
sw是从寄存器到内存里
s3是基址指针，12是偏移量offset
```

```
addi x12, value calue是常量
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

blt reg1, reg2, Label
if (reg1 < reg2) goto Label;

blt(less) bge(greater) 
: reg1 < reg2

eg.
bne x13, x14,Else
add x10, x11,x12
j Exit
Else:sub x10, x11, x12
Exit:
============
if (i == j)
f = g + h;
else
f = g - h;
```

