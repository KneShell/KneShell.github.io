---
title: "ModuleNotFoundError: No module named 'something'"
layout: post
categories: [python]
tags: [python]
---


![Screen Shot 2019-06-18 at 8 08 59 PM](https://user-images.githubusercontent.com/51946916/59677537-123d2680-9205-11e9-9fd1-80a8a3365fe1.png "good")

pytest를 이용하면 이런 오류가 출력된다.

python에서 pytest 모듈을 이용할 때, 환경변수가 제대로 설정이 되지 않아서 발생하는 것으로 보인다.
현재 python3.7 버젼에서 발생하는 문제로 보이는데, 후에 수정이 될지는 지캬봐야 할 것 같다.

해결 방법은 의외로 간단하다.
python -m pytest
명령어로 실행하는것.
python의 모듈 옵션을 이용해 파이테스트를 실행하면 환경변수를 제대로 잡아준다.

![Screen Shot 2019-06-18 at 9 06 14 PM](https://user-images.githubusercontent.com/51946916/59680708-f89fdd00-920c-11e9-8a06-e76823a723ce.png "No good")

워닝을 제외하면 정상적으로 실행되는 모습(?).

마지막으로 내가 도움을 받은 스택오버플로우의 주소를 남기며 마치겠다.

<https://stackoverflow.com/questions/20985157/py-test-no-module-named>  
<https://github.com/pytest-dev/pytest/issues/2287>
