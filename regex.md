# Python 正则表达式

## PART 1: 正则表达式基础

<img src="regex.png" alt="REGEX"
	title="regex expression" width="800" height="800" />

## PAER 2: python 正则函数

### re.match(regex, str)
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
### Match对象的分组
- 正则表达式中，用()括住的，就是要提取的分组（Group）
- 提取时，group(0)是原始字符串，group(1)、group(2)……表示第1、2、……个子串。
####用例：
```python
test = '010-122345'
m = re.match(r'^（\d{3}）[-]（\d{5}$）', test)
if m:
    return m.group(1)
```
### re.split(regex,str)
#### 返回值 
切分后的list
#### 用例
```python
patter = r'[,;\s
re.split(r'[\s,;]+', 'a.b;; c  d')
['a', 'b', 'c', 'd']

```
J
