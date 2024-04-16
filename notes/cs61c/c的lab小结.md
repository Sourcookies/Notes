`node **head_ptr` 中有两个星号的原因是，`head_ptr` 是一个指向指针的指针。

在函数中，`head_ptr` 是指向链表头部指针的指针。通过使用指向指针的指针，我们可以在函数内部修改指向链表头部的指针的值，而不仅仅是修改其副本。这样可以确保对链表头部指针的修改在函数外部也能生效。

在C语言中，如果我们想要修改函数参数指向的值，而不是只修改其副本，就需要传递指向该值的指针。因为我们要修改指针 `head_ptr` 所指向的指针，所以需要使用指向指针的指针 `node **head_ptr`。

 

```
结构体：
struct vector_t {
    size_t size;
    int *data;
};


vector_t *retval;        #*retval是个指针
retval = malloc(sizeof(vector_t));
          #为retval分配空间

retval->size = 1;
retval->data = malloc(sizeof(int));
		  #为它的属性data分配空间
		
        
如果要删除：
 free(retval->data);
 free(retval);
	#如果先把retval删除了,丢失了data所指向内存的引用，导致内存泄漏，无法访问retval->data所指向的内存来释放它
```

