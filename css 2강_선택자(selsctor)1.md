# CSS 선택자(selsctor)
CSS의 선택자는 스타일을 적용할 대상으로 HTML문서의 태그, ID, CLASS를 사용
CSS의 경우 가장 아래에 있는 CSS가 우선적으로 적용이 되지만 우선순위에 따라 적용 순서가 달라진다.   
**우선순위는 타입>Class>ID순서로 ID가 가장 높다.**

+ 특정태그를 선택하여, 해당 태그의 속성을 변경하는 목적으로 사용
    + 선택자 : 어떤 요소에 스타일을 적용할지에 대한 정보
    + {중괄호} : 선택한 요소에 적용할 스타일의 정의
    + 속성명 : 어떤 스타일 정의하고 싶은지에 대한 정보(색상, 크기)
    + **/"주석"/**
<br/>

# CSS 주요 선택자
### 전체(universal) 선택자
페이지 안의 모든 대상에 스타일을 지정할 때 사용   
사용 방법은 별표(⁎)문자로 지정하며 사용빈도가 가장 낮은 선택자(사용 시 속도가 느려질 수 있다)

**\⁎{스타일 속성: 값;\}**   
ex) \⁎{padding:0; margin:0;\}  (⁎은 전체 선택을 의미)

![alt css](https://postfiles.pstatic.net/MjAyMTExMTNfMTkw/MDAxNjM2ODEwNDU0MDc0.i7k_NjGI4J7EqaBoWrdn4_nWJR125b3xOMJhdknJJrcg.ZoQQJpnIcgWxKlgpJlQlxwGuhRW8BIAfpvLy1-2FIk8g.JPEG.daykkk/6.JPG?type=w966)

<br/>

### 타입 선택자
가장 기복적인 선택자로 스타일을 적용하고 싶은 태그명을 선택자에 입력하면, 그 태그에만 스타일이 적용   

**태그명\{스타일속성:값:\}**   
ex) p{color:orange;}  (html의 \<p\>\</p\>사이의 내용에 스타일을 지정)

![alt css](https://postfiles.pstatic.net/MjAyMTExMTRfMTAg/MDAxNjM2ODIzMDAyNTg4.5CC0Kv2V9Q-SzEfPDNsVzUob53_CV61F3btRE_nCbWEg.uUoN5YitmcP2PdP5PSmpWSVOeANvWMv-lXsZGpf1vxEg.JPEG.daykkk/3.JPG?type=w966)

<br/>

### id 선택자
지정한 id에 해당하는 영역에 대해서만 속성의 값이 적용   
아이디는 html문서안에 유일하게 하나만 가질 수 있음   
아이디를 id="green" 와 같이, 적용하고자 하는 태그에 아이디를 지정   

**\#id\{스타일 속성: 값;\}**   
ex) \<font id="aa"\>클래스 선택자\</font\>  (만약 html문서의 font부분에 이름을 aa로 지정했다면)   
#aa{color: orange;}  (id가 aa인 영역의 글자색만 오렌지 색으로 표시)

<br/>

### 클래스 선택자
지정한 클래스 명에 대해서만 속성의 값이 적용   
클래스를 class="blue" 와 같이 적용하고자 하는 태그에 클래스를 지정   
**.클래스명{스타일 속성: 값;}**   
ex) <font class="aa">클래스 선택자</font>  (만약 html문서의 font부분에 이름을 aa로 지정했다면)   
.aa{color: orange;}  (id가 aa인 영역의 글자색만 오렌지 색으로 표시)

![alt css](https://postfiles.pstatic.net/MjAyMTExMTRfOTAg/MDAxNjM2ODIzMTUwMjU2.AIjdlpJakhcnkkAcmxjSCZJFDi_mnYE_Mv6HTd4q8wMg.NnAS20QMr6pNFjWcZmIg0YXwLvMbt32yOfeW3DgyRRAg.JPEG.daykkk/4.jpg?type=w966)

<br/>

### 그룹 선택자
여러개의 요소를 나열하고 콤마(,)로 구분해 스타일을 적용   
**선택자, 선택자{속성:속성값;}**   
ex) h1{color:red;}         
    h2{color:red;}           =         h1, h2, h3{color:red;}  (두가지는 동일하다)   
    h3{color:red;}  

<br/>

### 자손 선택자
+ 조상요소 하위의 모든 요소에 스타일 적용
+ 여러개의 요소를 띄어쓰기를 이용해 구분
+ 아래의 경우, section 태그 안에 있는 모든 ul 태그에 속성이 적용   
**부모선택자 자손선택자{속성:속성값;}**
```
section ul { margin: 10px 0;}
```

<br/>

### 자식 선택자
+ 지정된 자식에게만 속성이 적용됨   
**부모선택자 > 자식선택자{속성:속성값;}**
```
section > ul > li { font-size: 20px; font-weight: bold;}
```

<br/>

### 인접 형제 선택자
+ 동일한 부모의 요소를 갖는 자식 요소들의 관계
+ a + ul : 같은 부모 내, a의 형제 요소 중 바로 뒤 (다음)의 ul에 적용   
**(부모가 같은)자손선택자+자손선택자{속성:속성값;}**

```
a + ul {
background-color: gold;}
```

<br/>

### 일반 형제 선택자
+ 형제 관계를 갖는 요소 중에서 형 요소 다음에 나오는 모든 동생 요소의 스타일을 적용
+ a ~ ul : a의 형제 요소 중, a 뒤에 오는 모든 ul에 적용   
**형선택자~동생선택자{속성:속성값;}**

```
a ~ ul {
border: 1px solid darkgray;}
```


