## 팁 계산하기

### - 코드

```
# 문제
#If the bill was $150.00, split between 5 people, with 12% tip.
#Each person should pay (150.00 / 5) * 1.12 = 33.6
#Format the result to 2 decimal places = 33.60
#Tip: There are 2 ways to round a number.

#Write your code below this line 👇
print("Welcome to the tip calculator!")
total_bill = input("What was the total bill? $")
percent = input("How much tip would you like to give? 10, 12, or 15? ")
split_people = input("How many people to split the bill? ")

total_bill  = float(total_bill)
percent = float(percent)/100 + 1
split_people = int(split_people)

print(f"total_bill : {total_bill}")             # 150
print(f"percent : {percent}")                   # 1.13
print(f"split_people : {split_people}")         # 5

result = (total_bill / split_people) * percent
fin_result = "${:.2f}".format(round(result,2))  # 33.90
# 🐸 java : System.out.printf("%.2f\n",3.2542);   //3.25

print(f"Each person should pay: {fin_result}")
```

### - 정리

- <h4>타입 확인 및 타입 변경</h4>
    
    ```
    - type("123")       >>> <class 'str'>               
    - int("123")        >>> 123
    - float("123.45")   >>> 123.45
    - str(123)          >>> "123"
    ```

- <h4>반올림</h4>

  1. // 기호

     ```
     round_result_2 = 8//3
     print(round_result_2)        # 2
     print(type(round_result_2))  # int
     ```

  2. round
     - round(수식, 자리수)
       ```
       print(round(1.23456))        # 1
       print(round(1.23456, 0))     # 1.0
       print(round(1.23456, 1))     # 1.2
       print(round(1.23456, 2))     # 1.23
       print(round(1.23456, 3))     # 1.235
       print(round(1.23456, 4))     # 1.2346
       ```

- <h4>f_string</h4>

  - 여러 자료형 String으로 사용

    ```
    score = 10        # int
    height = 160      # float
    isWining = True   # boolean

    # ❌ error
    # print("your scroe is " + score + "your height is " + height + "your are winning is " + isWining)

    # not error
    print(f"your scroe is {score}, your height is {height}, your are winning is {isWining}")

    # 🐸 javaScript : `text ${}`
    ```

- <h4>소수점 두자리</h4>

  - format 방법 2가지

    1. [ : ] 사용 | 변수 타입 관계 없이 {} 해주면 된다
    2. [ % ] 사용 | 변수타입에 따라서 %s, %d, %f 구분해서 써줘야 함

  - 1.20 일때 1.2로 보여지는 부분 수정 방법

    ```
    "{:.2f}".format(1.20)
    print('%.2f'%(1.20))
    # 🐸 java : System.out.printf("%.2f\n",1.20);

    print(1.20)                     # 1.2
    print("{:.2f}".format(1.20))    # 1.20
    ```

    - [참고 블로거](https://firedino.tistory.com/56)
    - [자바 format 참고](https://github.com/hyeah0/SmartWeb_Contents_WebApplication_developer_class/blob/main/1_Java/day01_%EC%9E%90%EB%B0%94%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0.md)

- <h4>String[2]</h4>
   
   - String의 n번째 글자 추출
    ```
    print("Hello"[1])  # e
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
        <td>텍스트 변수 혼합사용</td>
        <td>print(f"텍스트 {변수명}")</td>
        <td>`텍스트 ${변수명}`</td>
        <td>System.out.println("텍스트" + 변수명)</td>
    </tr>
    <tr>
        <td>format</td>
        <td>"{:.2f}".format(1.20)
        <br>print('%.2f'%(1.20))
        </td>
        <td>toFixed(fixed)
        <br>getFloatFixed(1.223, 2)
        </td>
        <td>System.out.printf("%.2f\n",1.20)</td>
    </tr>
</table>

- javascript : toFixed(fixed)
  - 소수점 둘 째자리까지 반올림하고 특정 변수까지 0으로 표시하는 함수이다.
- javascript : getFloatFixed(1.223, 2)
  - 1.223에서 소수점 둘째 자리까지 반올림
- [참고 블로거](https://shwjdqls.github.io/javascript-show-float-number/)
