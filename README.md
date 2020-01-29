# Python_AutomationClass_Lec2
두번째 수업은 첫번째 수업에서 배운 기본 자료형에 대한 처리를 위해 사용되는 여러가지 함수들에 대해 학습하고 간단한 연습문제를 풀었다.

## 1. 기본 자료형 함수

### 1.1. 문자열 함수
### 1.2. 리스트 함수
### 1.3. 튜플의 경우

## 2. 함수

## 3. 연습문제
코드 원본은 github repository([https://github.com/dbsghtmd99/Python_AutomationClass_Lec2](https://github.com/dbsghtmd99/Python_AutomationClass_Lec2))에서 다운로드 받을 수 있다.

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
