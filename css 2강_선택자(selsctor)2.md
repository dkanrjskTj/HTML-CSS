# CSS 선택자(selsctor)
### 속성 선택자

+ html 요소에서 src, href, style, type, id, class...와 같은 속성을 선택자로 지정해서 스타일을 적용
+ class 속성을 가진 ul 태그 중, li 라는 자손 모두에 적용
+ target 속성을 가지며, 그 값이 _self인 a태그에 적용   
**[속성명]{선언문;}**

```
ul[class] li {
width: 24%;
height: 50px;
display: inline-block;
}
a[target="_self"] {
border: 1px solid darkgray;
border-radius: 5px;
background-color: white;
padding: 5px;
}
```

+ 문자열 속성 선택자

| 선택자 | 형태 설명 |
| --- | --- |
| [속성=”값”] | 특정 값인 태그 선택 |
| [속성~=”값”] | 특정 값을 단어로 포함하는 태그 선택 / 띄어쓰기 기준 (alt=”바다 사진” / [alt~=”바다”]) |
| [속성|=”값”] | 특정 값을 단어로 포함하는 태그 선택 / 하이픈 기준 (alt=”바다-사진” / [alt|=”바다”) |
| [속성^=”값”] | 특정 값으로 시작하는 태그 선택 (alt=”apple banana” / [alt^=”app”]) |
| [속성$=”값”] | 특정 값으로 끝나는 태그 선택 (href=”ssafy.com/istj” / [href$=”istj”]) |
| [속성*=”값”] | 특정 값이 포함된 태그 선택(들어만 있으면 됨) (alt=”미세먼지싫어” / [alt*=”세먼지”]) |

+ 선택자의 우선순위
    + 태그 vs 클래스 : 클래스 선택자 우선
    + 태그 vs 아이디 : 아이디 선택자 우선
    + 태그 vs 아이디 vs 클래스 : 아이디 선택자 우선   
※최종 우선 순위 : 아이디 > 클래스 > 태그 > 전체 (요소들의 갯수 순서대로 라고 볼 수 있음)

+ CSS의 선택자는 **아래의 우선순위를 가짐**

<br/>

### 순서에 따른 가상 클래스 선택자
+ 클래스를 추가할 필요없이 요소 중에서 순서에 따라 원하는 특정 요소를 선택하여 스타일 적용   
**.클래스이름>선택바{속성:속성값;}**

| 태그 | 설명 |
| --- | --- |
| 태그:first-child | 태그의 요소중에서 첫번째에 해당하는 요소의 스타일을 적용 |
| 태그:last-child | 태그의 요소중에서 마지막에 해당하는 요소의 스타일을 적용 |
| 태그:nth-child(n) | 태그의 요소중에서 n번째에 해당하는 요소의 스타일을 적용 |
| 태그:nth-child(odd) | 태그의 요소중에서 홀수번째에 해당하는 요소의 스타일을 적용 |
| 태그:nth-child(even) | 태그의 요소중에서 짝수번째에 해당하는 요소의 스타일을 적용 |

+ 예제 1

![alt css](https://postfiles.pstatic.net/MjAyMTExMTVfMjA0/MDAxNjM2OTg0ODIxNDQ5.qSDzQAGiZEmYsuoiwdrgj-_IJaOU6H_cmgNDKuMMhvkg.Y9kbFgY6i_H__l5iP9D9R5_qjNX_LeBu0DNLUEtK6bkg.JPEG.daykkk/10.JPG?type=w966)

+ 예제 2

![alt css](https://postfiles.pstatic.net/MjAyMTExMTVfMTA2/MDAxNjM2OTg0OTAzMDI4.gWWdyp-q17D816JYkcEL9qIRxpOSCYnL0Et4nz4RDzcg.-fapRd8zAklT98cZmcKq-78bURewl3RQkgqmrPyA12cg.JPEG.daykkk/11.JPG?type=w966)

<br/>

### 가상요소 선택자

| 태그 | 설명 |
| --- | --- |
| ::before | 글, 이미지, 그라데이션 등을 요소 앞에 삽입한다. |
| ::after | 글, 이미지, 그라데이션 등을 요소 뒤에 삽입한다. |
| ::link | 하이퍼링크가 연결됐을때 스타일을 지정한다. |
| ::visited | 특정 하이퍼링크를 방문한 적이 있을때 스타일을 지정한다. |
| ::hovor | 마우스가 올라갔을 때를 바꾼다. |
| ::active | 마우스 버튼을 클릭하고 있을 때 스타일을 지정한다. |

+ 예제) ::hovor

![alt css](https://postfiles.pstatic.net/MjAyMTExMTVfMjE1/MDAxNjM2OTg0NTc3Nzgw.hGdYE10AA343gL3xb46PpWpggng-zZawlrhCZ7wJwqkg.MbRHcDlFt--Cd-7CeLJvWKUL_J9nYMoKSsKAGKfzbHYg.JPEG.daykkk/7.JPG?type=w966)



