#문제 5

```
PROGRAMMERS-962 행성에 불시착한 우주비행사 머쓱이는 외계행성의 언어를 공부하려고 합니다. 알파벳이 담긴 배열 spell과 외계어 사전 dic이 매개변수로 주어집니다. spell에 담긴 알파벳을 한번씩만 모두 사용한 단어가 dic에 존재한다면 1, 존재하지 않는다면 2를 return하도록 solution 함수를 완성해주세요.
```

## 제한사항

```
spell과 dic의 원소는 알파벳 소문자로만 이루어져있습니다.
2 ≤ spell의 크기 ≤ 10
spell의 원소의 길이는 1입니다.
1 ≤ dic의 크기 ≤ 10
1 ≤ dic의 원소의 길이 ≤ 10
spell의 원소를 모두 사용해 단어를 만들어야 합니다.
spell의 원소를 모두 사용해 만들 수 있는 단어는 dic에 두 개 이상 존재하지 않습니다.
dic과 spell 모두 중복된 원소를 갖지 않습니다.
```

## 고려해야 할 사항

spell에 담긴 알파벳을 *한번씩만 모두 사용한 단어*가 dic에 존재한다면 1, 존재하지 않는다면 2를 return하도록 solution 함수를 완성해주세요.

모두를 사용한 조합이 존재하는지만 확인하면 됨
=> dic은 spell의 단일 원소를 사용할 수 없음.
=> dic에 있는 단어로 만들 수 있는 모든 순열을 만들어 가능한 단어가 있는지 확인하기

존재하면 1, 존재하지 않으면 2 반환

## 정답

```python

from itertools import permutations 
#permutations는 주어진 리스트, 문자열 등 iterable들의 모든 가능한 순열을 생성하는 데에 사용된다.

def solution(spell, dic):
    possible_words = [''.join(p) for p in permutations(spell)]

    for word in possible_words:
        if word in dic:
            return 1

    return 2

```

## 알게 된 점

itertools 라이브러리의 permutations가 순열 생성에 사용
리스트 안에 join을 넣어 모든 조합들을 합치도록
리스트 안에 ''로 구분된 요소들을 합치는 데에 join이 사용되며 구분자는 '' 공백으로 한다.