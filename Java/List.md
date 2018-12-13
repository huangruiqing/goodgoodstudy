## List 源码篇

### 一、ArraryList

> 1、使用数组保存元素
>
> 2、初始容量 10
>
> 3、每次add 会计算容量是否给用，当容量超过范围时会在原
>
> 容量的基础 加上(+) 原容量>>1 的结果
>
> 4、在add,remove,set 扩容的时候，将原数据 copy到新的数组中 
>
> ```java
> System.arraycopy(elementData, index, elementData, index + 1,
>          size - index)
> ```
>
> 5、size变量 记录ArraryList 长度

### 二 LinkedList

> 1、

