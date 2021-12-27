# box-sizing태그
### margin/padding 태그

+ margin: 문단의 여백을 설정
+ padding: 내용과 테두리 간의 여백을 설정

![alt css](https://postfiles.pstatic.net/MjAyMTExMjRfMTk1/MDAxNjM3NzE2NjI2MDE4.rVYTi1f3P9wKTYN00wqgQXBtfmj834gZsjsj9SJyffsg.L9v9X8vz5EUpGZcVgqdGGqfTdCvggYHUX-zq5eWupXog.JPEG.daykkk/margin1.JPG?type=w966)

<br/>

### 크기 계산 (box-sizing) 
: 요소의 크기 계산 기준을 지정

+ content-box: 요소의 내용(content)으로 크기 계산 (기본 값)
+ border-box: 요소의 내용 \(+ padding\) \(+ border\)로 크기 계산   
※ 요소에 지정한 (CSS 중 .item) 가로너비와 세로 너비 만큼 정확한 크기로 내부 여백과 크기를 정하고 싶다면, box-sizing을 border-box로 함

```
<style>
.box {
width: 200px;
height: 120px;
border: 20px solid black;
padding: 30px;
}
</style>
<body>
<div class="box">
</div>
</body>
```

![alt css](https://postfiles.pstatic.net/MjAyMTExMjRfMjgy/MDAxNjM3NzE4Mzc0NTgz.2dnA5rr-udX9gotj3AUEd_AdhzlaDOj65mpimQdxLy8g.QzG_dBM9C3oItGW5_ssYEGA5bE4Son4Ff_hFCab8bmgg.JPEG.daykkk/margin2.JPG?type=w966)

+ content-box;
   + content-box 속성을 지정할 경우 컨텐츠 영역을 기준으로 크기를 결정
   + box-sizing 속성을 별도로 지정하지 않을 경우 content-box속성으로 설정 되기 때문에 결과 화면은 왼쪽 화면 처럼 나타나게 됨

<br/>

+ border-box;
   + border-box 속성을 지정할 경우 테두리를 기준으로 크기를 결정
   + border와 padding 영역을 포함한 전체길이가 지정한 만큼 설정 되기 때문에 위 이미지의 오른쪽 처럼 크기가 지정

<br/>

+ 아무것도 설정하지 않을 경우
   + 기본값으로 content-box 속성이 지정되기 때문에 위 예제의 경우 왼쪽의 이미지 처럼 결과화면이 나타나게 됨