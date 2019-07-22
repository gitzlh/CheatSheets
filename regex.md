# Python 正则表达式

## PART 1: 正则表达式基础

<img src="regex.png" alt="REGEX"
	title="regex expression" width="800" height="8jj00" />

## PAER 2: python 正则函数

### re.match(regex, str)j
* 返回值：* 匹配成功，返回Match对象，否则返回None。
* 用例 *
```python
test = '010-122345'
if re.match(r'^\d{3}[-]\d{5}$', test):
    print('success!')
else:
    print('fail!')
```

### re.split(regex,str)
