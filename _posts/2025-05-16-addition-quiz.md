---
title: addition quiz
date: 2025-05-16
categories: [Dreamhack, misc]
tags: [wargame] [pwntools]
---

# Description

---

랜덤한 2개의 숫자를 더한 결과가 입력 값과 일치하는지 확인하는 과정을 50번 반복하는 프로그램입니다. 모두 일치하면 flag 파일에 있는 플래그를 출력합니다. 알맞은 값을 입력하여 플래그를 획득하세요.

# Solution

---

### 주어진 파일 분석

```sh
$ ./chall
7067+34=?
TIME OUT
```

주어진 바이너리 실행 시 두 수의 합을 짧은 시간 내에 입력받는다.

chall의 코드를 보면 문제가 50번 반복이 되는 걸 확인할 수 있으니 익스플로잇 코드에서도 참고하여 결과값을 보내야 한다.

### 익스플로잇 코드 작성

```python
from pwn import *

p = process('./chall')

for i in range(50):
    a = p.recvuntil(b'+')[:-1]
    b = p.recvuntil(b'=')[:-1]

    sum = int(a)+int(b)
    p.recvuntil(b'?\n')
    p.sendline(str(sum).encode())

p.interactive()
```

- +랑 등호까지 포함해서 받아오기 때문에 숫자만 받기 위해 [:-1]로 잘라 줌
- pwntools에서 바이트 단위로 받아오기 때문에 b''로 받아 오는 거 볼 수 있고 sum 값도 바이트 값으로 보내 주기 위해서 encode() 사용함
