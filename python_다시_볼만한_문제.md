# 간단한 코드 스니펫

```python

```

## 특정 문자 제거하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120826

```python
import re

re.sub('A', '', 'abcde12345ABCDEabcde12345ABCDE')
re.sub('[a-z]', '', 'abcde12345ABCDEabcde12345ABCDE')
re.sub('[123]', '', 'abcde12345ABCDEabcde12345ABCDE')
re.sub('[135]', '', 'abcde12345ABCDEabcde12345ABCDE')
re.sub('[a-zA-Z]', '', 'abcde12345ABCDEabcde12345ABCDE')
re.sub('[0-9]', '', 'abcde12345ABCDEabcde12345ABCDE')

import re

re.sub('[a-zA-Z]', '', 'aAb1B2cC34oOp')
list(re.sub('[a-zA-Z]', '', 'aAb1B2cC34oOp'))
list(map(int, list(re.sub('[a-zA-Z]', '', 'aAb1B2cC34oOp'))))
# list(map(lambda x:int(x), list(re.sub('[a-zA-Z]', '', 'aAb1B2cC34oOp'))))
map(int, list(re.sub('[a-zA-Z]', '', 'aAb1B2cC34oOp')))
sum(map(int, list(re.sub('[a-zA-Z]', '', 'aAb1B2cC34oOp'))))

re.findall('[0-9]', 'aAb1B2cC34oOp')
sum(map(int, re.findall('[0-9]', 'aAb1B2cC34oOp')))

if True: print('hello')
print('if') if True else print('else')
1 if True else 2
1 if False else 2


# result = 0
# for i in 'hello134':
#     if i.isdigit():
#         result += int(i)

# '1'.isdigit()
# 't'.isdigit()
# '1'.isnumeric()
# 't'.isnumeric()
# 'abc'.islower()
# 'aBc'.islower()
# 'abc'.isalpha()
# 'abc123'.isalpha()

# https://www.bigocheatsheet.com/
```

## 문자열안에 문자열

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120908

```js
def solution(str1, str2):
    return 1 if str2 in str1 else 2
```

## 숨어있는 숫자의 덧셈 (1)

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120851

```python
def solution(my_string):
    result = 0
    for i in my_string:
        if i.isdigit():
            result += int(i)
    return result

import re

def solution(my_string):
    return sum(map(int, re.findall(r'[0-9]', my_string)))
```

## 진료순서 정하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120835

```py
def solution(emergency):
    # 원본은 a라는 이름으로 가지고 있습니다.
    # emergency를 정렬한 값을 b라고 합니다.
    # a에 있는 값을 b에서 찾는데 index만 찾아서
    # 새로운 리스트로 만듭니다.
    a = emergency
    b = sorted(a, reverse=True)
    result = []
    for i in a:
        result.append(b.index(i) + 1)

    return result


def solution(emergency):
    s_emergency = sorted(emergency, reverse=True)
    return [s_emergency.index(i) + 1 for i in emergency]

def solution(emergency):
    s_emergency = sorted(emergency, reverse=True)
    return list(map(lambda x:s_emergency.index(x)+1, emergency))
```

## 문자열 밀기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120921

```py
import collections

collections.Counter('aaabbccccccddddd')
sample = collections.deque("hello")
# sample.rotate(2)
sample.rotate(-1)
''.join(sample)

import collections

def solution(A, B):
    if A == B:
        return 0
    비교 = collections.deque(A)
    for i in range(len(A)):
        비교.rotate(1)
        if ''.join(비교) == B:
            return i + 1
    return -1

def solution(A, B):
    return (B*2).find(A)
```

## 특이한 정렬

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120880

## 다항식 더하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120863

## OX퀴즈

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120907?language=javascript

## 겹치는 선분의 길이

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120876
