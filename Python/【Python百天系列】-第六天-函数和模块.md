### 【Python百天系列】-第六天-函数和模块

#### 一：背景

代码有很多种坏味道，重复是最坏的一种

#### 二：函数的定义

关键字：`def`

使用`def`来定义函数并给函数起个名字（名字规则与变量规则一致），同时可设置函数的参数

```python
# 定义求两个数之和的函数
def sum(a,d):
    return a+b
```

#### 三：函数的参数

在python中，函数的参数可以有`默认值`，也支持`可变参数`，所以python中的函数`不支持函数重载`

```python
# 函数定义
def sum(a=0,b=0,c=0):
    return a+b+c
# 函数使用
print(sum()) #使用函数默认值，定义函数时参数必须赋值默认值，否则出错
print(sum(1)) #可变参数
print(sum(1,2))#可变参数
print(sum(1,2,3))#可变参数
print(sum(b=10,c=2,a=0))#不按照函数定义的顺序，但需要指定对应的参数名的值，否则出错
```

对于`可变参数`的函数，更好的实现方案为使用可变参数(可以理解可变参数是对函数重载的另一种体现)，例如上面的sum函数，可以优化为这样

```python
# 函数的定义
def sum(*args):
    total=0;
    for val in args:
        total+=val
    return total 

#函数的使用
print(sum())
print(sum(1)) 
print(sum(1,2))
print(sum(1,2,3))

# 此时不按照函数定义的顺序来调用函数会报错，要注意
```

#### 四：模块（module）

##### 模块的作用

1：解决函数，变量等命名冲突的问题

2：实现程序模块化

关键字：`module`，`import`

##### 使用场景

在module1和mdule2中分别定义sum函数，在test中调用

```python

```











