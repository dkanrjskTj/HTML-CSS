# HTML Form태그 / Input 태그
### \<form\>태그
+ **\<form action="#"(서버쪽 주소를 입력) method="get/post"\>**
+ Form : 사용자로부터 어떤 정보나 데이터를 받기 위한 태그   
주의해야할 것은 Form을 사용한다는 것은 사용자로부터 무엇인가를 받고 그것을 처리하는 과정도 같이 들어가야 한다는 점
+ form을 사용할 경우 반드시 2가지 속성을 기재해주어야함   
    **\<form action="" method=""\> \</form\>**
   + method 속성 : 입력된 내용을 서버에 전달하는 방법으로 get과 post를 사용함
        + GET : 단순히 정보를 '읽고(read)' 싶을 때, 입력된 내용이 그대로 표시 됨
        + POST : 입력한 내용의 길이에 제한받지 않고, 입력된 내용이 표시되지 않음
   + action: 이력된 내용을 서버에 전달하는 위치
   + autocomplete 속성 : 자동 완성, 초기값은 on이며, off로 설정하면 자동 완성 목록을 표시하지 않음
   + name 속성 : 자바스트립트로 폼을 제어할 때 사용할 폼의 이름
   + target 속성 : action 속성에서 지정한 스트립트 파일을 현재 창이 아닌 다른 탭에서 열 때

```
 <body>
    <form method="get" action="formtest.php">
        <p><lable>Input Color:<input type="text" name="color"></lable></p>
        <p><input type="submit" value="Submit"></p>
    </form>
    </body>
```

