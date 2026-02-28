---
title: Bandit 0 
published: 2026-02-28
description: "ssh로 서버 접속하기"
image: "./bandit.png"
tags: ["Linux", "Bandit", "Writeup"]
category: Bandit
draft: false
---


# Level Goal 
이 레벨에서의 목표는 SSH를 이용해 게임에 로그인 하는 것이다. 연결해야 하는 호스트는 bandit.labs.overthewire.org이고 포트 번호는 2220이다. username과 password는 bandit0이다. 로그인한 후 Level1 page로 이동해 게임을 진행하면 된다. 

# Commands you may need to solve this level 
## ssh
- <a  href="https://manpages.ubuntu.com/manpages/noble/man1/ssh.1.html">우분투 매뉴얼 페이지</a>
- <a href="https://en.wikipedia.org/wiki/Secure_Shell">위키피디아 SSH</a>
- <a href="https://itsfoss.com/ssh-to-port/">기본 포트가 아닌 다른 포트로 SSH 연결하는 방법</a>
- <a href="https://www.wikihow.com/Use-SSH">기본적인 SSH 사용법과 ssh-keygen</a>

### ssh란? 
**Secure Shell Protocol**의 약자로 SSH Protocol은 네트워크 상의 다른 컴퓨터에 로그인하거나, 원격 시스템에서 명령을 실행하고 다른 시스템으로 파일을 복사할 수 있도록 해 주는 응용 프로그램 또는 그 프로토콜을 말한다. 
기존의 rsh, rlogin, 텔넷 등을 대체하기 위해 설계되었으며, 기본적으로는 **22번 포트**를 사용한다. 
command line으로는 아래와 같이 입력해 사용할 수 있다. 
```sh
ssh -p [포트 번호] [username]@[Destination IP]
```
# Solution
<img src="./bandit/bandit0.png"/>
문제에서 주어진 포트 번호, username, destination 주소를 이용해 `ssh -p 2220 bandit0@bandit.labs.overthewire.org` 로 로그인이 가능하다. 
