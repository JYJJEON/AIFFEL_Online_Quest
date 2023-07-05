# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 전재영
- 리뷰어 : 임현석


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [o] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  
- [o] 주석을 보고 작성자의 코드가 이해되었나요?
  > 네, 각 줄 마다 주석이 달려있어서 이해하기 수월했습니다.
- [o] 코드가 에러를 유발할 가능성이 없나요?
  > 네, 입력값이 변해도 제대로 출력될 것 같습니다.
- [o] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 네, 각 코드의 기능들을 잘 설명해주셨습니다.
- [o] 코드가 간결한가요?
  > 알아보기 쉽게 작성되었습니다.

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
```python
import time as t
# 입력값을 입력하는 경우
'''
fish_list = []

while True:
    name = input("이름을 입력하세요 (or 'q' to quit): ")
    if name == 'q':
      break
    speed = int(input("speed를 입력하세요: "))
    fish = {"이름": name, "speed": speed}
    fish_list.append(fish)
'''
# 입력값을 처음부터 주는 경우
fish_list = [
{"이름": "Nemo", "speed": 3},
{"이름": "Dory", "speed": 5},
]
# comprehension을 사용하여 출력값을 입력
def show_fish_movement_comprehension(fish_list):
  # fish list에 있는  키, 밸류 값을 튜플 형식으로 저장
    출력값 = [(fish['이름'],fish['speed']) for fish in fish_list]
    # 출력값에서 name speed 의 변수로 for 반복문
    for name,speed in 출력값:
      # 각 반복되는 변수들을 밑에 형식으로 출력
      print(name,'is swimming at',speed, 'm/s')
      # 프린트를 한 후 2초를 정지
      t.sleep(2)

# generator를 통해 사용값을 출력
def show_fish_movement_Generator(fish_list):
  # newlist로 입력 변수값 저장
    newlist = fish_list
    # yield값을 얻어낼 generator 함수
    def generator(newlist):
        for fish in newlist:
            yield f'''{fish['이름']} is swimming at {fish['speed']} m/s'''
    # generator 진행상황을 위해 generator 값을 a로 지정
    a = generator(newlist)
    # generator가 진행 되는 동한 값을 출력
    for i in generator(newlist):
        print(next(a))
        t.sleep(2)

print("Using Comprehension:")
show_fish_movement_comprehension(fish_list)
print("Using Generator:")
show_fish_movement_Generator(fish_list)
#함수 안에 모든 실행문을 집어넣어서 출력명령문이 깔끔하게 쓰였습니다. 
```
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
```python
# comprehension을 사용하여 출력값을 입력
def show_fish_movement_comprehension(fish_list):
  
    출력값 = [(fish['이름'],fish['speed']) for fish in fish_list]
   
    for name,speed in 출력값:
     
      print(f"{name} is swimming at {speed} m/s")
      #f string으로 문자열을 포매팅 하는 방식도 있습니다.

      t.sleep(2)

# generator를 통해 사용값을 출력
def show_fish_movement_Generator(fish_list):
  
    newlist = fish_list
    
    def generator(newlist):
        for fish in newlist:
            yield f'''{fish['이름']} is swimming at {fish['speed']} m/s'''
   
    a = generator(newlist)
   
    for i in generator(newlist):
        print(next(a))
        t.sleep(2)

print("Using Comprehension:")
show_fish_movement_comprehension(fish_list)
print("Using Generator:")
show_fish_movement_Generator(fish_list)

```


