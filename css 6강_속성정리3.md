# CSS 속성(property)
### position
**1. position : 속성;**

| 속성 | 설명 |
| --- | --- |
| static(기본 값) | 기준 없음 |
| relative | 요소 자신을 기준 |
| absolute | 위치 상 부모 요소를 기준, 부모요소를 가지지 않으면 body요소를 기준으로 위치 설정 |
| fixed | 뷰포트(브라우저)를 기준, 스크롤을 움직여도 화면에서 고정 시키기 위해 사용 함 |
| sticky | 스크롤 영역 기준 |

+ position 과 CSS 속성 : 모두 음수를 사용할 수 있음
+ top, bottom, left, right : 요소의 각 방향별 거리 지정
+ auto(기본 값) : 브라우저가 계산
+ 단위 : px, em, rem 등 단위로 지정
+ 부모 요소에 position: relative를 작성 함

<br/>

**2. 요소 쌓임 순서(Stack order)** : 어떤 요소가 사용자와 더 가깝게 있는지(위에 쌓이는지) 결정
+ 요소에 position 속성의 값이 있는 경우 위에 쌓임. (기본값 static 제외)
+ 1번 조건이 같은 경우, z-index 속성의 숫자 값이 높을 수록 위에 쌓임
+ 1번과 2번 조건까지 같은 경우, HTML의 다음 구조일수록 위에 쌓임

```
﻿.container {
width: 300px;
background-color: royalblue;
position: relative;
}
.container .item {
width: 100px;
height: 100px;
border: 4px dashed red;
background-color: orange;
}
.container .item:nth-child(1) {
position: relative;
}
.container .item:nth-child(2) {
position: absolute;
top: 50px;
left: 50px;
}
.container .item:nth-child(3) {
}
```

**3. z-index**
+ 요소간의 겹치는 순서를 지정
+ 순서는 음수, 양수, 모두 사용할 수 있으며, 크기가 클수록 위에 위치하고 작을수록 아래에 위치한다.
   + auto : 부모 요소와 동일한 쌓임 정도
   + 숫자 : 숫자가 높을수록 위에 쌓임(음수도 사용 가능, 음수는 뒤에 쌓임)

 ※ z-index 사용 시 주의사항은 요소를 제일 위로 보내기 위해 999와 같은 과도하게 큰 값을 무작정 사용하는 것은 비효율적이다.   
실제로 이 경우 나중에 유지보수 시 어려움을 겪기에 숫자 1부터 차례대로 사용하는 것을 권장한다.

<br/>

### float
**float:배치;**   
float:left; / float:right; - 요소를 왼쪽/오른쪽에 배치   
※ 웹페이지 가운데 정렬 - **margin:0 auto;**
+ HTML 요소가 수평으로 나열된 다른 요소들과 자연스럽게 어울리도록 만들어준다.
+ float를 적용받은 요소의 다음 요소들이 끌어올려진다.
+ float를 적용받은 요소의 방향을 결정(left, right)한다.
+ 컨텐츠 크기만큼만 영역을 설정하고, float를 적용받은 요소는 다른 요소보다 위쪽에 위치한다.

<br/>

### clear
+ float 속성이 적용된 이후 나타나는 요소들의 동작을 조절한다.
+ float 속성이 적용되면 그 이후에 등장하는 모든 요소들은 정확한 위치를 설정하기 어려워진다.
+ clear 속성을 사용하면 이후에 등장하는 요소들이 더 이상 float 속성에 영향을 받지 않도록 설정할 수 있다.   
**clear:float** 배치 설정을 무시하고 새롭게 배치를 하는 속성   
clear:left; / clear:right;

<br/>

### gradient 
그라데이션(gradient)이란 둘 이상의 색 사이의 색상 표현을 부드럽게 전환해주는 효과를 의미합니다.
+ 두 개 이상의 색상 사이에서 색상의 점진적인 변화

| 속성 | 설명 |
| --- | --- |
| linear-gradient(..) | 선형 그라데이션 |
| repeating-linear-gradient(..) | 선형 그라데이션 반복 |
| radial-gradient(..) | 방사형 그라데이션 |
| repeating-radial-gradient(..) | 방사형 그라데이션 반복 |


• 그라데이션 코드값을 계산해주는 사이트
     참고 - (http://www.colorzilla.com/gradient-editor/)



