## 두 변수를 받아 락밴드 이름을 만들어 보자

### 코드

```
print("Welcome to the Band Name Generator.")

// input 값을 받아 변수에 지정
street = input("What's the name of the city you grew up in?\n")
pet = input("What's your pet's name?\n")

print("Your band name could be " + street + " " + pet)
```

### 정리

- print

  - console 창에 가로 값 보여줌

- \n

  - 엔터

- input

  - 사용자에게 데이터를 값을 받을 때 사용

- 변수
  - 변수 지정시 let, int와 같이 따로 붙이는 게 없다.

<br>
<hr>

### 비교

<table>
    <tr>
        <th>-</th>
        <th>Python</th>
        <th>JavaScript</th>
        <th>Java</th>
    </tr>
    <tr>
        <td>console창</td>
        <td>print()</td>
        <td>console.log()</td>
        <td>System.out.println()</td>
    </tr>
    <tr>
        <td>입력받기</td>
        <td>input()</td>
        <td>prompt("입력창에 보여질 메세지");</td>
        <td>Scanner sc = new Scanner
        <br>sc.nextInt() / sc.nextLine()
        </td>
    </tr>
    <tr>
        <td>변수지정</td>
        <td>변수명 = "a"</td>
        <td>let a = "a"
        <br>const a = "a"
        </td>
        <td> String a = "a"
        <br> Final String A = "a"
        </td>
    </tr>
</table>

- [자바 입력값 받기 추가 참고](https://github.com/hyeah0/SmartWeb_Contents_WebApplication_developer_class/blob/main/1_Java/%EA%B0%92%EC%9E%85%EB%A0%A5%EB%B0%9B%EA%B8%B0.md)
