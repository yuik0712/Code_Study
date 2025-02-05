![wjdqlswh 파이썬](https://github.com/user-attachments/assets/48ab558d-7aa7-4bfa-b377-61fc277d3ac1)

# 변수와 자료형 
### 정수형, 실수형, 자료형
- <b>정수형(int)</b>: 정수를 저장하는 자료형
- <b>실수형(float)</b>: 소수점이 있는 숫자를 저장하는 자료형
- <b>문자열(str)</b>: 문자나 문자의 집합을 저장하는 자료형
  - 파이썬에서 변수는 값을 저장하는 공간으로, 변수에 자료형을 별도로 명시하지 않아도 됨.
  - 문자열의 경우
    - 작은 따옴표('') 또는 큰 따옴표("")를 사용하여 표현할 수 있으며, 여러 줄의 문자열의 삼중 따옴표(''') 또는 (""")를 사용함.
      <br/>
      또한, 문자열의 연산을 통해 문자열을 결합하거나 반복할 수 있다.
- 불리언 자료형(Boolean)과 None
  - 불리언 자료형(Boolean): 참(True)과 거짓(False)을 나타내는 자료형
    - Bool 타입이며, 1은 true, 0은 False로 변환 가능
    - 조건문이나 논리 연산에서 주료 사용
    - 비교 연산자(>, <, ==, !=, >=, <=)와 논리 연산자(and, or, not)의 결과로 얻을 수 있음
  - None: 값이 없음을 나타내는 특별한 자료형
    - NoneType 타입을 가짐 -> type(none) 하면 ```<class 'NoneType'>``` 출력
    - 값이 없음을 나타내는 용도로 사용됨
    - 논리적으로 ```False```로 취급됨 (하지만 ```False```와는 다르다)
    - 변수를 초기화할 때 유용함 (```변수 = None```)
    - 함수에서 반환할 값이 없을 때 사용됨(```return None```)

#### 예제코드 
```
# 정수형 변수
num1 = 10 // num1이라는 정수형 변수를 만들고, 값과 자료형을 출력
// type(num1)은 num1의 자료형을 알려줌
print(f"num1: {num1}, type: {type(num1)}") 

# 실수형 변수
num2 = 3.14 // num2라는 실수형 변수를 만들고, 동일하게 값과 자료형을 출력
print(f"num2: {num2}, type: {type(num2)}")

# 문자열 변수
num3 = "Hello, World!" // num3라는 문자열 변수를 만들고, 이거 역시 동일하게 값과 자료형 출력
// greeting 변수가 없어서 에러가 발생할 수 있음! (실제로 num3를 직접 출력하거나 greeting = "" 처럼 변수를 맞추면 사용이 가능하다)
print(f"greeting: {greeting}, type: {type(num3)}")

# 여러 줄의 문자열
multiline = '''파이썬 // 작은따옴표 세 개(''')를 사용하면 여러 줄로 된 문자열을 쉽게 담을 수 있음.
프로그래밍 
환영합니다.'''
print(multiline) // 출력하면 엔터(줄바꿈)도 그대로 표현된다

# 문자열 연산
name = "홍길동"
message = "안녕하세요, " + name + "님!" // + 연산자를 이용하면 문자열끼리 이어 붙일 수 있음
print(message) // 결과 => "안녕하세요, 홍길동님!" 문자열 완성
```

```
# 불리언(Boolean) 과 None 예제 코드

# 불리언(Boolean) 예제 코드
# 불리언 값
is_python_fun = True // is_python_fun 이라는 변수를 생성하였고, true 값을 줌
is_snowing = False // is_snowing 이라는 변수를 생성하였고, False 값을 줌

# 출력 관련 부분 (True, False)
# True (f-string을 사용하여 is_python_fun 이라는 변수의 값과 데이터 타입을 출력하는 코드)
print(f"is_python_fun: {is_python_fun}, type: {type(is_python_fun)}")
# False (f-string을 사용하여 is_snowing 이라는 변수의 값과 데이터 타입을 출력하는 코드)
print(f"is_snowing: {is_snowing}, type: {type(is_snowing)}")

# 정수를 불리언으로 변환
print(bool(1)) # 출력: True
print(bool(0)) # 출력: False

# 비교 연산 결과
print(10 > 5) # True
print(3 == 4) # False

# 논리 연산
print(True and False) # False
print(True or False) # True
print(not True) # False

---
# None 예제 코드

# ✅ 기본적인 사용방법
# 변수를 None으로 초기화
nothing = None
print(f"nothing: {nothing}, type: {type(nothing)}") # 출력: nothing: None, type: <class 'NoneType'>

# ✅ None은 논리적으로 False로 취급됨
print(bool(None)) # 출력: False

if not None:
  print("None은 논리적으로 False!") # 출력: None은 논리적으로 False!

# ✅ None을 활용한 변수 초기화
# 아직 값이 정해지지 않은 변수
user_name = None

# 조건에 따라 값 할당
if user_name is None:
  user_name = "Guest"

print(user_name) # 출력: Guest

# ✅ 함수에서 None 반환
def do_nothing():
  return None

result = do_nothing()
print(result) # 출력: None
```

#### 🔥 불리언 vs None 차이점 정리
|자료형|값|논리적 의미|데이터 타입|
|------|---|---|-----|
|```True```|1|참 (```True```)|```bool```|
|```False```|0|거짓(```False```)|```bool```|
|```None```|없음|거짓 (```False``` 취급)|```NoneType```|
- ```Boolean```(```True```, ```False```)은 논리 연산을 위해 사용되며, ```1```, ```0```과 변환 가능함
- ```None```은 값이 없음을 나타내며, ```False```로 취급되지만 ```False```와는 다름
- 변수를 초기화할 때, 함수의 반환값이 없을 때 등 다양한 상황에서 활용됨

### 복소수 (Complex) 주요 특징 및 사용법
1. 복소수 생성
   - 복소수는 a + b; 형태로 나타내며, 여기서 a는 실수 부분이고 b는 허수 부분입니다. (j는 허수 단위를 나타낸다.)
   - 복소수 생성하는 방법 (두가지)
     - complex(a, b)를 사용하여 a + b; 복소수를 생성
     - 직접 a + b; 형태로 입력
       ```
       z1 = complex(3, 4) # 3 + 4;
       z2 = 3 + 4; # 3 + 4;
       ```
2. 복소수의 속성
   - complex 객체의 두 가지 속성
     - .real: 복소수의 실수 부분
     - .imag: 복소수의 허수 부분
  ```
  z = 3 + 4j
  print(z.real) # 출력: 3.0
  print(z.imag) # 출력: 4.0
  ```
3. 복소수 연산
   - 덧셈, 뺄셈, 곱셈, 나눗셈을 포함한 다양한 산술 연산 지원 > 연산 결과는 모두 complex 객체로 반환됨
     ```
     z1 = 3 + 4j
     z2 = 1 - 2j

     add_result = z1 + z2 # (3 + 4j) + (1 - 2j) = 4 + 2j
     sub_result = z1 - z2 # (3 + 4j) - (1 - 2j) = 2 + 6j
     mul_result = z1 * z2 # (3 + 4j) * (1 - 2j) = 11 + 2j
     div_result = z1 / z2 # (3 + 4j) / (1 - 2j) = -1 + 2j

     print(add_result) # 출력: (4 + 2j)
     print(sub_result) # 출력: (2 + 16j)
     print(mul_result) # 출력: (11 + 2j)
     print(div_result) # 출력: (-1 + 2j)
     ```
4. 복소수의 절대값
  - 복소수의 절댓값(크기)은 피타고라스 정리를 사용하여 계산됨.
    <br>
    #abs()함수를 사용하여 절댓값을 구할 수 있음.
  ```
  z = 3 + 4j
  magnitude = abs(z) # sqrt(3**2 + 4**2) = 5.0
  print(magnitude) # 출력: 5.0
  ```
5. 복소수의 복소켤레
   - 복소수의 허수 부분의 부호를 바꾼 값 (complex 객체의 conjugate() 메서드를 사용하여 복소켤레를 구할 수 있음)
   ```
   z = 3 + 4j
   conjugate_z = z.conjugate() # 3 - 4j
   print(conjugate_z) # 출력: (3 - 4j)
   ```
6. 극좌표 변환
   - 복소수를 극좌표로 변환할 때, cmath 모듈을 사용할 수 있음 (복소수의 크기와 각도를 구할 수 있음)
   ```
   import cmath

   z = 3 + 4j
   r, theta = cmath.polar(z) # 극좌표 변환
   print(r) # 출력: 5.0 (절댓값)
   print(theta) # 출력: 0.9272952180016122 (라디안 단위의 각도)

   # 극좌표를 직교좌표로 변환
   z_rect = cmath.rect(r, theta)
   print(z_rect)  # 출력: (3.0000000000000004+3.9999999999999996j)
   ```
  <br>
  
  ```
  # 극좌표와 직교좌표란?
  - 직교좌표(Cartesian Coordinates): 우리가 일반적으로 사용하는 (x,y) 좌표계 (복소수에서는 a + bj 형태로 표현됨
  - 극좌표(Polar Coordinated): 원점을 기준으로 거리를 r, 각도를 θ (라디안 단위)로 표현하는 방식
  ```
7. 복소수의 응용
   - 복소수는 물리학, 공학, 신호 처리, 전기 회로 이론, 제어 이론 등에서 광범위하게 사용됨 (예를 들어, 교류 전기 회로에서 임피던스를 계산할 때 사용)

### 핵심 포인트 정리
- <b>변수(Variable)</b>: 데이터를 저장하는 공간(num1, num2, ...등)
- <b>자료형(Type)</b>: 정수(int), 실수(float), 문자열(str) 등 어떤 종류의 데이터인가를 나타내는 것
- <b>출력(print 함수)</b>: print() 안에 변수나 문자열을 넣어 콘솔에 보여줌
- <b>문자열 연산</b>: + 연산자로 문자열을 이어 붙이거나, f"..."방식을 쓰면 {변수}처럼 변수를 간단히 포함할 수 있다.
- <b>여러 줄 문자열</b>: '''...''' 또는 """..."""를 쓰면 편하게 여러 줄을 표현할 수 있음

### 추가적으로, ```NameError: name 'greeting' is not defined```의 경우
- <b>NameError</b>: 정의되지 않은 (또는 선언되지 않은)변수를 사용하려 할 때 발생하는 에러
  - 코드 예시 (올바른 변수 선언)
    ```
    # 문자열 변수
    greeting = "Hello, World!" # 여기에 greeting 변수를 선언해줍니다.
    print(f"greeing: {greeting}, type: {type(greeting)}")
    ```
    - greeting 변수를 먼저 선언하였기 때문에, print 구문에서 greeting을 문제없이 사용할 수 있음
      
  - 코드 예시 (올바르지 않은 변수 선언)
    ```
    print(f"greeing: {greeting}, type: {type(greeting)}")
    greeting = "Hello, World!" # 여기에 greeting 변수를 선언해줍니다.
    ```

### 정리
- <b>NameError</b>: 정의(선언)되지 않은 변수를 참조할 때 발생하는 에러
- 해결 방법
  - 변수르 사용하기 전에 반드시 선언해야 함.
  - 코드에서 변수가 쓰이는 순서를 체크하며 선언해야 하고, 사용 순으로 두면 문제를 해결할 수 있음

# 블로그 참조
- https://gdngy.tistory.com/74 (GDNDY님 티스토리)
https://sosodev.tistory.com/entry/Python-complex-%ED%81%B4%EB%9E%99%EC%8A%A4%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%B4%EC%84%9C-%EB%B3%B5%EC%86%8C%EC%88%98-%EB%8B%A4%EB%A3%A8%EA%B8%B0
