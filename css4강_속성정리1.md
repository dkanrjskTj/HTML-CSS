# CSS 속성(property)
### CSS 단위

| 단위 | 설명 |
| --- | :--- |
| px(픽셀) | 픽셀 단위를 의미 |
| em(배수표현) | 기존 글꼴에 대한 상대적 크기(1배, 2배 등의 배수)를 의미 (1.3em=130% 원래 글꼴의 1.3배 크기) |
| %(배율) | 기존 글꼴 크기에 대한 상대적 크기를 퍼센티지 비율로 표시 (100%=원래 글꼴 크기) |

<br/>

### Color관련 속성

| 방법 | 설명 |
| --- | :--- |
| 색상의 이름으로 표현 | "red" |
| 16진수로 표현 | #FF0000 |
| 10진수로 표현 | rgb(255,0,0) |
| RGB퍼센트로 표현 | rgb(100%,0%,0%) |

+ 색상과 관련된 속성
    + color (텍스트의 색상)
    + baxkground-color (배경의 색상)
    
<br/>

### Font관련 속성

| 속성 | 설명 |
| --- | :--- |
| font |  한 줄에서 모든 폰트 속성을 설정할 때 사용 |
| font-family | 글꼴의 종류를 지정 |
| color | 폰트의 색상을 지정 |
| font-size | 폰트의 크기를 지정 |
| font-weight | 폰트의 굵기를 지정 (bold, normal 중에 선택할 수 있다) |
| font-style | 폰트의 기울임을 지정 (italic, normal 중에 선택할 수 있다) |

<br/>

### Text관련 속성

| 속성 | 설명 |
| --- | :--- |
| color | 텍스트 색상 지정 |
| direction | 가로쓰기, 세로쓰기 지정(텍스트 작성 방향) |
| letter-spacting | 글자간 간격 지정 |
| line-height | 텍스트 줄 높이 지정* (ex. 세로로 가운데 정렬할때 사용하기도 함) |
| text-align | 텍스트 수평 정렬 지정 |
| text-decoration | 텍스트 장식 설정 (ex. 링크 태그에 밑줄없이 출력) |
| text-shadow | 그림자 효과 지정 |
| text-transform | 대소문자 변환 지정 |

<br/>

### 배경(background) 관련 속성

| 속성 | 설명 |
| --- | :--- |
| background-color:색상; | 배경 색상을 표시 |
| background-image:url("파일경로"); | 배경에 넣을 이미지를 지정 |
| background-attachment:상수 값; | 상수값 :<br/> fixed : 배경 이미지를 고정<br/> scroll : 스크롤 시 문장과 함께 배경 이미지도 함께 하도록 한다.(기본 설정값) |
| background-size:값; | 삽입된 배경 이미지의 너비와 높이를 지정 |
| background-reprat:상수 값; | 상수값 : <br/> no-repeat : 배경 이미지 반복없이 한번만 화면에 표시<br/> repeat-x : x축(가로) 방향으로 반복 표시<br/> repeat-y : y축(세로) 방향으로 반복 표시 |
| background-position:상수 값; | 상수 값 : top/bottom : 이미지를 위/아래쪽에 정렬<br/> left/center/right : 이미지를 왼쪽/가운데/오른쪽으로 정렬 |

<br/>

### 문단 관련 속성
+ margin : 문단의 여백을 설정
+ padding : 내용과 테두리 간의 여백을 설정

| 속성 | 설명 |
| --- | :--- |
| margin-top:값 | 문단 경계로부터 위쪽에 여백을 지정 |
| margin-left:값 | 문단 경계로부터 왼쪽에 여백을 지정 |
| margin-right:값 | 문단 경계로부터 오른쪽에 여백을 지정 |
| margin-bottom:값 | 문단 경계로부터 아래쪽에 여백을 지정 |









