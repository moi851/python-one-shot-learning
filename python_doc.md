## 1. 파이썬 소개
### 파이썬이란 무엇인가?
파이썬은 간결하고 읽기 쉬운 문법을 가진 고급 프로그래밍 언어입니다. 1991년에 귀도 반 로섬(Guido van Rossum)이 발표했으며, 사용하기 쉬운 구문과 높은 생산성으로 인해 많은 개발자들이 애용하고 있습니다. 파이썬은 웹 개발, 데이터 분석, 머신러닝, 스크립트 작성 등 다양한 용도로 사용됩니다.

### 파이썬의 특징과 장점
- **간결한 문법**: 복잡한 코드를 단순하게 작성할 수 있어 초보자에게 적합합니다.
- **크로스 플랫폼**: 윈도우, 맥OS, 리눅스 등 다양한 운영체제에서 실행할 수 있습니다.
- **강력한 라이브러리**: 풍부한 표준 라이브러리와 서드파티 라이브러리 지원을 통해 다양한 기능을 쉽게 구현할 수 있습니다.
- **커뮤니티 지원**: 큰 사용자 커뮤니티 덕분에 다양한 예제 코드와 해결 방법을 쉽게 찾을 수 있습니다.

### 파이썬 설치 및 환경 설정
1. 파이썬 공식 웹사이트(https://www.python.org/)에서 파이썬을 다운로드합니다.
2. 설치 과정에서 "Add Python to PATH" 옵션을 체크하여 환경 변수를 설정합니다.
3. 설치 후, 터미널에서 `python --version`을 입력하여 설치가 완료되었는지 확인합니다.


## 2. 기본 문법 익히기
### 변수와 자료형
파이썬의 변수는 데이터 저장소 역할을 합니다. 변수에 값을 할당할 때는 별도의 타입을 명시할 필요가 없으며, 변수에 따라 타입이 결정됩니다.

예시:
```python
name = "Alice"  # 문자열
age = 25         # 정수
height = 5.9     # 실수
is_student = True # 논리형
```

### 기본 연산자
- **산술 연산자**: `+`, `-`, `*`, `/`, `//`, `%`, `**` (덧셈, 뺄셈, 곱셈, 나눗셈, 몫, 나머지, 거듭제곱)
- **비교 연산자**: `==`, `!=`, `>`, `<`, `>=`, `<=` (동등, 비동등, 크기 비교)
- **논리 연산자**: `and`, `or`, `not` (논리 연산)

### 입력과 출력
- **입력**: `input()` 함수를 사용해 사용자로부터 입력을 받을 수 있습니다.
- **출력**: `print()` 함수를 사용해 콘솔에 내용을 출력합니다.

예시:
```python
name = input("이름을 입력하세요: ")
print("안녕하세요,", name)
```

### 주석 처리
- **한 줄 주석**: `#` 기호를 사용합니다.
- **여러 줄 주석**: 작은따옴표 세 개(`'''`) 또는 큰따옴표 세 개(`"""`)를 사용합니다.


## 3. 제어문
### 조건문 (if, elif, else)
조건문은 특정 조건에 따라 코드 블록을 실행하거나 실행하지 않도록 합니다. 조건이 참(True)일 때 코드 블록이 실행됩니다.

#### 조건문의 기본 구조
조건문은 다음과 같은 구조를 갖습니다.
- **if**: 첫 번째 조건을 확인하고, 조건이 참이면 실행합니다.
- **elif**: 위 조건이 거짓일 때 추가로 다른 조건을 확인합니다. 여러 개의 `elif`가 사용될 수 있습니다.
- **else**: 모든 `if`와 `elif` 조건이 거짓일 때 실행됩니다.

예시:
```python
age = 18
if age >= 18:
    print("성인입니다.")
elif age >= 13:
    print("청소년입니다.")
else:
    print("어린이입니다.")
```
이 예시에서 `age`가 18 이상이면 "성인입니다"가 출력되고, 그렇지 않으면 13 이상인 경우 "청소년입니다"가 출력됩니다. 모든 조건이 거짓일 경우 "어린이입니다"가 출력됩니다.

#### 중첩 조건문
조건문은 중첩될 수 있습니다. 하나의 조건문 안에 또 다른 조건문을 넣어 더 복잡한 논리를 처리할 수 있습니다.

예시:
```python
age = 20
is_student = True

if age >= 18:
    if is_student:
        print("성인이면서 학생입니다.")
    else:
        print("성인이지만 학생은 아닙니다.")
else:
    print("미성년자입니다.")
```
이 경우, `age`가 18 이상이고 `is_student`가 `True`이면 "성인이면서 학생입니다"가 출력됩니다.

#### 조건 표현식 (삼항 연산자)
파이썬에서는 조건문을 한 줄로 표현할 수도 있습니다. 이를 **조건 표현식**이라고 부르며, 종종 간단한 조건에 따라 값을 결정할 때 사용됩니다.

예시:
```python
age = 20
status = "성인" if age >= 18 else "미성년자"
print(status)  # 성인
```
위 코드에서는 `age`가 18 이상인 경우 `"성인"`이, 그렇지 않은 경우 `"미성년자"`가 `status`에 저장됩니다.


### 반복문 (for, while)
반복문은 특정 코드 블록을 여러 번 실행하기 위해 사용됩니다.

#### for 반복문
**for** 반복문은 주로 리스트, 튜플, 문자열 등과 같은 **반복 가능한(iterable)** 객체를 순회할 때 사용됩니다. `range()` 함수를 사용하여 특정 횟수만큼 반복할 수도 있습니다.

예시:
```python
# 리스트 순회
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# 숫자 범위 반복
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4 출력
```

#### while 반복문
**while** 반복문은 조건이 참인 동안 계속해서 코드 블록을 반복합니다. 조건이 거짓이 되면 반복이 종료됩니다.

예시:
```python
count = 0
while count < 5:
    print(count)
    count += 1  # count 값을 1씩 증가시킵니다.
```
이 코드는 `count`가 5보다 작을 때까지 반복됩니다.

#### 무한 루프
**무한 루프**는 종료 조건이 없는 반복문으로, `while True:`와 같은 방식으로 작성됩니다. 무한 루프는 특정 이벤트나 `break` 문을 통해 반복을 중단할 수 있습니다.

예시:
```python
while True:
    user_input = input("종료하려면 'exit'을 입력하세요: ")
    if user_input == 'exit':
        break
```
이 코드는 사용자가 `"exit"`을 입력할 때까지 계속 실행됩니다.

### 반복문 제어 (break, continue)
반복문을 제어하기 위해 **break**와 **continue** 문을 사용할 수 있습니다.

- **break**: 현재 반복을 즉시 종료하고, 반복문을 완전히 빠져나옵니다.
- **continue**: 현재 반복만 건너뛰고, 다음 반복을 계속 진행합니다.

예시:
```python
for i in range(10):
    if i == 5:
        break  # i가 5일 때 반복을 종료합니다.
    print(i)  # 0, 1, 2, 3, 4 출력

for i in range(10):
    if i % 2 == 0:
        continue  # i가 짝수이면 건너뜁니다.
    print(i)  # 1, 3, 5, 7, 9 출력
```

## 4. 자료 구조
### 리스트 (List)
리스트는 여러 값을 순서대로 저장할 수 있는 자료형입니다. 대괄호 `[]`를 사용하여 선언합니다.

예시:
```python
fruits = ["apple", "banana", "cherry"]
print(fruits[0])  # apple
```

### 튜플 (Tuple)
튜플은 리스트와 비슷하지만, 한 번 생성하면 값을 변경할 수 없습니다. 소괄호 `()`를 사용하여 선언합니다.

예시:
```python
coordinates = (10, 20)
print(coordinates[1])  # 20
```

### 집합 (Set)
집합은 중복되지 않는 고유한 값들을 저장합니다. 중괄호 `{}`를 사용하여 선언합니다.

예시:
```python
unique_numbers = {1, 2, 3, 3, 4}
print(unique_numbers)  # {1, 2, 3, 4}
```

### 딕셔너리 (Dictionary)
딕셔너리는 키-값 쌍으로 데이터를 저장합니다. 중괄호 `{}`를 사용하여 선언합니다.

예시:
```python
person = {"name": "Alice", "age": 25}
print(person["name"])  # Alice
```


## 5. 함수
### 함수 정의와 호출
함수는 코드의 재사용성을 높이기 위해 사용됩니다. `def` 키워드를 사용해 정의합니다. 함수 이름은 소문자로 작성하며, 필요에 따라 밑줄(`_`)을 사용해 가독성을 높일 수 있습니다.

예시:
```python
def greet():
    print("Hello, World!")

greet()  # Hello, World!
```

함수에는 하나 이상의 매개변수를 전달할 수 있으며, 이를 통해 다양한 입력값에 대해 동일한 작업을 수행할 수 있습니다.

### 매개변수와 반환값
함수는 매개변수를 받을 수 있으며, `return` 키워드를 사용해 값을 반환할 수 있습니다. 함수에는 기본 매개변수 값도 설정할 수 있어, 호출 시 해당 인자를 생략할 수 있습니다.

예시:
```python
def add(a, b=5):
    return a + b

result = add(3)
print(result)  # 8
```

키워드 인수를 사용하여 함수 호출 시 매개변수의 순서를 무시할 수 있습니다.

예시:
```python
def introduce(name, age):
    print(f"이름: {name}, 나이: {age}")

introduce(age=25, name="Alice")  # 이름: Alice, 나이: 25
```

### 가변 인자와 키워드 인자
함수에 전달하는 인자의 개수가 가변적일 때는 `*args`와 `**kwargs`를 사용할 수 있습니다.
- `*args`: 위치 인자를 가변적으로 받습니다.
- `**kwargs`: 키워드 인자를 가변적으로 받습니다.

예시:
```python
def greet_all(*args):
    for name in args:
        print(f"Hello, {name}!")

greet_all("Alice", "Bob", "Charlie")

# Hello, Alice!
# Hello, Bob!
# Hello, Charlie!

def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=25, city="Seoul")

# name: Alice
# age: 25
# city: Seoul
```

### 람다 함수
람다 함수는 간단한 익명 함수입니다. `lambda` 키워드를 사용하여 정의하며, 주로 간단한 동작을 수행할 때 사용합니다. 람다 함수는 한 줄로 표현 가능하며, 여러 매개변수를 받을 수 있습니다.

예시:
```python
square = lambda x: x * x
print(square(4))  # 16

multiply = lambda a, b: a * b
print(multiply(3, 5))  # 15
```

람다 함수는 `map()`, `filter()`, `sorted()` 등의 함수와 함께 자주 사용됩니다.

예시:
```python
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x * x, numbers))
print(squared_numbers)  # [1, 4, 9, 16, 25]
```

### 재귀 함수
재귀 함수는 자기 자신을 호출하는 함수입니다.

예시:
```python
def factorial(n):
    if n == 1:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # 120
```


## 6. 모듈과 패키지
### 표준 라이브러리 사용하기
파이썬에는 기본적으로 제공되는 표준 라이브러리가 많습니다. 예를 들어 `math` 모듈을 사용해 수학 연산을 할 수 있습니다.

예시:
```python
import math
print(math.sqrt(16))  # 4.0
```

### 모듈 가져오기 (import)
`import` 키워드를 사용해 모듈을 가져올 수 있습니다.

예시:
```python
import random
print(random.randint(1, 10))  # 1부터 10 사이의 무작위 정수
```

### 패키지 설치와 활용 (pip)
`pip`는 파이썬의 패키지 관리 도구로, 외부 패키지를 설치하는 데 사용됩니다.

예시:
```sh
pip install requests  # requests 라이브러리 설치
```


## 7. 파일 입출력
### 파일 읽기와 쓰기
- **파일 쓰기**: 파일을 쓰기 모드(`w`)로 열고 데이터를 저장합니다.
- **파일 읽기**: 파일을 읽기 모드(`r`)로 열고 데이터를 읽습니다.

예시:
```python
# 파일 쓰기
with open("example.txt", "w") as file:
    file.write("Hello, Python!")

# 파일 읽기
with open("example.txt", "r") as file:
    content = file.read()
    print(content)  # Hello, Python!
```

### 텍스트 파일과 CSV 파일 처리
CSV 파일을 처리할 때는 `csv` 모듈을 사용합니다.

예시:
```python
import csv

with open("data.csv", "r") as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

### 예외 처리
파일 작업 중 오류가 발생할 수 있으므로 예외 처리를 사용하는 것이 좋습니다.

예시:
```python
try:
    with open("nonexistent.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("파일을 찾을 수 없습니다.")
```


## 8. 객체 지향 프로그래밍
### 클래스와 객체
파이썬은 객체 지향 프로그래밍(OOP)을 지원하며, 클래스는 객체를 생성하기 위한 청사진입니다. 클래스는 속성(데이터)과 메서드(동작)를 정의할 수 있습니다.

클래스를 정의할 때 `__init__()` 메서드는 객체가 생성될 때 자동으로 호출되며, 객체의 초기 속성을 설정하는 데 사용됩니다. `self` 매개변수는 현재 인스턴스를 참조하며, 클래스 내에서 속성을 정의하고 메서드를 호출하는 데 사용됩니다.

예시:
```python
class Dog:
    def __init__(self, name, age):
        self.name = name  # 이름 속성
        self.age = age    # 나이 속성

    def bark(self):
        print(f"{self.name}가 짖습니다: Woof!")

    def get_age(self):
        return self.age

    def set_age(self, age):
        if age > 0:
            self.age = age
        else:
            print("나이는 양수여야 합니다.")

my_dog = Dog("Buddy", 3)
print(my_dog.name)  # Buddy
my_dog.bark()  # Buddy가 짖습니다: Woof!
print(f"나이: {my_dog.get_age()}")  # 나이: 3
my_dog.set_age(4)
print(f"변경된 나이: {my_dog.get_age()}")  # 변경된 나이: 4
```

클래스는 객체를 생성하기 위한 틀이며, 객체는 클래스의 인스턴스입니다. 여러 객체를 생성하여 다양한 데이터를 저장할 수 있습니다.

### 속성과 메서드
- **속성**: 객체의 데이터를 저장하는 변수입니다.
- **메서드**: 객체가 수행할 수 있는 동작을 정의한 함수입니다.

예시:
```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def drive(self):
        print(f"{self.brand} {self.model}가 달립니다.")

my_car = Car("Toyota", "Corolla")
my_car.drive()  # Toyota Corolla가 달립니다.
```

### 상속과 다형성
상속은 기존 클래스의 기능을 물려받아 새로운 클래스를 만드는 기능입니다. 상속을 통해 코드의 재사용성을 높이고, 공통 기능을 쉽게 확장할 수 있습니다.

예시:
```python
class Animal:
    def __init__(self, species):
        self.species = species

    def sound(self):
        print("Some sound")

class Cat(Animal):
    def __init__(self, name, age):
        super().__init__("Cat")  # 부모 클래스의 생성자 호출
        self.name = name
        self.age = age

    def sound(self):
        print("Meow")

    def info(self):
        print(f"이름: {self.name}, 나이: {self.age}, 종: {self.species}")

my_cat = Cat("Whiskers", 2)
my_cat.sound()  # Meow
my_cat.info()  # 이름: Whiskers, 나이: 2, 종: Cat
```

`super()`를 사용하여 부모 클래스의 메서드를 호출할 수 있습니다. 이를 통해 중복된 코드를 줄이고, 부모 클래스의 기능을 확장할 수 있습니다.

다형성은 같은 이름의 메서드가 다양한 방식으로 동작하도록 하는 기능입니다. 이는 객체의 타입에 따라 다른 동작을 수행할 수 있게 합니다.

예시:
```python
class Dog(Animal):
    def sound(self):
        print("Bark")

animals = [Cat("Kitty", 1), Dog("Rover")]
for animal in animals:
    animal.sound()
```
위 예시에서 `animals` 리스트에 `Cat`과 `Dog` 객체를 저장하고, 반복문을 통해 각 객체의 `sound()` 메서드를 호출하면 객체의 타입에 따라 다른 소리가 출력됩니다.

추가로, 다중 상속도 가능합니다. 다중 상속은 여러 부모 클래스로부터 속성과 메서드를 상속받는 것을 의미합니다. 파이썬에서는 클래스 정의 시 여러 부모 클래스를 콤마로 구분하여 지정할 수 있습니다.

예시:
```python
class Walker:
    def walk(self):
        print("걷고 있습니다.")

class Swimmer:
    def swim(self):
        print("수영하고 있습니다.")

class Amphibian(Walker, Swimmer):
    pass

frog = Amphibian()
frog.walk()  # 걷고 있습니다.
frog.swim()  # 수영하고 있습니다.
```

## 9. 예외 처리
### try, except, finally 구조
예외 처리는 오류가 발생했을 때 프로그램이 비정상적으로 종료되지 않도록 하는 방법입니다.

예시:
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("0으로 나눌 수 없습니다.")
finally:
    print("예외 처리 완료.")
```

### 사용자 정의 예외
사용자가 직접 예외를 정의하고 발생시킬 수 있습니다.

예시:
```python
class NegativeNumberError(Exception):
    pass

def check_positive(number):
    if number < 0:
        raise NegativeNumberError("음수는 허용되지 않습니다.")

try:
    check_positive(-5)
except NegativeNumberError as e:
    print(e)  # 음수는 허용되지 않습니다.
```

