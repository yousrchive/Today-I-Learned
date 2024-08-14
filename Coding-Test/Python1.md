# Python Coding Test Datatype and Complexity
[course source](https://www.youtube.com/watch?v=m-9pAwq1o3w&list=PLRx0vPvlEmdAghTr5mXQxGpHjWqSz0dgC)

Online Judge

Abroad : Codeforces, TopCoder, LeetCode, CodeCHEF
Domestic: BOJ, CodeUp, Programmers, SW Expert Academy

Complexity
-Time-Complexity: Value time for each algorithms to perform
-Sparse-Complexity: Memory usage for each algorithms to perform

# Big-O Notation : 가장 빠르게 증가하는 항만을 고려하는 표기법
차수가 가장 큰 항만을 남김

# 

좋음
상수 시간 - 로그 시간 - 선형 시간 - 로그 선형 시간 - 이차 시간 - 삼차 시간 - 지수 시간
나쁨
소스코드가 내부적으로 다른 함수를 호출한다면 다른 함수의 시간복잡도까지 고려해야 함
코딩테스트 문제에서 시간 제한은 통상 1~5초 가량이며, Python은 연산 횟수가 5억을 넘어가면 15초까지 걸리기도 함.

문제에서 가장 먼저 확인해야하는 내용은 시간제한(수행시간 요구사항)임

1. 지문 읽기 및 컴퓨터적 사고
2. 요구사항(복잡도) 분석
3. 문제 해결을 위한 아이디어 찾기
4. 소스코드 설계 및 코딩

핵심 아이디어 캐치 후, 소스 코드 작성

``` python
import time
start_time = time.time() # 측정 시작

end_time = time.time()
print("time-consumed:", end_time - start_time) #수행시간 출력
```

# 파이썬의 자료형 dtype
파이썬의 자료형은 정수형, 실수형, 복소수형, 문자열, 리스트, 튜플, 사전 등이 있음.

파이썬은 변수에 소수점을 붙인 수를 대입하면 실수형 변수로 자동 변환됩니다.

지수표현방식 유효숫자e&지수 = 유효숫자 x 10의 지수승

1e9 = 10^9
지수 표현 방식은 임의의 큰 수를 표현하기 위해 자주 사용
최단 경로 알고리즘에서는 도달할 수 없는 노드에 대해 최단 거리를 INF로 설정
가능한 최대값이 10억 미만이면 1e9 사용 가능

IEEE754 표준에서는 실수형을 저장하기 위해 4, 8바이트의 고정된 크기의 메모리를 할당하므로 컴퓨터 시스템은 실수 정보 표현에 한계를 가짐
=> ROUND() 함수의 사용이 권장됨.

![img](../Coding-Test/img/스크린샷%202024-08-14%20오후%205.38.43.png)

Before heading to next cell, should take it to round func and make it to the shape that we desire.

# 수 자료형의 연산

사칙연산과 나누기 연산자
- /는 나눠진 결과를 실수형으로 반환
- 다양한 로직 설계 시 나머지 연산자인 %를 활용할 것을 권장
- 몫 연산자 //
- 거듭제곱 연산자 **

## 리스트 자료형

데이터를 연속적으로 담아 처리하기 위해 사용하는 자료형
배열, 테이블이라고 부르기도 함.

