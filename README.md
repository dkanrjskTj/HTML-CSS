# HTML기본
## HTML 기본형식

Markup Language인 HTML은 태그(tag)를 이용해서 문서와 데이터의 구조를 표현한다.<br />
태그는 시작하는 태그와 끝내는 태그 한쌍으로 이루어져있는 것이 기본이지만 \<br\>, \<hr\>처럼 홀로 쓰이는 태그도 있다.
<br />
<br />

* \<!DOCTYPE html\> : 해당 웹문서가 어떤 버전의 HTML 언어로 작성되었는지 알려주는 선언문
* \<html\>태그 : HTML문서의 시작과 끝을 알림
* \<head\>태그 : 해당 웹문서의 정보(작성자, 작성도구, 설명, 인코딩 등)을 웹브라우저에 알려주는 영역
* \<title\> 태그 : 웹페이지의 제목 태그
* \<body\>태그 : 웹브라우저에 표현할 내용을 입력하는 영역
<br />
  
 ```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>HTML문서의 타이틀</title>
<style>CSS를 입력하는 영역</style>
</head>
  
<body>
웹브라우저에 실제로 정보를 전달하기위한 영역
</body>
</html>
```
<br/>

  ![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfMTM3/MDAxNjM2NDY0NDI0MTIw.EeiqX6WkCbuxqbRPoj8mKEVjdLWPsW2QnYanFM9WEgwg.ccBxYOc1DLOivDCpl81GvVmOReL9tZZZ569dYWNYklkg.JPEG.daykkk/%EA%B0%95%EC%9D%981.JPG?type=w966)
  <br/>
  <br/>
  <br/>
  
  ### [주석입력]
코드작성시에 코드설명 등을 위해 꼭 필요한 주석 삽입
주석은 <mark> \<!-- [주석내용] --\> </mark> 이렇게 입력한다.
  
* 단축기 ctrl + / 를 누르면 자동으로 주석영역이 생성된다.
* 주석은 브라우저를 통해 코드가 노출되지는 않지만, 소스보기를 통해 확인이 가능하다.
* 만약 주석내용이 드러나는 것을 원하지 않을 경우 JSP 주석을 사용해야 한다.
<br/>

![alt 예제](https://postfiles.pstatic.net/MjAyMTExMDlfNzIg/MDAxNjM2NDY0NTQ5MTkw.uzY46coN0utexaxmn_kSgVVo9MIN9QBu7-wwLiH1de8g.uEk53DaJkTbGsNlIXf4AtjPM6kkBM92prxOAyUZC45Ig.JPEG.daykkk/2.JPG?type=w966)

