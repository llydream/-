### 【Python百天系列】-第六天-函数和模块

#### 一：背景

代码有很多种坏味道，重复是最坏的一种

#### 二：函数的定义

关键字：`def`

使用`def`来定义函数并给函数起个名字（名字规则与变量规则一致），同时可设置函数的参数

```python
# 定义求两个数之和的函数
def sum(a,b):
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

关键字：`import`，`from`，`as`

##### 使用场景

###### 导入模块

>第一种：适用于从某个模块中引入单个函数 （关键字`from [模块名] import [函数]`）
>
>```python
>from module1 import sum
>```
>
>第二种：将整个模块引入，可使用模块中的所有函数（关键字`import[模块名]as[别名]`）
>
>```python
>import module1 as module
>```

###### 可执行代码处理

>在导入其他模块时，除了定义函数外还有可执行的代码，那么python解释器在导入模块时会触发执行，实际应用中，我们可能不希望这样，因此我们在模块中编写可执行代码时，最好将这些可执行代码放入条件语句中，当条件满足时在执行
>
>`module1.py`
>
>```python
>def sum(a,b):
>    return a+b
>print('我是可执行代码')
>```
>
>`module2.py`
>
>```python
>import module1 as m1
>m1.sum(1,3)
>
># 此时除了会执行sum求和，同时会打印语句
>```
>
>修改后的`module1.py`
>
>```python
>def sum(a,b):
>    retun a+b
>if __name__='__main__':
>    print('我是可执行代码')
># __name__ 是python中一个隐含的变量，它代表模块的名字
># __main__ 是被pyhton解释器直接执行的模块名称
>```
>
>`module2.py`
>
>```python
>import module1 as m1
>m1.sum(1,3)
>
># 此时仅会执行sum求和，因为此时模块的名字为module1而不是__main__
>```

###### 示例

在module1和mdule2中分别定义sum函数，在test中调用

`module1.py`

```python
def sum(a,b):
    return a+b
```

`module2.py`

```python
def sum(a,b):
    return a+b
```

`test.py`

```python
# 第一种方式导入
from module1 import sum
sum(1,3)
from module2 import sum
sum(3,4)

# 第二种方式导入
import module1 as m1
import module as m2

m1.sum(1,3)
m2.sum(3,4)

```

###### 注意

```python
from module1 import sum
from module2 import sum
sum(1,2)

# 如果多个模块中有相同名称的函数，在导入时 后面的会覆盖前面的模块，因此日常推荐使用第二种方式的导入模块
```









