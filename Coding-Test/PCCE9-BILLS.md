# PCCE 기출문제 9번 / 지폐접기

```
문제 설명
민수는 다양한 지폐를 수집하는 취미를 가지고 있습니다. 지폐마다 크기가 달라 지갑에 넣으려면 여러 번 접어서 넣어야 합니다. 예를 들어 지갑의 크기가 30 * 15이고 지폐의 크기가 26 * 17이라면 한번 반으로 접어 13 * 17 크기로 만든 뒤 90도 돌려서 지갑에 넣을 수 있습니다. 지폐를 접을 때는 다음과 같은 규칙을 지킵니다.

지폐를 접을 때는 항상 길이가 긴 쪽을 반으로 접습니다.
접기 전 길이가 홀수였다면 접은 후 소수점 이하는 버립니다.
접힌 지폐를 그대로 또는 90도 돌려서 지갑에 넣을 수 있다면 그만 접습니다.
지갑의 가로, 세로 크기를 담은 정수 리스트 wallet과 지폐의 가로, 세로 크기를 담은 정수 리스트 bill가 주어질 때, 지갑에 넣기 위해서 지폐를 최소 몇 번 접어야 하는지 return하도록 solution함수를 완성해 주세요.

지폐를 지갑에 넣기 위해 접어야 하는 최소 횟수를 구하는 과정은 다음과 같습니다.

1. 지폐를 접은 횟수를 저장할 정수 변수 answer를 만들고 0을 저장합니다.
2. 반복문을 이용해 bill의 작은 값이 wallet의 작은 값 보다 크거나 bill의 큰 값이 wallet의 큰 값 보다 큰 동안 아래 과정을 반복합니다.
    2-1. bill[0]이 bill[1]보다 크다면
        bill[0]을 2로 나누고 나머지는 버립니다.
    2-2. 그렇지 않다면
        bill[1]을 2로 나누고 나머지는 버립니다.
    2-3. answer을 1 증가시킵니다.
3. answer을 return합니다.
```

## 제한사항

```
wallet의 길이 = bill의 길이 = 2
10 ≤ wallet[0], wallet[1] ≤ 100
10 ≤ bill[0], bill[1] ≤ 2,000
```

wallet[0], wallet[1]을 각각 a, b에
bill[0], bill[1]을 c, d에 담는 것 자체가 좋음

## 고려해야 할 사항

while 반복문을 사용해서 wallet의 가로/세로가 지폐의 가로/세로보다 모두 큰 경우가 될 때까지 반복하여 count를 세어야 한다.

그리고 90도 돌렸을 경우, 즉 가로/세로가 바뀌었을 경우에도 괜찮으므로 while문을 탈출하는 과정에 가로/세로가 바뀐 경우도 함께 포함하도록 한다.

## 정답

```python

def solution(wallet, bill):
    a, b = bill  # 지폐 크기 (가로, 세로)
    c, d = wallet  # 지갑 크기 (가로, 세로)

    answer = 0  # 초기 접기 횟수

    while True:
        # 지폐가 지갑에 들어갈 수 있는지 확인
        if (a <= c and b <= d) or (a <= d and b <= c):
            break  # 접을 필요 없음

        # 더 긴 쪽을 반으로 접기
        if a > b:
            a //= 2  # 가로를 반으로 접음
        else:
            b //= 2  # 세로를 반으로 접음

        answer += 1  # 접기 횟수 증가

    return answer
```

## 안 보고 다시 풀기

```python

def solution(wallet, bill):
    a, b = bill
    c, d = wallet

    answer = 0 #일단 0

    while True: #계속 반복한다 어떤 경우에?
        if (a <= c and b <= d) or ( a <= d and b <= c):
            break #접을 필요 없이, 반복문을 그대로 answer=0을 유지한 채로 빠져나온다.

        if a > b :
            a // =2

        else: b//=2

        answer += 1

    return answer

```