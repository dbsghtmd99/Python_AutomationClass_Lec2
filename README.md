# Python_AutomationClass_Lec2

두번째 수업은 첫번째 수업에서 배운 기본 자료형에 대한 처리를 위해 사용되는 여러가지 함수들에 대해 학습하였다.

소스 코드 파일은 [https://github.com/dbsghtmd99/Python_AutomationClass_Lec2](https://github.com/dbsghtmd99/Python_AutomationClass_Lec2) 에서 확인 가능하다.

## 1. 기본 자료형 함수

### 1.1. 문자열 함수

```python
'문자열'.count('문자') # 문자열 안에서 문자 에 대한 문자가 몇 개 있는지 알려준다

# 문자열에서 문자 가 처음 나오는 인덱스 를 알려준다. 일치하는 문자가 없을 시 -1 을 반환한다
'문자열'.find('문자') 

'문자열'.index('문자') # find 와 동일하지만 일치하는 문자가 없을 시 에러 발생

'추가할 문자열'join('문자열') # '추가할 문자열' 을 '문자열' 사이에 삽입한다

'문자열'.upper() # 소문자 대문자로 변환 
'문자열'.lower() # 대문자 소문자로 변환

'문자열'.lstrip() # 왼쪽 공백 지우기 
'문자열'.rstrip() # 오른쪽 공백 지우기
'문자열'.strip() # 양쪽 공백 지우기

'문자열'.replace('기존 문자열', '바꿀 문자열') # 문자열을 바꿔준다

'문자열'.split('기준 문자열') # 문자열에서 '기준 문자열'을 기준으로 문자열을 나누어 준다

```
### 1.2. 리스트 함수

1. append(추가할 object)
   
```python
a = [1, 2, 3]
a.append(4)         # a = [1, 2, 3, 4]
a.append([5, 6])    # a = [1, 2, 3, 4, [5, 6]]
```

2. sort()

```python
a = [1, 3, 2]
a.sort()                # a = [1, 2, 3]
a.reverse()             # a = [3, 2, 1]
a.sort(reverse = True)  # a = [3, 2, 1]
```

3. index(찾는 요소)

```python
a = ['a', 'b', 'c']
a.index('c')    # 2
```

4. insert(인덱스, 추가할 object)

```python
a = ['a', 'b', 'c']
a.insert(1, 'a')    # a = ['a', 'a', 'b', 'c']
```

5. remove(제거할 object) 또는 del a[인덱스]

```python
a = ['a', 'b', 'c']
a.remove('a')   # a = ['b', 'c']
del a[1]    # a = ['b']
```

6. pop(제거할 object) (제거된 요소를 반환)

```python
a = ['a', 'b', 'c']
a.pop('b')  # ['b']
```

7. count(개수를 알고싶은 object)

```python
a = ['a', 'b', 'a', 'c']
a.count('c')    # 2
```

8. extend(뒤에다 추가할 리스트)

```python
a = ['a']
a.extend(['b', 'c'])    # a = ['a', 'b', 'c']
```

### 1.3. 튜플의 경우

튜플은 내부의 값을 변경할 수 없기에 다음과 같은 코드를 실행하면 런타임 에러가 발생한다.

```python
t1 = (123, 456)

del t1[0] # Error

```

## 3. 연습문제

```python
# 1-1
list_a = [171500, 172000, 174500, 170500, 174000]
print("min : {}".format(min(list_a)))
print("max : {}".format(max(list_a)))
```

```python
# 1-1
dict_a = {"12/02": 171500, "12/03": 172000, "12/04": 174500, "12/05": 170500, "12/06": 174000}

```

```python
# 1-2
print("12/05 : {}".format(dict_a["12/05"]))
```

```python
# 1-3
score1 = [51, 32, 88, 86, 15]
score2 = [78, 64, 94, 42, 50]
```

```python
# 2-1
score1 = [51, 32, 88, 86, 15]
score2 = [78, 64, 94, 42, 50]
```

```python
# 2-2
sum = []
for i in range(0, 5):
    sum.append(score1[i] + score2[i])
print(sum)

# 다음과 같이도 표현 할 수 있다.
print(list(map(lambda x, y: x+y, score1, score2)))
```

```python
# 2-3
Letter = []
for i in sum:
    if i / 2 >= 90:
        val = 'A'
    elif i / 2 >= 80:
        val = 'B'
    elif i / 2 >= 70:
        val = 'C'
    elif i / 2 >= 60:
        val = 'D'
    else:
        val = 'F'
    Letter.append(val)

print(Letter)
```

```python
# 3-1
for i in range(2, 10):
    for j in range(1, 10):
        print(str(i) + "*" + str(j) + "=" + str(i * j))
```

```python
# 3-2
a = 2

while a < 10:
    b = 1
    while b < 10:
        print(str(a) + "*" + str(b) + "=" + str(a * b))
        b += 1
    a += 1
```

```python
# 4-1
def fact(n):
    if n == 1 or n == 0:
        return 1
    elif n > 1:
        return n * fact(n - 1)


print(fact(5))
```

```python
# 4-2
def swap(inputList):
    inputList.sort(reverse=True)
    return inputList


inputList = [10, 20]
```
