# HTML 목록(리스트) 태그
### \<ul\>태그 - 순서 없는 목록
+ ul은 Unordered List의 약자 **\<ul\> \</ul\>**
+ 목록은 \<li\> 태그로 작성하며, \</li\> 태그는 생략 가능
+ 블럭엘리먼트
+ 불릿형태로 목록이 출력

```
<ul>
<li>목록1
<li>목록2
</ul>
```

![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfMjI5/MDAxNjM2NDY1OTIxMDUz.1cnkbeYMciSptnFIX8q1dmp9LVc5s2wzNNn8_J4857gg.I7IOfbMdqyH4F1qWo4Kr-fdqobKYtykbZiFLzs_FPrwg.JPEG.daykkk/7.JPG?type=w966)

<br/>
<hr/>

### \<ol\>태그 - 순서 있는 목록
+ ol은 Ordered List의 약자 **\<ol\> \</ol\>**
+ 목록은 \<li\>태그로 작성하며 \</il\>태그는 생략 가능
+ 블럭엘리먼트
+ 1,2,3으로 목록이 출력 (type="1"이 디폴트값)
+ [주요속성]
   + type : 목록에 사용되는 마커를 지정(1, A, a, I, i)
   + start : 시작 목록의 순번을 지정
   + reversed : 항목을 역순으로 표시

```
<ol type="1" start="1">
<li>순서1
<li>순서2
</ol>
```

![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfMTIz/MDAxNjM2NDY2MjY4MTAx.7Le0_GUCT21rUfbZnMFmIxgfC0Pr88ngrAzlhPJQM6Qg.ZADcBE2PHkDqOmclno9y-0yhpqQ409VkEmVrdqUR7HEg.JPEG.daykkk/8.JPG?type=w966)

<hr/>

### \<dl\>태그 - 설명목록
+ dl은 Definition List의 약자 **\<dl\> \</dl\>**
+ 제목과 설명이 한 쌍인 설명 목록을 만들때 사용
+ 목록은 단어태그\<dt\>와 설명태그\<dd\>로 작성
   + dl - Definition list : 정의 목록
   + dt - Definition Term : 정의할 용어
   + dd - Definition Description : 용어 설명
+ 블럭엘리먼트
+ ※유의사항
   1. dl을 사용할 경우 dt와 dd를 같이 써야됨.
   2. dl의 자식요소는 반드시 div, dt, dd만 사용이 가능
   3. dt와 dd는 반드시 dl의 자식 요소로 존재해야함.
```
<dl>
<dt>단어1</dt>
<dd>설명1</dd>
<dt>단어2</dt>
<dd>설명2</dd>
</dl>
```

![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfMTk5/MDAxNjM2NDY2Mzk0MDA0.sFcjXxLS-xdHaSdOq7n0rAngVYQpvlAVcNp9u5xqv6sg.bD9ibgdIcck7bLRLjRBGCh1UnWGABkypcaasIuWfVaAg.JPEG.daykkk/9.JPG?type=w966)

<br/>
<hr/>

### 코드작성 Tip Emmet활용
목록태그들은 여러 개의 동일한 태그를 반복하여 입력하기 때문에 Emmet 기능을 활용하는 것이 편리하다.

​1. **! 엔터**를 누르면 **html의 기본 뼈대**가 나다난다.

![alt html](https://postfiles.pstatic.net/MjAyMTExMDlfMjYg/MDAxNjM2NDY3NTY4MTMx.Bi5Cy3RMn_8hyuLNA44tT1ZNfp2FVpvsZ8KbrWsVeiog.YwW4aGoRzq1tQ5wnXelp3YEZzJGL5OhX8ImoZpvc0Bcg.JPEG.daykkk/14.JPG?type=w966)

2. \<li\> 태그가 4개인 \<ul\> 태그 작성 시 **ul\>li\*4**를 입력하면 아래와 같이 자동완성이 뜬다.   
여기서 탭 혹은 엔터를 누르면 아래처럼 한번에 태그 구조를 입력할 수 있다.


![html](https://postfiles.pstatic.net/MjAyMTExMDlfMjMg/MDAxNjM2NDY3NjM3MTU3.FQ5lb6wJNhzo5vybgoo5l8fNDS8fKpo7jk-fkwi-cMMg.8nKg39tJNg-3rirwpusZ_hF4DAWJjkqQUqscpOB3_yYg.JPEG.daykkk/15.JPG?type=w966)
