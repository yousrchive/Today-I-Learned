#문제 1

```
머쓱이는 태어난 지 6개월 된 조카를 돌보고 있습니다. 조카는 아직 "aya", "ye", "woo", "ma" 네 가지 발음을 최대 한 번씩 사용해 조합한(이어 붙인) 발음밖에 하지 못합니다. 문자열 배열 babbling이 매개변수로 주어질 때, 머쓱이의 조카가 발음할 수 있는 단어의 개수를 return하도록 solution 함수를 완성해주세요.
```

## 제한사항

```
1 ≤ babbling의 길이 ≤ 100
1 ≤ babbling[i]의 길이 ≤ 15
babbling의 각 문자열에서 "aya", "ye", "woo", "ma"는 각각 최대 한 번씩만 등장합니다.
즉, 각 문자열의 가능한 모든 부분 문자열 중에서 "aya", "ye", "woo", "ma"가 한 번씩만 등장합니다.
문자열은 알파벳 소문자로만 이루어져 있습니다
```

## 고려해야 할 사항

한 단어에서 인지하는 단어와 그렇지 않은 단어가 함께 나오는 경우, 해당 단어는 할 수 없는 발음으로 생각한다.

## 정답

```python

import re

def solution(babbling):
    count = 0
    patterns = ['aya', 'ye', 'woo', 'ma']

    regex_pattern = re.compile("^(aya|ye|woo|ma)+$")
    #정규 표현식을 컴파일하여 정규식 객체를 생성하는 함수
    #문자열에서 패턴을 찾거나 매칭할 때 사용
    #'+'는 패턴이 1번 이상 반복될 수 있음을 의미
    #'$' 문자열의 끝
    #'^'시작
    #aya, ye, woo, ma 문자열이 하나 이상 반복, 문자열의 처음부터 끝까지 일치하는지 확인

    for word in babbling: #solution의 객체로 들어오는 babbling의 하나하나씩 word에 대해
        if regex_pattern.match(word):
            count += 1

    return count #모든 word에 대해 수행 후 count
    #이때 해당 word를 구성하고 있는 요소들이 아니라, 각각 하나씩이 아니라 regex_pattern 하나씩을 수행.

```

## 배운 것

우리가 보고자 하는 단어집을 생성하고, 그것으로 모든 패턴을 만든 후
그 패턴에 해당한다면 +=1을 한다는 발상

## 안 보고 다시 풀어보기

```python
def solution(babbling):
    count = 0 #count 객체 초기화
    pattern = ['aya', 'ye', 'ma', 'woo']

    regex_pattern = re.compile("^(aya|ye|ma|woo)+$")#따옴표 붙여줘야 함!

    for word in babbling:
        if regex_pattern.match(word): #match 함수 사용
            count += 1 #babbling은 list임

    return count
```

따옴표 붙이기, return count 탭 확인!

## C 언어로 바꾸기

```C
#include <stdio.h>
#include <string.h>

// 문자열이 패턴에 맞는지 확인하는 함수
int is_valid_babbling(const char* word) {
    // 가능한 패턴 목록
    const char* pattern[] = {"aya", "ye", "ma", "woo"};
    int pattern_count = 4;  // 패턴 개수
    int word_len = strlen(word);  // 입력 단어 길이
    int i = 0;

    while (i < word_len) {
        int matched = 0;
        // 각 패턴과 비교
        for (int j = 0; j < pattern_count; j++) {
            int pattern_len = strlen(pattern[j]);
            // 입력 문자열이 현재 패턴으로 시작하는지 확인
            if (strncmp(&word[i], pattern[j], pattern_len) == 0) {
                matched = 1;
                i += pattern_len;  // 패턴에 맞으면 인덱스를 이동
                break;
            }
        }
        // 패턴이 일치하지 않으면 유효하지 않은 문자열
        if (!matched) {
            return 0;
        }
    }

    return 1;  // 패턴에 모두 맞으면 유효한 문자열
}

int solution(const char* babbling[], int babbling_count) {
    int count = 0;

    for (int i = 0; i < babbling_count; i++) {
        if (is_valid_babbling(babbling[i])) {
            count++;
        }
    }

    return count;
}
```