---
title: "fatal-destination path '.' already exists and is not an empty directory"
layout: post
categories: [git]
tags: [git]
---

![Screen Shot 2019-07-08 at 2 12 12 PM](https://user-images.githubusercontent.com/51946916/60786104-3353c000-a190-11e9-9448-d4d916d4fee3.png "yas")

git clone을 만들때 발생하는 오류.
현재 디렉토리를 clone으로 지정하기 위해서는 해당 디렉토리에 반드시 폴더나 파일이 없는 상태여야한다.
즉, 저러한 오류가 발생한다면 폴더안에 파일이 존재한다는 뜻.

그러나 MAC의 경우에는 눈 씻고 찾아봐도 당췌 무슨 파일이 있다는건지 알 수 없을 때가 있다.
범인은 바로 ".DS_Store"라는 파일이다.
파인더에서 폴더를 탐색할 경우 생기는 파일로, 사용자 단에서는 알 수 없도록 은폐된 파일인 듯하다.
여튼 이 파일 덕분에 깃에서 클론을 만들때 충돌이 일어난다.

해결 방법은 간단하다.

1. 터미널을 열고 해당 디렉토리로 이동
2. "rm .DS_Store" 입력

참고 링크.
<https://stackoverflow.com/questions/6224626/clone-contents-of-a-github-repository-without-the-folder-itself>  
<https://nine-hundred.github.io/Blog/DS_store가-생기는-이유와-삭제하는-방법/>