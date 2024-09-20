# 주어진 C 코드를 MIPS 어셈블리로 변환하기
: compiling IF statements


주어진 C 코드
```
if (i == j) {
    f = g + h;
} else {
    f = g - h;
}
```

레지스터 저장 가정: 
**i는 $s0, j는 $s1, f는 $s2, g는 $s3, h는 $s4에 저장**



MIPS 어셈블리 코드