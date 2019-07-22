# Python 正则表达式

## PART 1: 正则表达式基础

<img src="regex.png" alt="REGEX"
	title="regex expression" width="800" height="800" />

## PART 2: python 正则函数

### 1. re.match(regex, str)
#### 返回值
匹配成功，返回Match对象，否则返回None。
#### 用例：
```python
test = '010-122345'
if re.match(r'^\d{3}[-]\d{5}$', test):
    print('success!')
else:
    print('fail!')
```
### 2. Match对象的分组
- 正则表达式中，用()括住的，就是要提取的分组（Group）
- 提取时，若m为Match对象，m.group(0)是原始字符串，m.group(1)表示第1个子串,m.groups()返回一个tuple。

#### 用例：
```python
test = '010-122345'
m = re.match(r'^(\d{3})[-](\d{6}$)', test)
if m:
    print(m.group(1))
```
### 3. re.split(regex,str)
#### 返回值 
切分后的list
#### 用例
```python
re.split(r'[\s,;]+', 'a.b;; c  d')
['a', 'b', 'c', 'd']

```

