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

## 문자열안에 문자열

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120908
-   python

```py
def solution(str1, str2):
    return 2 if str1.find(str2) == -1 else 1

def solution(str1, str2):
    return 1 if str2 in str1 else 2
```

-   js

```js
function solution(str1, str2) {
    return str1.includes(str2) ? 1 : 2;
}

function solution(str1, str2) {
    return str1.split(str2).length > 1 ? 1 : 2;
}
```

## 짝수 홀수 개수

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120824
-   python

```py
def solution(num_list):
    짝수 = 0
    홀수 = 0
    for i in num_list:
        if i % 2 == 0:
            짝수 += 1
        else:
            홀수 += 1

    return [짝수, 홀수]

def solution(num_list):
    answer = [0,0]
    for n in num_list:
        answer[n % 2] += 1
    return answer

def solution(num_list):
    나머지 = list(map(lambda v : v % 2, num_list))
    return [나머지.count(0), 나머지.count(1)]
```

-   js

```js
function solution(num_list) {
    var answer = [0, 0];

    for (let a of num_list) {
        answer[a % 2] += 1;
    }

    return answer;
}

function solution(num_list) {
    return [
        num_list.filter((num) => num % 2 === 0).length,
        num_list.filter((num) => num % 2 === 1).length,
    ];
}
```

## 배열 뒤집기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120821
-   python

```py
def solution(num_list):
    return num_list[::-1] # slicing의 연산 가산이 있습니다.
```

-   js

```js
function solution(num_list) {
    return num_list.reverse();
}
```

## 가장 큰 수 찾기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120899
-   python

```py
def solution(array):
    return [max(array), array.index(max(array))]
```

-   js

```js
function solution(array) {
    return [Math.max(...array), array.indexOf(Math.max(...array))];
}
```

## 아이스 아메리카노

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120819
-   python

```py
def solution(money):
    return [money//5500, money%5500]
```

-   js

```js
function solution(money) {
    return [Math.floor(money / 5500), money % 5500]; // parseInt(money/5500)
}
```

## 최댓값 만들기(1)

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120847
-   python

```py
def solution(numbers):
    numbers.sort()
    return numbers[-2] * numbers[-1]

def solution(numbers):
    numbers.sort(reverse=True)
    return numbers[0]*numbers[1]

def solution(numbers):
    v = list(reversed(sorted(numbers)))
    return v[0] * v[1]
```

-   js

```js
function solution(numbers) {
    numbers.sort((a, b) => b - a);
    return numbers[0] * numbers[1];
}
```

## 약수 구하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120897
-   python

```py
def solution(n):
    answer = []
    for i in range(1, n+1):
        if n % i == 0:
            answer.append(i)
    return answer


def solution(n):
    answer = [i for i in range(1,n+1) if n%i == 0]
    return answer
```

-   js

```js
function solution(n) {
    return Array(n)
        .fill(0)
        .map((v, i) => v + i + 1)
        .filter((v) => n % v === 0);
}
```

## 배열 두 배 만들기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120809
-   python

```py
def solution(numbers):
    answer = [i * 2 for i in numbers]
    return answer

def solution(numbers):
    return list(map(lambda x : x * 2, numbers))

import numpy as np

def solution(numbers):
    return (np.array(numbers) * 2).tolist()
```

-   js

```js
function solution(numbers) {
    return numbers.map((i) => i * 2);
}
```

## 배열 자르기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120833
-   python

```py
def solution(numbers, num1, num2):
    return numbers[num1:num2+1]
```

-   js

```js
function solution(numbers, num1, num2) {
    return numbers.splice(num1, num2 - num1 + 1); // 제거한 요소를 반환합니다.
}

///////
v = [10, 20, 30, 40, 50, 60, 70];
v.splice(2, 3);
// [30, 40, 50]
v;
// [10, 20, 60, 70]
v = [10, 20, 30, 40, 50, 60, 70];
v.splice(2, 3, 1000);
// [30, 40, 50]
v;
// [10, 20, 1000, 60, 70]

v = [10, 20, 30, 40, 50, 60, 70];
v.splice(2, 3, [1, 2, 3]);
// (3) [30, 40, 50]
v;
// (5) [10, 20, Array(3), 60, 70]
v = [10, 20, 30, 40, 50, 60, 70];
v.splice(2, 3, 1, 2, 3);
// (3) [30, 40, 50]
v;
// (7) [10, 20, 1, 2, 3, 60, 70]
///////

function solution(numbers, num1, num2) {
    return numbers.slice(num1, num2 + 1); // python의 slice
}

function solution(numbers, num1, num2) {
    return numbers.filter((n, i) => num1 <= i && i <= num2);
}
```

## n의 배수 고르기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120905
-   python

