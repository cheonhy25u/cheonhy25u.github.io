---
title: Bandit 1 -> 2
published: 2026-02-28
description: "디렉터리명에 특수문자가 있을 때"
image: "../bandit.png"
tags: ["Linux", "Bandit", "Writeup"]
category: Bandit
draft: false
---
https://overthewire.org/wargames/bandit/bandit2.html

# Level Goal
다음 단계를 위한 패스워드는 - 라는 이름의 파일에 있다. 

# Commands you may need to solve this level
이전 단계와 동일 

# Helpful Reading Material 
- <a href="https://www.google.com/search?q=dashed+filename">Google Search for “dashed filename”</a>
- <a href="https://linux.die.net/abs-guide/special-chars.html">Advanced Bash-scripting Guide - Chapter 3 - Special Characters</a>

# Solution
```
cat ./"-"
```
위와 같이 현재 경로를 나타내는 `./`와 따옴표를 사용하여 파일명을 넣어 주니 다음 단계 패스워드를 얻을 수 있었다. 