![alt html](https://postfiles.pstatic.net/MjAyMTExMTNfMTg4/MDAxNjM2NzkyOTE2MzQ5.EvtL3BEyKsrIMQWqPX9mJ1tzA7koUEJThoDhkL3rgKEg.4HGh2mPGb-6Hh-cixu7pq7lRSvBK4AiZs-LuCnsutf8g.JPEG.daykkk/22.JPG?type=w966)

<br/>
<hr/>

### \<input\>태그

### Form#1 input / Syntax alert
**\<input type="text/\>**
+ type을 반드시 기재해주어야 함
+ input 태그의 type 속성

| type | 속성 설명 | 
|---|---|
|text | 한 줄짜리 텍스트를 입력할 수 있는 텍스트 박스 생성 |
| textarea | 여러 줄의 텍스트 입력 가능한 텍스트 박스 |
| password | 비밀번호를 입력하는 필드 생성 |
| search | 검색할 때 입력하는 필드 생성 |
| url | url을 이상한값을 적용하면 경고가 뜸 |
| email | text와 비슷하지만 다름, 이메일(@)을 입력하지않으면 넘어가지 않음 |
| tel | 전화번호를 적을수 있음 |
| checkbox | 주어진 여러 항목에서 2개 이상 선택할 수 있는 체크박스 생성 |
| number | 숫자로 값을 받기 위한 것 |
| file | 이미지 첨부할수 있게끔 하는것, 특정 파일을 제한 하는법 accecpt=".jpg, .pdf" |

+ input type 속성

| type | 속성 설명 |
|---|---|
| number | 숫자를 조절할 수 있는 스핀 박스 생성 |
| range | 숫자를 조절할 수 있는 슬라이드 막대 생성 |
| date | 사용자 지역을 기준으로 날짜(연, 월, 일) 생성 |
| month | 사용자 지역을 기준으로 날짜(연, 월) 생성 |
| week | 사용자 지역을 기준으로 날짜(연, 주) 생성 |
| time | 사용자 지역을 기준으로 시간(시, 분, 초, 분할 초) 생성 |
| datetime | 국제 표준시(UTC)로 설정된 날짜와 시간(연, 월, 일, 시, 분, 초, 분할 초) 생성 |
| datetime-local | 사용자가 있는 지역을 기준으로 날짜와 시간(연, 월, 일, 시, 분, 초, 분할 초) 생성 |
| submit | 전송 버튼 생성 / reset : 리셋버튼 생성 |
| image | submit버튼 대신 사용할 이미지 삽입 |

+ input 태그의 기타 속성

| 기타 | 속성 설명 | 
|---|---|
| name | PHP와 같은 웹 프로그래밍에서 폼 요소를 제어할 때 사용 |
| placeholder="" | 아무것도 값이 없을때 기본적으로 보여주는 text |
| value | placeholder와 비슷한 속성이지만, value는 그 값을 복사할수 있음, placeholder는 복사가 불가능|
| size | 텍스트와 비밀번호 필드의 길이|
| maxlength="" | input창에 작성할 수 있는 문자의 갯수를 제한하기 위한 속성|
| minlength="" " | input창에 작성할 수 있는 문자의 최솟값을 제한하기 위한 속성|
| placeholder | input 텍스트 상자 안에 표시되는 회색 글자|
| readonly | 입력할 수 없고 읽을 수만 있는 텍스트 상자 readonly만 입력(readonly="readonly" 또는 readonly="true") |
| autofocus | 폼을 열면 자동으로 커서가 표시되도록 설정 |
| required | 필수로 입력을 하지 않으면 동작하지 않게 하는 속성 |
| disable | input창을 사용하지 못하게 막아둠 |
| min="" | 입력할 수 있는 수의 최소값 |
| max="" | 입력할 수 있는 수의 최대값 |

<br/>

### From #2 Label
+ form 양식에 이름을 붙이는 태그
```
   \<label for="누구"\> 라벨 \</label\>
   \<label for="user-name"\>이름\</label\>
   \<input type="text" id="user-name"/\​>
```

<br/>

### Form #3 Radio & Check box
+ Radio : 여러가지 항목중에서 1가지만 선택이 가능하게끔 하는것 
+ Radio사용시 반드시 적어야하는 attribute가 2개가 있음
    + name : input type radio간 서로 연관이 있는것을 알려주기 위함
    + value: : 어떤 하나의 항목이 선택되어 서버에게 전달할때 구분을 하기 위해 각기 값을 설정해야 하는 값
+ check box : 여러가지 항목중에서 다중선택을 가능하게끔 하는 것
    (radio와 하는것은 같음)

```
    <input id="HTML" name="skills" value="html" type="checkbox"/>
    <label for="HTML">HTML</label>
    <input id="CSS" name="skills" value="css" type="checkbox"/>
    <label for="CSS">CSS</label>
    <input id="JavaScript" name="skills" value="javascript" type="checkbox"/>
    <label for="JavaScript">JavaScript</label>
```

<br/>

### Form #4 Select & Option
+ Select 여러개중 하나를 고르는 것

```
    <form action="" method="get">
    <label for="skill">스킬</label>
    <select multiple name="skills" id="skill">
    <option value="html">HTML</option>
    <option value="css">CSS</option>
    <option value="js">JavaScript</option>
    </select>
    <button type="submit">
    submit
    </button>
    </form>
```
+ select 아래 자식으로 option이 있기 때문에 id, for을 사용하지 않아도 됨

<br/>

### Form #5 Textarea
+ \<input type="text"\>는 한줄이상 기재가 불가능하지만 Textarea를 사용하면 그 이상을 사용가능   
\<textarea id="filed" cols="10" rows="10" placeholder="자기소개를 입력하세요"\> \</textarea\> 

<br/>

### Form #6 button
+ type이 총 3(button, submit, reset)개가 있으며 실제로 사용하는것은 두개
    (※버튼을 사용할때는 반드시 type값을 작성)
   + sumbit : 무엇인가를 제출하는데 사용
   + button : 그외에는 button값을 사용
   + reset : 입력한 값을 리셋하는 용도

![alt html](https://postfiles.pstatic.net/MjAyMTExMTBfNzQg/MDAxNjM2NTE4OTE2NzIx.wxRSfIkKh1yvX1ENw-hf7UUk2345vkDXinBi3do7gU4g.3Cp2vVuIUqel3KHOphoZxxmymGnND7rRV5be9duuvHkg.JPEG.daykkk/18.JPG?type=w966)
예제) 폼 태그와 인풋 태그를 사용한 회원가입 양식 페이지