```py
def solution(n, numlist):
    answer = []
    for i in numlist:
        if i % n == 0:
            answer.append(i)
    return answer

def solution(n, numlist):
    answer = [i for i in numlist if i%n==0]
    return answer
```

-   js

```js
function solution(n, numlist) {
    return numlist.filter((v) => v % n === 0);
}
```

## 제곱수 판별하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120909
-   python

```py
def solution(n):
    return 1 if int(n ** 0.5) ** 2 == n else 2

def solution(n):
    return 1 if n ** 0.5 == int else 2

def solution(n):
    return 1 if (n ** 0.5).is_integer() else 2
```

-   js

```js
function solution(n) {
    return Math.sqrt(n) === Math.floor(Math.sqrt(n)) ? 1 : 2;
}

function solution(n) {
    return Number.isInteger(Math.sqrt(n)) ? 1 : 2;
}
```

## 짝수는 싫어요

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120813
-   python

```py
def solution(n):
    return [i for i in range(1, n + 1, 2)]
```

-   js

```js
function solution(n) {
    var answer = [];
    for (let i = 1; i <= n; i += 2) answer.push(i);
    return answer;
}

function solution(n) {
    return Array(n)
        .fill(1)
        .map((v, i) => v + i)
        .filter((v) => v % 2 === 1);
}
```

## 삼각형의 완성조건 (1)

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120889
-   python

```py
def solution(sides):
    sides.sort(reverse=True)
    return 1 if sides[0] < sides[1] + sides[2] else 2
```

-   js

```js
// reduce
// 누산기 (acc)
// 현재 값 (cur)
// 현재 인덱스 (idx)
// 원본 배열 (src)
function solution(sides) {
    var answer = 0;
    const max = Math.max(...sides);
    const sum = sides.reduce((a, c) => a + c, 0) - max;

    answer = max < sum ? 1 : 2;

    return answer;
}
```

## 옷가게 할인 받기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120818
-   python

```py
def solution(price):
    if price >= 500000:
        price *= 0.8
    elif price >= 300000:
        price *= 0.9
    elif price >= 100000:
        price *= 0.95
    return int(price)
```

-   js

```js
function solution(price) {
    if (price >= 500000) return parseInt(price * 0.8);

    if (price >= 300000) return parseInt(price * 0.9);

    if (price >= 100000) return parseInt(price * 0.95);

    return price;
}
```

## 점의 위치 구하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120841
-   python

```py
def solution(dot):
    x, y = dot
    if x >= 0 and y >= 0:
        return 1
    elif x < 0 and y >= 0:
        return 2
    elif x < 0 and y < 0:
        return 3
    elif x >= 0 and y < 0:
        return 4
    return answer
```

-   js

```js
function solution(dot) {
    // const [x, y] = dot;
    var answer = 0;
    if (dot[0] >= 0 && dot[1] >= 0) answer = 1;
    if (dot[0] < 0 && dot[1] >= 0) answer = 2;
    if (dot[0] < 0 && dot[1] < 0) answer = 3;
    if (dot[0] >= 0 && dot[1] < 0) answer = 4;
    return answer;
}
```

## 순서쌍의 개수

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120836
-   python

```py
# 시간초과
def solution(n):
    answer = []
    for i in range(1, n+1):
        for j in range(1, n+1):
            if i * j == n:
                answer.append([i, j])
    return len(answer)


def solution(n):
    answer = 0
    for i in range(n):
        if n % (i+1) == 0: # 나누어 떨어지면 매칭되는 값이 있다는 얘기임
            answer += 1
    return answer
```

-   js

```js
function solution(n) {
    var answer = 0;
    for (let i = 0; i <= n; i++) {
        if (n % i === 0) {
            answer += 1;
        }
    }
    return answer;
}

function solution(n) {
    let answer = 0;
    for (let i = 1; i <= n; i++) {
        if (!(n % i)) answer++;
    }
    return answer;
}
```

## 모음 제거

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120849
-   python

```py
def solution(my_string):
    return my_string.replace('a', '').replace('e', '').replace('i', '').replace('o', '').replace('u', '')

def solution(my_string):
    answer = ''

    for c in my_string:
        if c in ['a', 'e', 'i', 'o', 'u']:
            continue
        answer += c

    return answer

import re

def solution(my_string):
    return re.sub(r"[aeiou]", "", my_string)
```

-   js

```js
function solution(my_string) {
    return my_string.replace(/[aeiou]/g, "");
}

function solution(my_string) {
    return Array.from(my_string)
        .filter((t) => !["a", "e", "i", "o", "u"].includes(t))
        .join("");
}
```

## 배열의 유사도

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120903
-   python

```py
def solution(s1, s2):
    answer = 0
    for i in s1:
        if i in s2:
            answer += 1
    return answer

def solution(s1, s2):
    return len(set(s1) & set(s2))

# 특이한 풀이
def solution(s1, s2):
    dic = {i:1 for i in s1}
    answer = sum(dic.get(j,0)for j in s2)
    return answer
```

