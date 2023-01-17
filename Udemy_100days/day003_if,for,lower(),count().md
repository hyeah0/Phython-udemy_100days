## 보물찾기

### - 코드

- [코드 실행](https://replit.com/@hyeah0/day003find-treasure#main.py)

```
print('''
*******************************************************************************
          |                   |                  |                     |
 _________|________________.=""_;=.______________|_____________________|_______
|                   |  ,-"_,=""     `"=.|                  |
|___________________|__"=._o`"-._        `"=.______________|___________________
          |                `"=._o`"=._      _`"=._                     |
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
 _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______
|                   | |o;    `"-.o`"=._``  '` " ,__.--o;   |
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
/______/______/______/______/______/______/______/______/______/______/_____ /
*******************************************************************************
''')
print("보물섬에 오신걸 환영합니다.")
print("모험을 떠나 보물섬에 숨겨진 보물을 찾아보세요")

#https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Treasure%20Island%20Conditional.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1oDe4ehjWZipYRsVfeAx2HyB7LCQ8_Fvi%26export%3Ddownload

#Write your code below this line 👇
choose_side = ''
choose_action = ''
choose_door_color = ''

choose_side = input('두갈래 길이 나왔습니다. 왼쪽 또는 오른쪽 어디로 가겠습니까? Type "왼쪽" or "오른쪽" >>> ')
if(choose_side == '오른쪽'):
    print('함정 구멍에 빠졌습니다.')
    print('게임 종료')

else:
    choose_action = input('강에 도착했습니다. 수영해서 가시겠습니까? 보트를 기다리겠습니까? Type "수영" or "기다림" >>> ' )
    if(choose_action == '수영'):
        print('악어에게 공격 당했습니다.')
        print("게임 종료")
    else:
        choose_door_color = input('강을 건너 길을 걷다보니 집이 3개가 있습니다. 집의 문 색깔이 빨강색, 노란색, 파란색이 이며 어떤 색깔의 문을 열겠습니까? Type "빨강" or "노랑" or "파랑" >>> ')
        if(choose_door_color == '빨강'):
            print('집 안에 불이 가득합니다.')
            print('게임 종료')

        elif(choose_door_color == '파랑'):
            print('집 안에 자물쇠로 잠겨진 보물상사가 있습니다. 열쇠를 찾아야합니다.')
            choose_search = input('주변을 살펴보니 액자, 어항, 서랍이 보입니다. 어디를 확인 하시겠습니까? Type "액자" or "어항" or "서랍" >>> ')

            if(choose_search == '액자'):
                print('액자 안을 살펴보다가 손을 베였습니다.')
                print('게임 종료')

            elif(choose_search == '어항'):
                print('물고기들이 공격해서 어항 안을 찾아 볼 수 없습니다.')
                print('게임 종료')

            elif(choose_search == '서랍'):
                print('서랍 안에서 열쇠를 찾았습니다.')
                print('찾은 열쇠로 보물상자를 열었습니다. 안에는 보물이 가득 들어있습니다.')

        elif(choose_door_color == '노랑'):
            print('집 안에 가스가 가득합니다.')
            print('게임 종료')
        else:
            print('보물찾기를 포기 했군요... 게임을 종료합니다.')
```

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
