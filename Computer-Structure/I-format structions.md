# I-format 

MIPS 어셈블리 안에서 I-format(Immediate Format)은 명령어의 형식 중 하나입니다.

### I Format의 구조
op(6 bits): 명령어의 연산 코드 (Operation Code)
rs(5 bits): 첫 번째 소스 레지스터의 주소(register source)
rt(5 bits): 두 번째 소스 레지스터 혹은 목적지 레지스터의 주소(register terminal)
immediate/address (16 bits): 즉시 값(상수) 또는 주소

### I format의 용도

I format 명령어는 주로 다음과 같은 작업에 사용됩니다:

1) 즉시 값 사용: 연산에 사용할 상수를 포함합니다.

예: `addi, andi, ori` 등.

2) 분기 명령어: **프로그램 흐름을 제어하는 명령어**에서 사용됩니다.

예: `beq, bne` 등.

3) **메모리 접근**: 특정 주소에 대한 로드 또는 저장 명령어에서 사용됩니다.

예: lw, sw와 같은 명령어.


+ 예시
다음은 I format 명령어의 예시입니다:

-addi: 즉시 값을 더하는 명령어

```addi $t0, $t1, 5```

이 명령어는 $t1의 값에 5를 더하여 결과를 $t0에 저장합니다.

-lw: 메모리에서 단어를 로드하는 명령어

```lw $t0, 0($t1)```

이 명령어는 $t1 레지스터가 가리키는 주소에서 값을 로드하여 $t0에 저장합니다.

(lw 저장하는 곳, 로드하는 곳)