-   js

```js
function solution(s1, s2) {
    const i = s1.filter((x) => s2.includes(x));
    return i.length;
}

function solution(s1, s2) {
    let count = 0;
    for (let v of s1) if (s2.includes(v)) count++;
    return count;
}
```

## 특정 문자 제거하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120826
-   python

```py
def solution(my_string, letter):
    return my_string.replace(letter, '')

import re

solution = lambda s, l : re.sub(l, "" , s)
```

-   js

```js
function solution(my_string, letter) {
    const answer = my_string.split(letter).join("");
    return answer;
}

function solution(my_string, letter) {
    let reg = new RegExp(letter, "g");
    return my_string.replace(reg, "");
}
```

## 문자 반복 출력하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120825
-   python

```py
def solution(my_string, n):
    return ''.join(i*n for i in my_string)

def solution(my_string, n):
    answer = ''
    for i in my_string:
        answer += (i * n)
    return answer
```

-   js

```js
function solution(my_string, n) {
    var answer = [...my_string].map((v) => v.repeat(n)).join("");
    console.log(answer);
    return answer;
}
```

## 세균 증식

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120910
-   python

```py
def solution(n, t):
    return n << t

def solution(n, t):
    return n*(2**(t))
```

-   js

```js
function solution(n, t) {
    return n * 2 ** t;
}

function solution(n, t) {
    while (t-- > 0) n *= 2;
    return n;
}
```

## 숨어있는 숫자의 덧셈 (1)

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120851
-   python

```py
def solution(my_string):
    answer = 0
    for i in my_string:
        if i.isnumeric():
            answer += int(i)
    return answer

def solution(my_string):
    return sum(int(i) for i in my_string if i.isdigit())

import re

def solution(my_string):
    return sum(int(n) for n in re.sub('[^1-9]', '', my_string))
```

-   js

```js
function solution(my_string) {
    return my_string
        .replaceAll(/[^\d]/g, "")
        .split("")
        .map((v) => +v)
        .reduce((a, v) => a + v, 0);
}

function solution(my_string) {
    return my_string
        .match(/[0-9]/g)
        .reduce((a, b) => parseInt(a) + parseInt(b));
}
```

## 개미군단

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120837
-   python

```py
def solution(hp):
    answer = hp // 5
    hp = hp % 5
    answer += hp // 3
    hp = hp % 3
    answer += hp // 1
    return answer

def solution(hp):
    return hp // 5 + (hp % 5 // 3) + ((hp % 5) % 3)
```

-   js

```js
function solution(hp) {
    return Math.floor(hp / 5) + Math.floor((hp % 5) / 3) + ((hp % 5) % 3);
}
```

## 문자열 정렬하기 (1)

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120850
-   python

```py
def solution(my_string):
    return sorted(int(i) for i in my_string if i.isdigit())
```

-   js

```js
function solution(my_string) {
    return my_string
        .match(/\d/g)
        .sort((a, b) => a - b)
        .map((n) => Number(n));
}

function solution(my_string) {
    return my_string
        .split("")
        .filter((v) => !isNaN(v))
        .map((v) => v * 1)
        .sort((a, b) => a - b);
}
```

## 중앙값 구하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120811
-   python

```py
def solution(array):
    중앙 = len(array) // 2
    return sorted(array)[중앙]
```

-   js

```js
function solution(array) {
    return array.sort((a, b) => a - b)[Math.floor(array.length / 2)];
}
```

## 직각삼각형 출력하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120823
-   python

```py
n = int(input())
for i in range(n):
    print('*' * (i+1))
```

-   js

```js
// 기본 소스코드
const readline = require("readline");
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout,
});

let input = [];

rl.on("line", function (line) {
    input = line.split(" ");
}).on("close", function () {
    console.log(Number(input[0]));
});

// 풀이
const readline = require("readline");
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout,
});

let input = [];

rl.on("line", function (line) {
    input = line.split(" ");
}).on("close", function () {
    for (let i = 1; i <= +input[0]; i++) {
        console.log("*".repeat(i));
    }
});
```

## 대문자와 소문자

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120893
-   python

```py
def solution(my_string):
    answer = ''
    for i in my_string:
        if i.isupper():
            answer += i.lower()
        else:
            answer += i.upper()
    return answer
```

-   js

```js
function solution(my_string) {
    var answer = "";
    for (let c of my_string)
        answer += c === c.toLowerCase() ? c.toUpperCase() : c.toLowerCase();
    return answer;
}
```

##

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120839
-   python

