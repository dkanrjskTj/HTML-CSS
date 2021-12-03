# HTML 텍스트 태그
### 제목 글자 태그

* 형식: **\<h1\> 제목내용 \</h1\>**
* \<h1\> 부터 \<h6\> 까지 있으며 \<h1\> 이 가장 크다.
* 볼드체 \<b\> 하고 줄바꿈 \<br\> 이 되는 태그가 기본으로 적용되어있다.
<br/>

![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfMjA1/MDAxNjM2NDY0OTg1NzUx.9sV5XY7F5TppVUyMttq0JuvCvVjTjRe2p3v-phsh5Zsg.z94TBGdE0ja6HOBcc7nfQX4MXg4_KIOkQRnCyYtLcQAg.JPEG.daykkk/3.JPG?type=w966)

<br/>
<hr/>

### 본문 태그
#### p태그
+ **\<p\> \</p\>**
+ 단락을 정의, 추가 공백이나 줄바꿈을 생략하여 출력
+ p태그와 p태그사이에는 문단의 구분을 위한 공백이 삽입
<br/>

#### hr태그
+ **\<hr\> \</hr >**
+ 콘텐츠 주제 변경을 정의
+ 수평줄이 출력된다
<br/>

#### br태그
+ **\<br\>**
+ 줄바꿈 태그
<br/>

#### pre태그
+ **\<pre\>**
+ 내부의 텍스트는 고정 너비 글꼴로 표시되며 공백과 줄 바꿈을 모두 유지
<br/>

#### blockquote태그
+ **\<blockquote\> \</blockquote\>**
+ 인용문을 표시할 때 사용되는 태그
+ 들여쓰기가 적용되며 글이 중앙정렬된 상태로 출력
<br/>
<hr/>

### 공백과 줄바꿈 태그
코드에 텍스트를 입력할 때 아무리 띄어쓰기를 하고 줄바꿈을 해도 공백 한칸으로 표시된다.
따라서 줄바꿈이나 한칸이상의 공백을 넣고 싶을 경우 아래 태그와 기호를 활용해야 한다.
+ 줄바꿈: **\<br\> 또는 \<br /\>** (종료태그가 없는 단일태그)
+ 한칸 이상의 공백: \&nbsp\;
<br/>

![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfMjkw/MDAxNjM2NDY1MTc5NjI0.U2bFfISTI1jw5Yej1qBgkyISWJapVC3xvYmZt9hq7M4g.6d0bw5Z2JhiGB6ObW-rNv9r8LbHgMeOs5__Rnj7AKbMg.JPEG.daykkk/4.JPG?type=w966)

<br/>
<hr/>

### 텍스트 효과 태그
+ 텍스트를 입력할 때 가장 기본으로 사용하는 글씨 굵기, 기울기, 밑줄긋기 등의 효과를 주는 태그
+ 태그 종류
   + \<b\> 볼드체
   + \<strong\> 볼드체(웹표준용)
   + \<i\> 이텔릭체
   + \<sup\> 윗첨자
   + \<sub\> 아랫첨자
   + \<ins\> 밑줄표시
   + \<del\> 취소선(웹표준용)
   + \<mark\> 형광펜으로 내용강조
+ 여러 효과 중복해서 사용 가능
<br/>
<hr/>

### 기타 특수기호 입력
웹문서에 따옴표(""), 엠퍼센트(&) 등의 특수기호는 코드로 활용되기 때문에 입력시 출력되지 않는다.   
따라서 엔티티 코드(Entity code)를 활용하여 특수기호를 입력할 수 있다.

|특수기호|엔티티 문자|엔티티 숫자|
|---|:---:|---:|
|공백(space)|\&nbsp\;|&#160|
|&|&amp|&#38|
|<|&lt;|&#8249|
|>|&gt;|&#62|
|"(따움표)|&quot;|&#34|


