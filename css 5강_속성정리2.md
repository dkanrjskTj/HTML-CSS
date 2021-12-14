# CSS 속성(property)
### 테두리선(border) 관련 속성
border : 선-두께(border-width) 선-종류(border-style) 선-색상(border-color);   
ex) .container .item:first-child {border: 10px(두께) solid(종류) black(색상);}

+ border-width (두께)

| 사용값 | 설명 |
| --- | --- |
| medium | 중간두께 (기본값) |
| thin | 얇은 두께 |
| thick | 두꺼운 |
| 단위 | px, em, % 등 |

+ border-style (종류)

| 사용값 | 설명 |
| --- | --- |
| none | 선 없음 (기본값) |
| solid | 실선 |
| dotted | 점선 |
| dashed | 파선 |
| double | 두줄 선 |
| groove | 홈이 파여있는 모양 |
| ridge | 솟은 모양 (groove의 반대) |
| inset | 요소 전체가 들어간 모양 |
| outset | 요소 전체가 나온 모양 |

+ border-color (색상)
    + black (기본 값) : 검정색
    + 색상 : 선의 색상
    + transparent : 투명
    + 색상표현
       1) 색상이름 : 브라우저에서 제공하는 색상이름 >> red, tomato, royalblue
       2) Hex 색상코드 : 16진수 색상(Hexadecimal Colors : 헥사데시멀) >> #000, #FFFFFF
       3) RGB : 빛의 삼원색 >> rgb(255, 255, 255)
       4) RGBA : 빛의 삼원색 + 투명도 >> rgba(0, 0, 0, 0.5)
       5) HSL : 색상, 채도, 명도 >> hsl(120, 100%, 50%)
       6) HSLA : 색상, 채도, 명도 + 투명도 >> hsl(120, 100%, 50%. 0.3)

+ border-방향
    + border-방향: 두께 종류 색상;
    + border-방향-width: 두께;
    + border-방향-style: 종류;
    + border-방향-color: 색상;

+ border-radius (레디어스)   
    : 요소의 모서리를 둥글게 깎음
  + 0 (기본값) : 둥글게 없음
  + 단위 : px, em, vw등 단위로 지정

<br/>

### 크기 계산 (box-sizing)   
요소의 크기 계산 기준을 지정
   + content-box (기본 값) : 요소의 내용(content)으로 크기 계산
   + border-box : 요소의 내용 + padding + border로 크기 계산

요소에 지정한 (CSS 중 .item) 가로너비와 세로 너비 만큼 정확한 크기로 내부 여백과 크기를 정하고 싶다면, box-sizing을 border-box로 함

<br/>

### 넘침 제어 (overflow)
요소의 크기 이상으로 내용이 넘쳤을 때, 보여짐을 제어하는 단축 속성
   + visible (기본 값) : 넘친 내용을 그대로 보여줌
   + hidden : 넘친 내용을 잘라냄
   + scroll : 넘친 내용을 잘라냄, 스크롤바 생성
   + auto : 넘친 내용이 있는 경우에만 잘라내고 스크롤바 생성

※ overflow-x   overflow-y : 개별 속성으로 사용 가능함

<br/>

### 출력 특성 (display)
요소의 화면 출력 (보여짐) 특성

| 사용값 | 설명 |
| --- | --- |
| block (각 요소의 기본 값) | 상자(레이아웃) 요소 |
| inline (각 요소의 기본 값) | 글자 요소 |
| inline-block (각 요소의 기본 값) | 글자 + 상자 요소 |
| flex | 플렉스 박스 (1차원 레이아웃) : 하나의 축을 기준으로 정렬에 용이 |
| grid | 그리드 (2차원 레이아웃) |
| none | 보여짐 특성 없음, 화면에서 사라짐 |
| 기타 | table, table-row, table-cell 등 |

<br/>

### 투명도 (opacity)
요소 투명도
   + 1 (기본 값) : 불투명
   + 0~1 : 0부터 1사이의 소수점 숫자
