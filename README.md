# Python Notes

### 切片
> 定义：使用冒号来截取列表元素的操作叫做切片，切片可以让我们从列表中取出多个元素。

> 切片口诀：左右空，取到头；左要取，右不取。

> 注意：切片是截取了列表的某一部分，所以取到的结果还是列表。

示例代码：
```python
list2 = [5,6,7,8,9]
print(list2[:])  // [5,6,7,8,9]
print(list2[2:])  // [7,8,9]
print(list2[:2])  // [5,6]
print(list2[1:3])  // [6,7]
print(list2[2:4])  // [7,8]
```

### append()

> 作用：给数据添加元素
```
list = [1,2]
list.append(3)
print(list)  // [1,2,3]
```

### del 删除语句
> 可以删除列表元素，也可以删除整个变量
```python
list = [1,2,3,4]
del list[1:2]
print(list);  // [1,3,4]

album = {'周杰伦':'七里香', '王力宏':'心跳'}
del album['周杰伦']  // {'王力宏':'心跳'}
album
```

### len()  获取列表或字典的长度
```python
students = [1,2,3,4]
scores = {
    '小明': 90，
    '小红': 95,
    '小刚': 100
}
print(len(students))  // 4
print(len(scores))  // 3
```

### 列表和字典的区别
> 在python中，字典是无序的，只要键值一样，那么这两个字典就是相等的（和js不一样）。

> 列表和字典都支持任意嵌套；
```python
scores1 = {'小明':95,'小红':90,'小刚':100}
scores2 = {'小刚':100,'小明':95,'小红':90}
print(scores1 == scores2)  // true
```

### for...in...循环

