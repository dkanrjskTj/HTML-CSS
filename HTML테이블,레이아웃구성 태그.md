# HTML 표를 나타내는 테이블 태그
### \<table\>테이블 태그-표만들기 태그
+ **\<table\> \</table\>**
```
<table>
<tr>
<td>
</td>
</tr>
</table>﻿
```
+ 표 요소, 행(Row)과 열(Columm)의 집합
+ \<tr\> \</tr\> (table row) 표의 행을 만드는 태그
\<td\> \</td\>(table data) 표의 열을 만드는 태그

![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfNzYg/MDAxNjM2NDY5MDUzNjgw.7MvyTlIlftig4ceVDOPvfyR0K7lO0CW7jy6i_PIJPzEg.Oe4GjzmyWAZw2STH8RCCeYB8h4yttY0IbM_R_MwP0N8g.JPEG.daykkk/16.JPG?type=w966)

+ 전체 영역에서 사용할 수 있음. HTML body 부분에 모두 사용 가능
    + **title 속성** : 마우스 포인트를 올렸을때 설명 내용을 출력해 주는 속성
    + **style 속성** : 요소에 적용할 스타일(CSS)을 지정
    + **class 속성** : 요소를 지칭하는 중복 가능한 이름
    + **id 속성** : 요소를 지칭하는 고유한 이름
    + **data-원하는이름** : 요소에 데이터를 지정

+ 속성
   + **colspan** : 열을 합쳐주는 속성
   + **rowspan** : 행을 합쳐주는 역할
   + **border** : 두께, 굵기 설정

![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfMyAg/MDAxNjM2NDY5MzY2NjU3.6Xjz9neLweHbxXa4fk4uTCYUq4Q7lwnphnaa4ZE-ASUg.voyg4lbRmJusawPyS09pY0V8KWbdgPH4unQqeRPLQWMg.JPEG.daykkk/17.JPG?type=w966)

※colspan, rowspan을 사용하게 되면 합쳐지는 숫자에 맞춰 행과 열 숫자를 조정해준다.   
오류가 생길 확률이 높아 많이 사용되지는 않는다.

<br/>
<hr/>

# HTML 레이아웃 구성 태그
### 블럭엘리먼트와 인라인엘리먼트
**블럭 엘리먼트(Block Element)**
+ 컨텐츠 크기에 상관없이 무조건 가로영역을 모두 사용하는 하나의 블럭을 차지하여 세로로 배치된다.
+ 예시 태그: \<div\>*, \<hn\>, \<p\>, \<blockquote\>, \<dl\>, \<ul\>, \<ol\>

<br/>

**인라인 엘리먼트(Inline Element)**
+ 컨텐츠 크기에 따라 가로영역이 설정되어 컨텐츠들이 가로로 배치된다.
+ 예시 태그: \<span\>*
+ 블럭 엘리먼트, 인라인 엘리먼트 예제

![alt html](https://postfiles.pstatic.net/MjAyMTExMTNfMjkg/MDAxNjM2NzkxNjM1NTY1.AdlCEIAInk4oORbZNbtxUC7y8pUacwVFx6O18sCkM3sg.Z8JKC4bzYoTYeTrHYRjxdLl8t3ka9zfsjpBdpgAVtysg.JPEG.daykkk/19.JPG?type=w966)

+ \<div\>예제
  
![alt html](https://postfiles.pstatic.net/MjAyMTExMTNfMTg2/MDAxNjM2NzkyMDMyOTA0.xRxyxoL_z-zHfOC47YKu8dgbPo6QaMyjbaeuyuhxXHkg.7osgFg3XHlZ6TmxdXOniZlSGoe2rlTscNCApFH_169gg.JPEG.daykkk/20.JPG?type=w966)

<br/>
