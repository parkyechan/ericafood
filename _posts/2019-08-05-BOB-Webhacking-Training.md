

BOB Webhacking Training

BOB 멘토님이 만들어주신 web hacking training(이하 BOB WHT)에 대한 풀이를 진행해보도록 하겠습니다.

## Auth with JS 1(50)

---

![img1]({{site.url}}/img/190805/img1.png)

로그인 폼.



![img2]({{site.url}}/img/190805/img2.PNG)

스크립트 까면 그냥 나옵니다.

flag 획득 성공.

## Auth with JS 2(100)

---

![1]({{site.url}}/img/190806/1.PNG)

레벨 1과 같은 로그인폼

![2]({{site.url}}/img/190806/2.PNG)

스크립트를 까보면 다음과 같습니다.



![3]({{site.url}}/img/190806/3.PNG)

조합을 수작업으로해서 복잡하지만 저런 함수를 뜯어보면 됩니다.

SPLIT REVERSE 라고 나오는데 두번째 사진의 hfj4khjasfdj를 거꾸로 입력하면 되나 싶어서 입력했습니다.

정답 : FLAG{do_not_trust_obfuscated_javascript}

## File Upload 1(100)

---

## File Upload 1(100)

---

![1]({{site.url}}/img/rubiya/dlist/1.PNG)

그냥 이미지만 덩그러니 있어서 뭘해야할지 몰라서 개발자모드부터 켰습니다.

![2]({{site.url}}/img/rubiya/dlist/2.PNG)

dirlist 아래에 static이라는 폴더가 있더라구요.

![3]({{site.url}}/img/rubiya/dlist/3.PNG)

들어갔더니 파일 목록들이 보임.

![4](C:\Users\park\Desktop\git\parkyechan.github.io\img\rubiya\dlist\4.PNG)

flag가 저기 보이는군요. 성공.



## Parameter Manipulation

---



![1]({{site.url}}/img/rubiya/para/1.PNG)

다음과 같은 로그인 폼이 보입니다. 원래 저기 id와 이름이는 제 id와 이름이 있었으나 지웠습니다.

![2]({{site.url}}/img/rubiya/para/2.PNG)

보니까 주소에 이렇게 파라미터가 있더라고요. 제가 가입한 순서 같습니다.



![3]({{site.url}}/img/rubiya/para/3.PNG)

그래서 1번으로 바꿔보니, 관리자분의 id와 이름이 나옵니다.



![4]({{site.url}}/img/rubiya/para/4.PNG)

변조해서 제출을 누르니 flag가 나옵니다. 성공

## XML Injection

---



![1]({{site.url}}/img/rubiya/xml/1.PNG)

로그인 폼이 나옵니다. xml 파일을 보라니까 확인해봐야겠습니다.

![2]({{site.url}}/img/rubiya/xml/2.PNG)

기존의 xml 코드입니다.

![3]({{site.url}}/img/rubiya/xml/3.PNG)

임의로 아이디를 만들고 로그인을 시도했습니다. usertype이 admin이 아니라고 하는 군요.

![4]({{site.url}}/img/rubiya/xml/4.PNG)

위와 같은 소스 중에서 username 부분에 <!--로 주석으로 처리하기 시작하면서 email까지 주석으로 처리하고 나머지 tag들을 이메일 부분에 넣어줍니다. 이때 Usertype을 제가 admin으로 넣어줍니다.

![5]({{site.url}}/img/rubiya/xml/5.PNG)

넣고 난 다음에 xml 소스를 확인해보면 다음과 같습니다.

![6]({{site.url}}/img/rubiya/xml/6.PNG)

확인해보면 usertype으로 로그인을 한뒤에 다음과 같이 flag가 나옴을 알 수 있습니다.