```
& and
| or
^ xor
<< sll
>> srl
没有not： xor 11111111 代替not
```

```
算术右移： 一般处理有符号数
sra 数向右移动，符号位复制到空出的高位
```

```
mv rd, rs = addi rd, rs, 0
li rd, 13 = addi rd, 13
nop = addi x0, x0, 0 空转等待时用的
```

```
old:
1008 addi ra, zero,1016
1012 j sum
:ra = 1016 goto sum

new: 
1008 jal sum

```

