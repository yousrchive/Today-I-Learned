#문제 4

```
연속된 세 개의 정수를 더해 12가 되는 경우는 3, 4, 5입니다. 두 정수 num과 total이 주어집니다. 연속된 수 num개를 더한 값이 total이 될 때, 정수 배열을 오름차순으로 담아 return하도록 solution함수를 완성해보세요.
```

## 제한사항

```
1 ≤ num ≤ 100
0 ≤ total ≤ 1000
num개의 연속된 수를 더하여 total이 될 수 없는 테스트 케이스는 없습니다.
```

## 고려해야 할 사항

num개의 정수를 더해 total을 만들 것이다.
해당 정수들은 이어져 있는 숫자임
a b c d ... x
합을 달리 생각하면 가장 첫 숫자와 열의 마지막 숫자를 더해 2로 나누고, 쌍의 개수인 n개만큼 곱하면 a * (a + n-1) * n / 2 = total로 만드는 a를 가장 첫째항으로 삼아 n만큼 더해가면 됨.

## 정답

```python

def solution(num, total):
    a = (total - (num * (num -1)) // 2) // num
    return [a + i for i in range(num)]

```

## C 언어로 풀면

```C
int* solution(int num, int total) {
    int a = (total - (num * (num -1)) / 2) / num;

    int* result = (int*)malloc(num * sizeof(int));
    if (result == NULL) {
        return NULL;
    }

    for (int i = 0; i < num; i++) {
        result[i] = a + i;
    }

    return result;
}
```