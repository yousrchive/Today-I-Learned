# Compiling-While-Loop


정답

```js
loop:
    sll $t0, $s3, 2             # $t0 = i * 4 (인덱스를 바이트 단위로 변환)
    add $t0, $t0, $s6           # $t0 = save[i]의 주소 ($s6 + $t0)
    lw $t1, 0($t0)              # $t1 = save[i] (save 배열에서 값 로드)

    beq $t1, $s5, increment      # save[i]가 k와 같으면 increment로 분기

exit_loop:
    # 반복문 종료 후 코드 계속
    j end

increment:
    addi $s3, $s3, 1             # i += 1
    j loop                       # 반복문 시작으로 점프

end:
    # 프로그램의 나머지 부분 계속
```