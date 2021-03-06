# wsgi 와 web server 전체적인 흐름
Django 웹 어플리케이션을 서버에 배포할때 기본적인 구조는 다음과 같다.

**사용자 <-> 웹서버 <-> WSGI <-> Django**

### WSGI
>웹 서버 게이트웨이 인터페이스(WSGI, Web Server Gateway Interface)는 웹서버와 웹 애플리케이션의 인터페이스를 위한 파이선 프레임워크다.  
>- 출처: [위키피디아](https://ko.wikipedia.org/wiki/%EC%9B%B9_%EC%84%9C%EB%B2%84_%EA%B2%8C%EC%9D%B4%ED%8A%B8%EC%9B%A8%EC%9D%B4_%EC%9D%B8%ED%84%B0%ED%8E%98%EC%9D%B4%EC%8A%A4)  
  
WSGI는 웹서버와 Django를 연결해주는 역할을 하는 python 프레임 워크다. 웹서버가 직접적으로 python으로 된 Django와 통신할 수 없기 때문에 둘을 연결해주는 역할이 필요한데 wsgi가 그 역할을 한다.  

WSGI에는 여러가지 종류가 있는데 그 중 기능이 가장 뛰어나고 확장성이 좋은 uWSGI를 보통 사용한다.

### 웹서버
>웹 서버(Web Server)는 HTTP를 통해 웹 브라우저에서 요청하는 HTML 문서나 오브젝트(이미지 파일 등)을 전송해주는 서비스 프로그램을 말한다.  
>웹 서버의 주된 기능은 웹 페이지를 클라이언트로 전달하는 것이다. 주로 그림, CSS, 자바스크립트를 포함한 HTML 문서가 클라이언트로 전달된다.  
>주된 기능은 콘텐츠를 제공하는 것이지만 클라이언트로부터 콘텐츠를 전달 받는 것도 웹 서버의 기능에 속한다. 이러한 기능은 파일 업로드를 포함하여 클라이언트에서 제출한 웹 폼을 수신하기 위해 사용된다.  
>- 출처: [위키피디아](https://ko.wikipedia.org/wiki/%EC%9B%B9_%EC%84%9C%EB%B2%84)

uWSGI처럼 Nginx도 웹서버 소프트웨어 중 하나이다.

### 출처
- https://nachwon.github.io/django-deploy-3-nginx/  
- https://nachwon.github.io/django-deploy-2-wsgi/  
