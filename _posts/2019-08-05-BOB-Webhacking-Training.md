BOB Webhacking Training

BOB 멘토님이 만들어주신 web hacking training(이하 BOB WHT)에 대한 풀이를 진행해보도록 하겠습니다.

## Auth with JS 1(50)

![img1]({{site.url}}/img/190805/img1.png)

로그인 폼.



![img2]({{site.url}}/img/190805/img2.PNG)

스크립트 까면 그냥 나옵니다.

flag 획득 성공.

## Auth with JS 2(100)

![1]({{site.url}}/img/190806/1.PNG)

레벨 1과 같은 로그인폼

![2]({{site.url}}/img/190806/2.PNG)

스크립트를 까보면 다음과 같습니다.



![3]({{site.url}}/img/190806/3.PNG)

조합을 수작업으로해서 복잡하지만 저런 함수를 뜯어보면 됩니다.

SPLIT REVERSE 라고 나오는데 두번째 사진의 hfj4khjasfdj를 거꾸로 입력하면 되나 싶어서 입력했습니다.

정답 : FLAG{do_not_trust_obfuscated_javascript}