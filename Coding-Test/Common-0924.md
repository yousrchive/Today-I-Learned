#문제 2

```
등차수열 혹은 등비수열 common이 매개변수로 주어질 때, 마지막 원소 다음으로 올 숫자를 return 하도록 solution 함수를 완성해보세요.
```

## 제한사항

```
2 < common의 길이 < 1,000
-1,000 < common의 원소 < 2,000
common의 원소는 모두 정수입니다.
등차수열 혹은 등비수열이 아닌 경우는 없습니다.
등비수열인 경우 공비는 0이 아닌 정수입니다.
```

## 고려해야 할 사항

등차수열/등비수열 그 수열의 관계는 내가 직접 정의해야 함.
common이라는 리스트 내에서의 관계를 인지하기, 그리고 그걸 다음 항에 적용하기

-> 등차수열인지, 등비수열인지의 확인이 선행되어야 한다.
-> 이 두 경우를 모두 포괄하도록 함수가 정의되어야 한다.
-> 등차수열, 등비수열의 수학적 의미는 무엇인가?

## 정답

```python

def solution(common): #common이라는 리스트를 인수로 받음
    if common[1] - common[0] == common[2] - common[1]:
        diff = common[1] - common[0]
        return common[-1] + diff #마지막 것에서 공차를 더한 걸 return

    else: #등비수열인 경우
        ratio = common[1] // common[0] #공비
        return common[-1] * ratio

```

## 배운 것

등비수열, 등차수열의 정의 사용과 함께 한 함수 내 if, else로 가정 사용

## 안 보고 다시 풀어보기

```python
def solution(common):
    if common[1] - common[0] == common[2] - common[1]:
        diff = common[1] - common[0]
        return common[-1] + diff #마지막 거에다 공차 더하기

    else:
        ratio = common[1] / common[0]
        return common[-1] * ratio

```

근데 /와 //의 차이가 무엇이지?

1. /(나눗셈 연산자): 부동소수점 나눗셈을 수행, 항상 소수점을 포함한 실수 형태로 반환

2. //(몫 연산자) : 소수점을 버리고 정수로 반환됩니다. 버림 연산을 거쳐 정수 값이 됩니다.

본 연산에서는 몫이 아닌 나눗셈 연산자가 더 적합. 
=>'common의 원소는 모두 정수입니다.'
'/'는 부동소수점 연산을 수행하지만 '//'는 단순 정수 연산이므로 연산 복잡성이 낮고 메모리 효율이 더 좋음(실수 타입X)


## C 언어 해석

```C
int solution(int common[], int length) {
    if (common[1] - common[0] == common[2] - common[1]) {
        int diff = common[1] - common[0];
        return common[length-1] + diff;
    } else {
        int ratio = common[1] / common[0]; //공비 확인
        return common[length-1] * ratio;
    }
}
```