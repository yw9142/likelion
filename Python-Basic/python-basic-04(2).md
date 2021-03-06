# [Python] BASIC 4. 제어문(2)

## 반복문

 이번 시간에는 제어문의 종류인 **반복문**에 대해 배워 보겠습니다. 
 
 이름을 보니 무언가를 반복할 것만 같습니다. 반복문은 **컴퓨터에게 우리가 원하는 작업을 반복하게끔 지시하는 방법**입니다. 
 
 예를 들어 학생 100명의 성적을 출력해야 한다고 생각해봅시다.

```python
print(영희의 성적은 96점입니다.)

print(영준이의 성적은 80점입니다.)

print(성준이의 성적은 100점입니다.)

print(물결이의 성적은 99점입니다.)
..............
```

이렇게 100명을 출력해야 할 때 위처럼 print로 100줄을 적는 건 너무나도 고된 일입니다. 

반복문은 이런 반복적인 일들을 컴퓨터에게 맡길 수 있게 해줍니다. 

파이썬의 반복문에는 **for문**과 **while문**이 있습니다.

---

### for문

for문의 문법적인 틀을 알아보겠습니다.

```python
for 반복제어변수 in 반복대상 :
	반복실행 할 내용
```

 여기서 **반복대상**이란 반복되길 바라는 대상입니다. 
 
 즉, `어떤 걸 반복할 거야?` 라고 물었을 때 대상이 되는 것을 의미합니다. 
 
 예를 들어봅시다.
 
 우리 반 학생 성적의 평균을 구하고 싶을 때 **우리 반 학생들의 성적**을 반복해서 더해준 뒤 학생 수만큼 나눠줘야 합니다. 
 
 이때 반복해야 하는 것은 **우리 반 학생들의 성적 리스트**입니다. 이렇게 리스트, 튜플, 문자열 등 길이가 있는 자료형이 반복 대상이 됩니다.

 반복대상이 뭔지 알았습니다! 그럼 이제 그 반복대상을 하나하나 순회하며 직접 반복을 해 줄 변수가 필요합니다. 
 
 반복대상의 첫 번째 대상이 되어 실행하고, 두 번째 대상이 되어 실행하고... 
 
 이렇게 내용을 하나하나 반복하며 실행해 주는 변수를 **반복제어변수**라고 합니다.

```python
for score in [96,98,100,87]:
	print(score)

-----------------결과-----------------
96
98
100
87
```

위 프로그램에서 반복대상은 `[96,98,100,87]`라는 리스트이고, 

반복제어변수는 `score` 이 됩니다.

### for문에서 유용한 range함수

```python
sum = 0
for i in range(5):
	sum += i
```

> range(x,y) : x이상 y미만의 수 리스트를 반환합니다.   
> range(x) : 0부터 x미만의 수 리스트를 반환합니다.

---

### while문

 for문이 `이 반복 대상을 반복하세요` 였다면 
 
 while문은 `이 조건을 만족하는 동안 반복하세요` 라는 의미가 됩니다. 
 
 if문을 사용할 때 '이 조건에서 이런 코드를 실행하세요' 하고 알려줬던 거 기억나시나요? 
 
 while문은 이 조건에서 이런 코드를 반복실행하라고 알려줍니다.

```python
num = 10
while(num > 0):
	print("반복문 수행 중!")
	num-=1

-----------------결과-----------------
10
9
8
7
6
5
4
3
2
1
```

 그럼 해당 조건을 충족함에도 불구하고 반복문을 탈출하고 싶을 때는 어떻게 하면 좋을까요? 
 
 `break` 는 반복문의 조건을 만족하더라도 무조건 루프를 탈출시킵니다. 
 
 break문은 무한루프와 함께 자주 쓰입니다. 
 
 무한루프란 끝나지 않는 반복문을 의미합니다. 즉 조건이 영원히 참일 때를 의미하죠.

```python
num = 0

while(True):
	num += 1
	if(num>10):
		break

-----------------결과-----------------
11
```

조건이 `true` 이니 무한루프를 돌고, num 변수가 10이 될 때 루프를 탈출하는 프로그램입니다.

> **for**문의 경우 **반복 횟수가 정확하게 정해진 경우**에 주로 사용합니다.   
> 반면에 **while**문의 경우 **특정 조건이 종료될 때 까지 반복하고 싶을 때** 많이 사용합니다. 


- 주사위를 10번 던져 합을 구하는 프로그램  ⇒ for문을 사용합니다.
- 주사위를 굴려 나온 수의 합이 50이 될 때까지 반복하는 프로그램 ⇒ while문을 사용합니다.

이처럼 본인의 상황과 목적에 따라 사용할 수 있습니다. 

for문과 while문을 이용해 다양한 프로그램을 직접 만들어보세요! 

직접 쓰면서 다른 점을 찾는 과정이 도움이 됩니다.