```py
def solution(rsp):
    d = {'0':'5','2':'0','5':'2'}
    return ''.join(d[i] for i in rsp)

def solution(rsp):
    answer = ''
    for i in rsp:
        if i == "0":
            answer += '5'
        elif i == "2":
            answer += '0'
        else:
            answer += '2'
    return answer

def solution(rsp):
    rsp = rsp.replace('2','s')
    rsp = rsp.replace('5','p')
    rsp = rsp.replace('0','r')
    rsp = rsp.replace('r','5')
    rsp = rsp.replace('s','0')
    rsp = rsp.replace('p','2')
    return rsp
```

-   js

```js
function solution(rsp) {
    let arr = {
        2: 0,
        0: 5,
        5: 2,
    };
    var answer = [...rsp].map((v) => arr[v]).join("");
    return answer;
}
```

## 문자열 정렬하기 (2)

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120911
-   python

```py
def solution(my_string):
    return ''.join(sorted(my_string.lower()))
```

-   js

```js
function solution(my_string) {
    return my_string.toLowerCase().split("").sort().join("");
}
```

## 배열 회전시키기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120844
-   python

```py
from collections import deque

def solution(numbers, direction):
    numbers = deque(numbers)
    if direction == "right": direction = 1
    if direction == "left": direction = -1
    numbers.rotate(direction)
    return list(numbers)

def solution(numbers, direction):
    return [numbers[-1]] + numbers[:-1] if direction == 'right' else numbers[1:] + [numbers[0]]
```

-   js

```js
function solution(numbers, direction) {
    var answer = [];
    if ("right" == direction) {
        numbers.unshift(numbers.pop());
    } else {
        numbers.push(numbers.shift());
    }
    answer = numbers;
    return answer;
}

function solution(numbers, direction) {
    return direction === "right"
        ? [numbers[numbers.length - 1], ...numbers.slice(0, numbers.length - 1)]
        : [...numbers.slice(1), numbers[0]];
}
```

## 피자 나눠 먹기 (2)

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120815
-   python

```py
def solution(n):
    for answer in range(1, 1000):
        if (answer * 6) % n == 0:
            return answer
    return answer

def solution(n):
    i = 1
    while(1):
        if (6 * i) % n == 0:
            return i
        i += 1
```

-   js

```js
const solution = (n) => {
    let piece = 6;

    while (true) {
        if (piece % n === 0) {
            break;
        }
        piece += 6;
    }

    return piece / 6;
};

function solution(n) {
    let pizza = 1;
    while ((pizza * 6) % n) {
        pizza++;
    }
    return pizza;
}
```

## 숫자 찾기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120904
-   python

```py
def solution(num, k):
    num = str(num)
    k = str(k)
    if not k in num:
        answer = -1
    else:
        answer = num.find(k) + 1
    return answer
```

-   js

```js
function solution(num, k) {
    return (
        num
            .toString()
            .split("")
            .map((el) => Number(el))
            .indexOf(k) + 1 || -1
    );
}

function solution(num, k) {
    var answer = num.toString();
    if (answer.includes(k)) {
        return answer.indexOf(k) + 1;
    } else {
        return -1;
    }
}
```

## 주사위의 개수

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120845
-   python

```py
def solution(box, n):
    return (box[0] // n) * (box[1] // n) * (box[2] // n)
```

-   js

```js
function solution(box, n) {
    let [width, length, height] = box;

    return (
        Math.floor(width / n) * Math.floor(length / n) * Math.floor(height / n)
    );
}
```

## 외계행성의 나이

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120834
-   python

```py
def solution(age):
    answer = ''
    for i in str(age):
        answer += str(chr(int(i) + 97))
    return answer
```

-   js

```js
function solution(age) {
    let char = "abcdefghij";
    return Array.from(age.toString())
        .map((t) => char[+t])
        .join("");
}

function solution(age) {
    return age
        .toString()
        .split("")
        .map((v) => "abcdefghij"[v])
        .join("");
}
```

## 암호 해독

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120892
-   python

```py
def solution(cipher, code):
    return cipher[code-1::code]
```

-   js

```js
function solution(cipher, code) {
    return cipher
        .split("")
        .filter((_, index) => (index + 1) % code === 0)
        .join("");
}

function solution(cipher, code) {
    var answer = "";
    for (let i = code - 1; i < cipher.length; i += code) {
        answer += cipher[i];
    }
    return answer;
}
```

## 인덱스 바꾸기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120895
-   python

```py
def solution(my_string, num1, num2):
    answer = my_string[:num1] + my_string[num2] + my_string[num1+1:num2] + my_string[num1] + my_string[num2+1:]
    return answer

def solution(my_string, num1, num2):
    s = list(my_string)
    s[num1],s[num2] = s[num2],s[num1]
    return ''.join(s)
```

-   js

```js
function solution(my_string, num1, num2) {
    my_string = my_string.split("");
    [my_string[num1], my_string[num2]] = [my_string[num2], my_string[num1]];
    return my_string.join("");
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
