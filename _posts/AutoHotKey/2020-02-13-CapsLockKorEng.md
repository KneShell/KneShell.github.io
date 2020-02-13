---
title: "CapsLock 한영전환"
layout: post
categories: [AutoHotKey]
tags: [AutoHotKey]
---

윈도우에서 Auto Hot Key를 이용해 CapsLock키에 한영전환을 맵핑하는 방법을 알아보겠다.  

1. 우선 <https://autohotkey.com/>에서 Auto Hot Key를 다운 받는다.
2. 메모장을 이용해 아래 스크립트를 붙여넣은 뒤, 시작 프로그램 폴더에 .ahk 확장자로 저장한다.

>일반적인 버전

```python
capslock::
KeyWait,capslock
if A_TimeSinceThisHotkey >= 1000 ; in milliseconds.
SetCapsLockState, % (State:=!State) ? "On" : "Off"
else
Send, {vk15sc1F2}
return
```

- 캡스락 키를 한번 눌렀을때는 한영전환으로 동작, 1초이상 길게 눌렀을때는 capslock으로 동작하는 스크립트
- 하지만 길게 눌렀을때 capslock 기능이 동작을 하지 않는 문제점이 있다.
  - 대안으로 shft + capslock을 이용하면 정상적으로 capslock기능이 동작한다.

> 더블탭 버전

```python
CapsLock::
KeyWait, CapsLock
KeyWait, CapsLock, D T0.2
If ErrorLevel
Send, {vk15}
Else
SetCapsLockState, % (State:=!State) ? "On" : "Off"
Return
```

- capslock을 한번 누르면 한영전환, 두번 연타하면 capslock으로 동작하는 스크립트. 이경우 의도한대로 작동한다. 다만 한영전환을 빠르게 연속적으로 사용할 경우 버벅이는 문제점이 있다.

>출처  
><https://iian.tistory.com/46>
><https://www.clien.net/service/board/lecture/13734816>
