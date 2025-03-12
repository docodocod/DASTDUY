### scanf와 scanf_s
예전의 c언어 공부를 떠올리면 입력함수는 출력은 printf , 입력은 scanf라고 머릿속에 기본적으로 박혀 있었다.
c언어 복습을 하기 위해 유튜브 인터넷 강의를 들으면서 복습하는 중에 강사가 scanf_s 함수를 사용하여 입력을 받고 있었다.
그래서 scanf와 scanf_s는 어떤 차이가 있는지 찾아 보았다.

### scanf와 scanf_의 차이점
>scanf =>C 표준 함수<BR>
>scanf_s => visual studio(MSVC) 전용 보안 강화 함수

또한 scanf와 달리 scanf_s는 visual studio 전용 함수이기 때문에 다른 c컴파일러(GCC, Clang)에서는 작동이 되지 않는다.


### 그럼 사용법은 뭐가 다를까?
>char name[50];<BR>
scanf("%s", name);<BR>
scanf_s("%s", name, (unsigned int)sizeof(name));

코드를 보면 scanf는 그냥 변수만 넣으면 되지만 scanf_s는 변수와 버퍼사이즈까지 같이 넣어줘야지 실행이 된다.

#### 결론: scanf_s()는 Microsoft에서만 쓰이는 보안 함수라, 범용성을 위해 scanf() + 크기 제한을 쓰는 게 더 좋다!

