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
> 列表、字典和字符串都可以使用for-in遍历
```python
for i in [1,2,3]:
    print(i)
# 打印出的是列表的每一项
for i in {"id":0, "name":"cellerchan"}:
    print(i)   
# 打印出的i是字典中的键
for i in "吴承恩"：
    print(i)
# 打印出的是字符串中的每一个字符
```

### range(x)函数
> 功能：接收一个数字，生成一个从0到x-1的整数序列。
```python
for i in range(3):
    print(i)
# 0 1 2 
```

其他用法：
- `range(a,b)`生成一个取头不取尾的整数序列。
- `range(0,10,3)` 从0取到9(取头不取尾)，整数的间隔为3

### while循环
```python
a = 0
while a < 5:
    a = a + 1;
    print(a)
# 1 2 3 4 5
```
```python
# 只有当输入的password等于123的时候，while循环才执行结束，才会执行print语句
password = ''
while password != '123':   
    password = input('请输入密码：')
print('欢迎回家')
```

### 布尔值
```python
# 注意：首字母大写
True
False
```
python中为假的值：
```python
False
0
''
[]
{}
None
```

### bool()方法
> 可以判断表达式是否为真
```python
print(bool(1))  # True
print(bool(0))  # False
print(bool(''))  # False
```

### 布尔值运算
- and  与
- or   或
- not  翻转
- in   判断一个元素是否在一堆数据之中
- not in 判断一个元素是否不在一堆数据之中
```python
print(bool(1 and True))  # True
print(bool(1 or False))  # True
print(bool(not True))  # False
print(bool(1 in [1,2,3]))  # True
print(bool(1 not in [1,2,3]))  # False
```

### break语句
> 用于跳出循环
```python
# 大于50跳出循环
for i in range(1,100):
    if i > 50:
        break;

# 孙悟空来了之后跳出循环
while True:    
    print('上供一对童男童女')
    t = input('孙悟空来了吗')
    if t == '来了':
        break
print('孙悟空制服了鲤鱼精，陈家庄再也不用上供童男童女了')
```

### continue语句
```python
while True:
    q1 = input('第一问：你一生之中，在什么地方最是快乐逍遥？')
    if q1 != '黑暗的冰窖':
        continue
    print('答对了，下面是第二问：')
    q2 = input('你生平最爱之人，叫什么名字？')
    if q2 != '梦姑':
        continue
    print('答对了，下面是第三问：')
    q3 = input('你最爱的这个人相貌如何？')
    if q3 == '不知道':
        break
print('都答对了，你是虚竹。')
```

### pass语句
> 跳过
```python
a = int(input('请输入一个整数：'))
if a > 100:
    pass;
else:
    print('你输入了一个小于100的数字')
```

### else语句
> 当循环中没有碰到break语句，就会执行循环后面的else语句，否则就不会执行
```python
# 会打印 你到了3
for i in range(5):
    if i ==3:
        break;
else:
    print('你到了3')
```

### while和if-else配合使用
```python
a = 24
while True:
    inp = int(input('请输入数字：'))
    if inp < 24:
        print('太小了')
    elif inp > 24:
    	print('太大了')
    else:
        break;
print('你终于猜对了')
```

### sleep()函数
```python
import time  # 调用time模块
time.sleep(secs)  
# 使用time模块的sleep()函数，参数是间隔的秒数
# time.sleep(1.5) 表示停留1.5秒后再运行后续代码
```

### randint()函数
```python
import random
print(random.randint(0,9))  # 随机生成0-9（含0和9）的整数
```