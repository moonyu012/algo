# 문제 제목: 
Baekjoon 24510 시간복잡도를 배운 도도
## 문제 정보
- **출처:** 
- **난이도:** Easy, Medium, Hard 중 하나.

## 문제 설명
도도는 이번 신촌캠프에서 시간복잡도의 개념에 대해 배웠다. 하지만 듣다가 졸려서 자버린 결과 오개념을 가져 버렸는데, 바로 반복문의 개수로만 시간복잡도를 판단한다는 것이다. 

시간복잡도를 판단하기 위해 도도는 같은 줄에 몇 개의 반복문이 있는지 궁금해졌다. 도도가 반복문으로 생각하는 코드는 for, while 이다. 

도도를 위해 같은 줄에 있는 반복문의 최대 개수를 구하는 프로그램을 작성해보자.

## 해결 과정
함수에서 반복의 갯수를 더하고 리턴해줌
max는 계속 갱신하며 최대 값이 나옴
### 접근 방법

## 코드
```python
def find_loop(Line:str) ->int:
    cnt = line.count("for")
    cnt += line.count("while")
    return cnt
max = 0

n = int(input())
for i in range(n):
    line = input()
    cnt = find_loop(line)
    if max < cnt:
        max = cnt

print(max)
