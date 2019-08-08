### 数据类型

```python
str()  # 创建字符串
int()  # 创建整数
float()  # 创建浮点数
bool()  # 创建布尔值
```



### 数据结构

```python
# list
classmates = ['Michael', 'Bob', 'Tracy']
classmates.append('Adam')  # 追加元素到末尾
classmates.insert(1, 'Jack')  # 插入元素到指定的位置
classmates.pop(1)  # 删除指定位置的元素
classmates[1] = 'Sarah'  # 替换元素

# tuple
classmates = ('Michael', 'Bob', 'Tracy')

# dict
d = {'Michael': 95, 'Bob': 75, 'Tracy': 85}
d['Adam'] = 67  # 通过key放入
'Thomas' in d  # 通过in判断key是否存在
d.get('Thomas')  # 通过get()判断key是否存在
d.get('Thomas', -1)  # 或者自己指定的value
d.pop('Bob')  # 用pop(key)删除一个key

# set
s = set([1, 2, 3])
s.add(4)  # 通过add(key)添加元素
s.remove(4)  # 通过remove(key)删除元素
```



### 循环

```python
# for...in循环
sum = 0
for x in [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]:
    sum = sum + x
print(sum)

# while循环
sum = 0
n = 99
while n > 0:
    sum = sum + n
    n = n - 2
print(sum)

# break
n = 1
while n <= 100:
    if n > 10: # 当n = 11时，条件满足，执行break语句
        break # break语句会结束当前循环
    print(n)
    n = n + 1
print('END')

# continue
n = 0
while n < 10:
    n = n + 1
    if n % 2 == 0: # 如果n是偶数，执行continue语句
        continue # continue语句会直接继续下一轮循环，后续的print()语句不会执行
    print(n)
```

