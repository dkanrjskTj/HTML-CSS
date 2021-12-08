# CSS 기본
+ HTML의 제한된 기능을 추가적으로 처리하기 위하여 개발된 것으로   
기존 HTML 태그에 추가적 스타일을 설정하여 보기 좋은 웹페이지 구현을 가능하게 한다.
+ CSS 구조

|웹페이지의 골격 HTML | 웹페이지를 꾸며주는 CSS|
|:---|:---|
| \<head\><br/>호출 혹은 직접 작성한다.<br/>\</head\>| 표 : 웹페이지마다 조금씩 다른 테두리 색을 지정한다. <br/>글꼴 : 다양한 글꼴 및 색상을 지정한다. <br/>표 스타일, 글꼴 스타일|
|\<body\><br/>내용에 영향을 준다.<br/>\</body\>||

+ CSS 기본 문법 형식
```<head>
  <style>
    CSS 블록 기술
  </style>
</head>

​<body>
    내용 기술
</body>
```

+ CSS 블록의 구성   
**선택자 {속성명: 속성값;}**   
ex) body {background:black;}

```<head>
 <style>
 body{background:black;}
 p{color:white;}
 </style>
</head>

<body>
<p>안녕하세요</p>
</body>
```

![alt css](https://postfiles.pstatic.net/MjAyMTExMTNfMjU1/MDAxNjM2NzkzNzkwMzI3.rF4Qr-kYXzIMOcvcfGqGUkQNHaBvPpp5SkBPu9tFkkQg.gBvUD9xL6u8__fd-Dc1Yk_YWYoPatH7oBCNpEhiSfaMg.JPEG.daykkk/1.JPG?type=w966)

<br/>
<hr/>

### 캐스캐이딩(Cascading)
요소는 하나 이상의 CSS 선언에 영향을 받을 수 있다   
이때 충돌을 피하기 위해 CSS 적용 우선순위가 필요하다

+ 중요도 : CSS가 어디에 선언되었는지에 따라 우선순위가 달라짐<br/>
    우선순위 1 > 4
   1) 인라인 스타일(HTML 요소 내부의 style 속성으로 사용)
   2) 내부 스타일 시트(HTML 문서의 style 태그안에 사용)
   3) 외부 스타일 시트(CSS 파일을 따로 만들어 불러와 사용)
   4) 웹 브라우저 기본 스타일 (폰트크기 : 16px)

+ 명시도 : 명확하게 특정할 수록 우선순위가 높다<br/>
!important > 인라인 스타일 > id 선택자 > 클래스 선택자 > 태그 선택자 > 전체 선택자 > 상속받은 속성

   → !important 를 이길수 있는 스타일은 없다

+ 선언순서 : 나중에 선언된 스타일이 우선 적용
여러개 클래스 명을 사용하는 경우에도 나중에 선언된 스타일이 우선 적용된다
<br/>

# CSS사용 방법
### 인라인 스타일(Inline Styles)
+ 스타일을 적용하고 싶은 HTML태그안에서 직접 기술하는 방법
+ 간단한 스타일 정보라면 스타일 시트를 사용하지 않고도 적용할 대상에 직접 표기
+ 웹 콘텐츠와 스타일시트 분리 위해서는 사용하지 않는게 좋음

### 내부 스타일 시트(Internal Style Sheet)
+ HTML문서내에서 \<head\>와 \</head\>사이에 \<style\> \</style\>을 정의하는 방법
+ HTML문서마다 스타일을 매번 지정해 주어야 하지만, 한 문서에만 해당되는 스타일을 지정할때 사용

```
<head>
<title></title>
<style>
ul { background-color: #000000;}
ul>li { color: pink;}
</style>
</head>
```

### 외부 스타일 시트(External Style Sheet)
+ css파일을 따로 만들고 이 파일을 HTML 문서에 불러와 사용하는 방법
+ 확장자가*.css인 스타일시트 파일을 생성해 CSS코드를 작성하고 HTML 문서에 연결
+ 홈페이지 전체의 스타일을 일관성있게 유지하면서 변경시에도 일괄적으로 변경되므로 홈페이지 제작의 효율성을 극대화
+ \<link\> 태그는 HTML 문서의 \<head\> \</head\> 내부에서 사용
   + herf : 연결하고자 하는 외부 소스의 url을 기술하는 속성
   + rel : 현재 문서(HTML)와 외부 소스의 연관 관계를 시술하는 속성

```
<head>
 <link rel="stylesheet" href="mystyle.css">
</head>
```
