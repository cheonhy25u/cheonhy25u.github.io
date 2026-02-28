---
title: Natas1
published: 2026-02-28
description: "개발자 도구 열기"
image: "../natas.png"
tags: ["Web", "Natas", "Writeup"]
category: Natas
draft: false
---
# Description
Username: natas1
URL:      http://natas1.natas.labs.overthewire.org

You can find the password for the next level on this page, but rightclicking has been blocked!

0에서와 같이 해당 페이지 내부에서 패스워드를 찾을 수는 있으나 페이지 소스 읽기를 위한 우클릭이 막혀 있다. 

# Solution
개발자 도구를 열면 소스를 확인할 수 있기 때문에 F12를 눌러 개발자 도구를 열고 html 파일을 확인하니 아래와 같이 주석으로 패스워드가 있는 것을 확인할 수 있었다.
![image](./Natas1.png)


