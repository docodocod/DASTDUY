# OAUTH란?
인터넷 사용자들이 비밀번호를 제공하지 않고 다른 웹사이트 상의 자신들의 정보에 대해 웹사이트나 애플리케이션의 접근 권한을 부여할 수 있는 공통적이 수단으로서 사용되는 접근 위임을 위한 개방형 표준이다.
어느 회원가입 페이지를 들어가보면 Google,Facebook,kakao 등 외부 소셜 계정을 기반으로 간편하게 회원가입 및 로그인을 할 수 있게 되어 있다.
이 프로토콜을 이용하여 연동되는 외부 웹 어플리케이션에서 제공하는 기능을 간편하게 사용할 수 있다는 장점이 있다.
---
## OAUTH 구성요소
>Resource Owner : 웹 서비스를 이용하려는 유저, 자원(개인정보)을 소유하는자<br>
> 
> Client : 자사 또는 개인이 만든 애플리케이션 서버<br>
> 클라이언트라는 이름은 client가 Resource server에게 필요한 자원을 요청하고 응답하는 관계<br>
> 
> Authorization Server : 권한을 부여해주는 서버다.<br>
> 사용자는 이 서버로 ID,PW를 넘겨 Authorization Code를 발급 받을 수 있다.<br>
> Client는 이 서버로 Authorization Code를 넘겨 Token을 발급 받을 수 있다.
> 
> Resource Server : 사용자의 개인정보를 가지고 있는 애플리케이션 회사 서버<br>
> Client는 Token을 이 서버로 넘겨 개인정보를 응답 받을 수 있다.<br>
> 
> Access Token : 자원에 대한 접근 권한을 Resource Owner가 인가하였음을 나타내는 자격증명<br>
> 
> Refresh Token : access token은 보안상 만료기간이 짧기 때문에 얼마 지나지 않아 만료되면 사용자는 로그인을 다시 시도해야 한다.<br>
> 그러나 refresh token이 있다면 access token이 만료될 때 refresh token을 통해 access token을 재발급 받아 재 로그인 할 필요없게끔 한다.<br>
> 

client는 Resource Owner을 대신해 로그인을 하고 이때 필요한 정보를 Resource Server에서 얻어 서로 비교한 후 유~~효성을 판단한다~~
               
