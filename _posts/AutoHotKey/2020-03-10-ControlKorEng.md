---
title: "HappyHaking Keyboard Control 한영전환"
layout: post
categories: [AutoHotKey]
tags: [AutoHotKey]
---

해피해킹 키보드의 경우 캡스락이 "펑션 + Tab"키로 숨어버리고, 기존 위치에 Control키가 대신 자리를 차지하고 있다. 따라서 캡스락을 한영전환으로 사용하기에는 애매한 상황이다.  

이를 타개하기 위해 선택한 방법은 다음과 같다.  

1. 컨트롤 키를 한영전환으로 맵핑한다.
2. 왼쪽 윈도우키(메타키)를 컨트롤키로 맵핑한다.

이렇게하면 맥 OS와 비슷한 환경에서 해피해킹을 사용 할 수 있다.  
실행창에서 shell:startup를 입력후 나오는 시작 프로그램 폴더에 다음 두 파일을 저장하자.

>HHKBControlToCapsLock.ahk

```Python
Control::
KeyWait,capslock
if A_TimeSinceThisHotkey >= 1000 ; in milliseconds.
SetCapsLockState, % (State:=!State) ? "On" : "Off"
else
Send, {vk15sc1F2}
return
```

>LWinToControl.ahk

```python
LWin::Control
```

하나의 파일로 정리하는 방법은 모르기 때문에 2개로 나눠서 저장했다.
