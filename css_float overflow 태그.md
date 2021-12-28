# float 해제 방법
```
<div class="container">
  <div class="wrapper">
    <div class="element1">element1</div>
    <div class="element2">element2</div>
  </div>
</div>
```

```
<style>
  .container {
    width: 600px;
  }
  .wrapper {
    position: relative;
    border: 1px dashed red;
    padding: 10px;
  }
  .element1 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: red;
  }
  .element2 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: yellow;
  }
</style>
```

부모 영역인 wrapper 영역 밖으로 두개의 div element가 이탈해서 보여진다.

![alt css](https://postfiles.pstatic.net/MjAyMTExMjlfMjA3/MDAxNjM4MTc2ODMyNDY1.lwukxvQmqorL68pHokoPdi7FdIxjHKPIbR3ebOjsic0g.N9glnJENmAuZLbFbH3iLbsjIzaY4hB5CjhQ_SU-0yhQg.JPEG.daykkk/float%ED%83%9C%EA%B7%B81.JPG?type=w966)

이렇게 float 속성 사용 후 부모요소인 wrapper영역의 배치에 영향을 줄 경우 float 속성의 해제가 필요함

<br/>

### float 해제 방법
+ 부모 요소에 overflow : hidden 속성 주기
+ 인접하는 다음 형제 요소에 clear 속성 주기
+ 가상 요소를 사용하여 clear 속성 주기

<br/>

### 방법1. 
첫번째 방법은 부모 요소인 wrapper영역에 overflow: hidden 속성을 부여하는 방법
```
<style>
  .container {
    width: 600px;
  }
  .wrapper {
    overflow: hidden;
    position: relative;
    border: 1px dashed red;
    padding: 10px;
  }
  .element1 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: red;
  }
  .element2 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: yellow;
  }
</style>
```

overflow: hidden 속성 부여 하게 되면 부모 영역인 wrapper영역이 아래와 같이 정삭적으로 자리잡게 된다.

![alt css](https://postfiles.pstatic.net/MjAyMTExMjlfMjk2/MDAxNjM4MTc2OTAxOTA3.XtOD8_wfPJj8fivYzE44AIspwUFF4wEkrHfqaPbSwEUg.rx5xkl-UT8UDPtE_EVlRg6UqEwabRKXVFAJIxLGz72Ig.JPEG.daykkk/float%ED%83%9C%EA%B7%B82.JPG?type=w966)

하지만 이 경우에 주의할 사항이 하나 있습니다.   
div element를 하나 더 추가하여 absolute 포지션을 주고 위치를 조정하면

```
<div class="container">
  <div class="wrapper">
    <div class="element1">element1</div>
    <div class="element2">element2</div>
    <div class="element3">element3</div>
  </div>
</div>
```

```
<style>
  .container {
    width: 600px;
  }
  .wrapper {
    overflow: hidden;
    position: relative;
    border: 1px dashed red;
    padding: 10px;
  }
  .element1 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: red;
  }
  .element2 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: yellow;
  }
  .element3 {
    position: absolute;
    top: 60px;
    left: 300px;
    width: 80px;
    height: 80px;
    background-color: green;
  }
</style>
```

아래와 같이 부모에 적용된 overflow: hidden 속성 때문에 position: absolute 속성을 지닌 요소가 새로 삽입될 경우 영역 일부가 숨겨져 보이지 않게 된다.

![alt css](https://postfiles.pstatic.net/MjAyMTExMjlfNTYg/MDAxNjM4MTc2OTYyNDQ0.GopsEKN7LXj_yiAOWTIDnGfxvZtrreF4E8PFSOgkhq8g.k87pIf-ZuV8kDMIIxr6oY--puewcKsy5xEUFCizVki0g.JPEG.daykkk/float%ED%83%9C%EA%B7%B83.JPG?type=w966)

위 방법 을 해결하기 위한 두번째 방법

<br/>

### 방법2. 
두번째 방법은 인접하는 다음 형제 요소에 clear 속성 주는 방법 입니다.

<br/>

마지막 요소로 clear element를 추가하고 clear:both 속성을 추가 하여 주었습니다.   
(clear:both 속성 사용을 위해서는 display: block 속성변경이 필요)

```
<div class="container">
  <div class="wrapper">
    <div class="element1">element1</div>
    <div class="element2">element2</div>
    <div class="element3">element3</div>
    <div class="clear"></div>
  </div>
</div>
```

```
<style>
  .container {
    width: 600px;
  }
  .wrapper {
    position: relative;
    border: 1px dashed red;
    padding: 10px;
  }
  .element1 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: red;
  }
  .element2 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: yellow;
  }
  .element3 {
    position: absolute;
    top: 60px;
    left: 300px;
    width: 80px;
    height: 80px;
    background-color: green;
  }
  .clear {
    display: block;
    clear: both;
  }
</style>
```

아래 결과와 같이 부모 요소도 정상적으로 자리잡고 element3의 경우에도 잘리지 않고 모두 표시 되는 것을 확인 할 수 있습니다!


![alt css](https://postfiles.pstatic.net/MjAyMTExMjlfMzkg/MDAxNjM4MTc3MDIzMzA5.z0Eoanr_7V65trBS49U-wbHy5F2ZTK3YO6H8Xk9JtYsg.LODop999usFASXPnd0BuGzNC36EL5zFncJdqsX66GNUg.JPEG.daykkk/float%ED%83%9C%EA%B7%B84.JPG?type=w966)

clear 속성의 경우 float 해제를 위한 속성으로 깔끔하게 float속성 해제가 가능하지만 위 방법의 경우 clear element와 같은 의미 없는 빈 요소를 추가해야 합니다.   
때문에 각 태그별로 의미를 갖는 시멘틱 마크업에 위배 되고 불필요한 요소가 추가되게 됩니다.   
이를 개선 할 수 있는 마지막 방법을 알아보겠습니다.   

<br/>
 
### 방법 3. 
가상 요소를 사용하여 clear 속성 주기

<br/>

html에 불필요한 태그를 추가하지 않고 float속성을 부여한 부모요소에 가상요소인 ::after를 추가하여 거기에 clear 속성을 부여하는 방법입니다.   
(가상요소::after 사용시에는 추가할 내용이 담긴 content:' '를 써 주어야 합니다.)

```
<div class="container">
  <div class="wrapper">
    <div class="element1">element1</div>
    <div class="element2">element2</div>
    <div class="element3">element3</div>
  </div>
</div>
```

```
<style>
  .container {
    width: 600px;
  }
  .wrapper {
    position: relative;
    border: 1px dashed red;
    padding: 10px;
  }
  .element1 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: red;
  }
  .element2 {
    float: left;
    width: 80px;
    height: 80px;
    background-color: yellow;
  }
  .element3 {
    position: absolute;
    top: 60px;
    left: 300px;
    width: 80px;
    height: 80px;
    background-color: green;
  }
 .wrapper::after {
    content: '';
    display: block;
    clear: both;
  }
</style>
```

시멘틱 태그에도 위배 되지 않고, 요소의 잘림 현상이 없는 최종 결과 화면
![alt css](https://postfiles.pstatic.net/MjAyMTExMjlfMzAw/MDAxNjM4MTc3MjA3OTM5.IqsW5_FbwvreVEBYavvB7iBwnidCH3x11ndxJdovRjcg.CvPesMf0y3NGN_zK6xo5FxwTDNr5Z2MuiFWzuwfMYv8g.JPEG.daykkk/float%ED%83%9C%EA%B7%B85.JPG?type=w966)

<br/>

# overflow
+ **overflow: hidden;**
+ 요소의 크기 이상으로 내용(자식요소)이 넘쳤을 때, 내용의 보여짐을 제어

![alt css](https://postfiles.pstatic.net/MjAyMTExMjZfMTAg/MDAxNjM3OTE0OTkyNDQ0.diA66Tezj1VXjxMXqnqSiEmkC4tUYOJG_Cx5wA85lysg.t2PEsGD7LQW5Ok72L921QXogq_nCBmK7Y7GtX3y0ZpYg.JPEG.daykkk/overflow.JPG?type=w966)

| 속성값 | 내용 |
| --- | --- |
| visible(기본 값) | 넘친 내용을 그대로 보여줌 |
| hidden | 넘친 내용을 잘라냄 |
| scroll | 넘친 내용을 잘라냄, 스크롤바 생성 |
| auto | 넘친 내용이 있는 경우에만 잘라내고 스크롤바 생성 |












