# Lv0

## 몫 구하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120805
-   python

```py
def solution(num1, num2):
    return num1 // num2
```

-   js

```js
function solution(num1, num2) {
    return Math.floor(num1 / num2);
}
```

## 두 수의 곱

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120804
-   python

```py
def solution(num1, num2):
    return num1 * num2
```

-   js

```js
function solution(num1, num2) {
    return num1 * num2;
}
```

## 두 수의 차

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120803
-   python

```py
def solution(num1, num2):
    return num1 - num2
```

-   js

```js
function solution(num1, num2) {
    return num1 - num2;
}
```

## 두 수의 합

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120802
-   python

```py
def solution(num1, num2):
    return num1 + num2
```

-   js

```js
function solution(num1, num2) {
    return num1 + num2;
}
```

## 나머지 구하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120810
-   python

```py
def solution(num1, num2):
    return num1 % num2
```

-   js

```js
function solution(num1, num2) {
    return num1 % num2;
}
```

## 숫자 비교하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120807
-   python

```py
def solution(num1, num2):
    if num1 == num2: return 1
    else: return -1

# 3항 연산자로 표현하기
# A if 조건 else B
def solution(num1, num2):
    return 1 if num1 == num2 else -1

def solution(num1, num2):
    answer = 1 if num1 == num2 else -1
    return answer

def solution(num1, num2):
    answer = {num1 == num2 : 1, num1 != num2 : -1}.get(True, -1)
    return answer
```

-   js

```js
function solution(num1, num2) {
    var answer = num1 === num2 ? 1 : -1;
    return answer;
}
```

## 나이 출력

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120820
-   python

```py
def solution(age):
    return 2022 - age + 1
```

-   js

```js
function solution(age) {
    return 2022 - age + 1;
}
```

## 각도기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120829
-   python

```py
def solution(angle):
    if angle < 90:
        return 1
    elif angle == 90:
        return 2
    elif angle < 180:
        return 3
    elif angle == 180:
        return 4
    return answer

# 3항 연산자로 표현하기
# A if 조건 else B if 조건 else C

# error 코드
# def solution(angle):
#     return 1 if angle < 90 elif angle == 90 2 elif angle < 180 3 elif angle == 180 4

def solution(angle):
    return 1 if angle < 90 else 2 if angle == 90 else 3 if angle < 180 else 4 if angle == 180 else -1

```

-   js

```js
function solution(angle) {
    if (angle < 90) {
        return 1;
    } else if (angle == 90) {
        return 2;
    } else if (angle < 180) {
        return 3;
    } else if (angle == 180) {
        return 4;
    }
}
```

## 두 수의 나눗셈

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120806
-   python

```py
def solution(num1, num2):
    answer = 0
    return int(num1 / num2 * 1000)
```

-   js

```js
function solution(num1, num2) {
    return Math.floor((num1 / num2) * 1000);
}

function solution(num1, num2) {
    return parseInt((num1 / num2) * 1000);
}

// 비트 부정연산자 2회 사용 ~n = -(n+1)
function solution(num1, num2) {
    return ~~((num1 / num2) * 1000);
}
```

## 배열의 평균값

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120817
-   python

```py
def solution(numbers):
    return sum(numbers)/len(numbers)

# 다차원 배열의 합도 구할 수 있음
import numpy as np

def solution(numbers):
    return np.sum(numbers)/len(numbers)
```

-   js

```js
function solution(numbers) {
    var answer = 0;
    for (i of numbers) {
        answer += i;
    }
    return answer / numbers.length;
}

function solution(numbers) {
    var answer = numbers.reduce((a, b) => a + b, 0) / numbers.length;
    return answer;
}
```

## 짝수의 합

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120831
-   python

```py
def solution(n):
    answer = 0
    for i in range(0, n+1, 2):
        answer += i
    return answer

def solution(n):
    return sum([i for i in range(2, n + 1, 2)])

def solution(n):
    answer = sum(range(2, n + 1, 2)) # list로 형변환 할 필요 없습니다.
    return answer
```

-   js

```js
function solution(n) {
    var answer = 0;
    for (let i = 0; i <= n; i += 2) {
        answer += i;
    }
    return answer;
}

function solution(n) {
    // Array(Math.floor((n+3)/2)).fill().map((_, i) => i * 2).reduce((a, c) => a + c, 0); // 왜 안되지?
    return Array(n)
        .fill()
        .map((_, i) => i + 1)
        .filter((v) => v % 2 === 0)
        .reduce((a, c) => a + c, 0);
}
```

## 중복된 숫자 개수

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120583
-   python

```py
def solution(array, n):
    return array.count(n)

from collections import Counter

def solution(array, n):
    return Counter(array).get(n)
```

-   js

```js
function solution(array, n) {
    return array.filter((v) => v === n).length;
}

function solution(array, n) {
    var answer = 0;
    for (num of array) if (num === n) answer++;
    return answer;
}
```

## 머쓱이보다 키 큰 사람

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120585
-   python

```py
def solution(array, height):
    count = 0
    for i in array:
        if  i > height:
            count += 1
    return count

def solution(array, height):
    array.append(height)
    array.sort(reverse=True)
    return array.index(height)
```

-   js

```js
function solution(array, height) {
    var answer = array.filter((v) => v > height).length;
    return answer;
}
```

## 양꼬치

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120830
-   python

```py
def solution(n, k):
    if n >= 10:
        k -= n // 10

    return n*12000 + k*2000

def solution(n, k):
    return 12000 * n + 2000 * (k - n // 10)
```

-   js

```js
function solution(n, k) {
    return n * 12000 + k * 2000 - parseInt(n / 10) * 2000;
}
```

## 편지

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120898
-   python

```py
def solution(message):
    return len(message) * 2
```

-   js

```js
function solution(message) {
    return message.length * 2;
}
```

## 자릿수 더하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120906
-   python

```py
def solution(n):
    answer = 0
    for i in str(n):
        answer += int(i)
    return answer

def solution(n):
    answer = sum(list(map(int, str(n))))
    return answer
```

-   js

```js
function solution(n) {
    return n
        .toString()
        .split("")
        .reduce((a, c) => a + parseInt(c), 0);
}
```

## 피자 나눠 먹기(3)

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120816
-   python

```py
def solution(slice, n):
    for i in range(51):
        if n <= i * slice:
            break
    return i
```

-   js

```js
function solution(slice, n) {
    return Math.ceil(n / slice);
}
```

## 문자열 뒤집기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120822
-   python

```py
def solution(my_string):
    return my_string[::-1]

def solution(my_string):
    return ''.join(reversed(list(my_string)))
```

-   js

```js
function solution(my_string) {
    return my_string.split("").reverse().join("");
}

function solution(my_string) {
    return [...my_string].reverse().join("");
}
```

## 배열 원소의 길이

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120854
-   python

```py
def solution(strlist):
    return list(map(lambda x : len(x), strlist))

def solution(strlist):
    answer = []
    return [ len(i) for i in strlist ]
```

-   js

```js
function solution(strlist) {
    return strlist.map((e) => e.length);
}
```

## https://school.programmers.co.kr/learn/courses/30/lessons/120814

-   링크 : 피자 나눠 먹기 (1)
-   python

```py
def solution(n):
    return ((n - 1) // 7) + 1

import math

def solution(n):
    return math.ceil(n / 7)
```

-   js

```js
function solution(n) {
    return Math.ceil(n / 7);
}
```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```

##

-   링크 :
-   python

```py

```

-   js

```js

```
