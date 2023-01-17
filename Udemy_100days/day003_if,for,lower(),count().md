## 보물찾기

### - 코드

- [코드 실행](https://replit.com/@hyeah0/day003find-treasure#main.py)

- flow chart

<img src="https://github.com/hyeah0/Python/blob/main/Udemy_100days/image/day003_FlowChart.png" width="80%">

### - 정리

- [추가 코드 실행](https://replit.com/@hyeah0/day003ifforlowercount#main.py)

#### - if elif else

```
if 조건1:
    조건1이 참일때 실행문
elif 조건2:
    조건1이 거짓이고 조건2가 참일때 실행문
else:
    조건1, 조건2가 모두 거짓일때 실행문
```

#### - even, odd

- even : 짝수
- odd : 홀수

#### - 윤년 구하기

- year를 4로 나눴을때 남은값이 0이면 윤년
- year를 4로 나눴을때 남은값이 0이 아니거나,
- year를 100으로 나눴을때 남은값이 0 이고, 400으로 나눴을때 남은 값이 0이 아닐경우 윤년이 아니다.

```
year % 4                         # 0 >>> 윤년
year % 100 and year % 400        # 0 and 0이 아님 >>> 윤년X
year % 400                       # 0 >>> 윤년
```

#### - and, or

- 조건식1 and 조건식2

  - 조건식1, 조건식2 모두 true여야 true 이다.

- 조건식3 or 조건식4
  - 조건식3, 조건식4 중 한개이상 true면 true 이다.

```
if(percent < 10 or percent > 90 ): # less then 10 or greater than 90
    print(f'Your score is {percent}, you go together like coke and mentos.')
elif(percent >= 40 and percent <= 50):  # between 40 and 50
    print(f'Your score is {percent}, you are alright together.')
else:
    print(f'Your score is {percent}')
```

#### - Stirng.lower(), String.count()

- String.lower() : String 값에 대문자가 있으면 소문자로 변경
- String.count('a') : String 값에 'a'의 갯수

```
apple = 'Apple'
apple.lower()       >>> apple
apple.count('p')    >>> 2
```

#### - for i in 배열명

```
str_true = ['t','r','u','e']
for i in str_true:
    print(i)    >>> t, r, u, e
```

### - 비교

<table>
    <tr>
        <th>-</th>
        <th>Python</th>
        <th>JavaScript</th>
        <th>Java</th>
    </tr>
    <tr>
        <td>if, else</td>
        <td>if(조건식1): 실행문
        <br>elif(조건식2): 실행문
        <br>else: 실행문
        </td>
        <td colspan="2">
        if(조건식1){ 실행문 }
        <br>else if(조건식2){ 실행문 }
        <br>else{실행문}
        </td>
    </tr>
    <tr>
        <td>삼항 연산자</td>
        <td>[True일때] if a > 5 else [False일때]</td>
        <td colspan="2">조건식1? true일때 실행문 : false일때 실행문
        </td>
    </tr>
    <tr>
        <td>논리연산자</td>
        <td>and, or, not</td>
        <td colspan="2">&&, ||, !</td>
    </tr>
</table>

- java, javascript 에서 if, for, while.. 사용시 실행문 작성 부분에 {} 로 감싼다.
  <br> 실행문이 한줄일 경우 생략 가능
- python 에서는 조건식 뒤에 : 을 사용 하고 {} 를 따로 사용하지 않는다.
