## 8. 폼과 폼 요소

- 폼 태그
  * 사용자가 입력한 데이터를 수집하고, 서버 전송하기 위해서 사용되는 태그다.
  * ```<form>``` 태그가 있다.
  * ```<form>``` 태그는 다양한 입력 양식 태그를 포함할 수 있다.
    + 입력양식 태그 : input, textarea, select, checkbox, radio, button
  * 주요 속성
    + method
      - 사용자가 입력한 데이터를 서버로 전송하는 방식을 지정한다.
        ```html
        <form method="GET">
        <!-- 폼이 수집한 입력데이터가 요청 메세지의 헤더부의 요청 URL 뒤에 포함되어 서버로 전송된다. -->
        ```

        ```html
        <form method="POST">
        <!-- 폼이 수집한 입력데이터가 요청 메세지의 바디부에 포함되어 서버로 전송된다 -->
        ```
 
    + action
      - 폼이 수집한 입력값이 전송될 서버의 URL을 지정한다.
      - 필수 속성값이다.
        ```html
        <form method="GET" action="login.jsp">
        ```
	
    + enctype
      - 폼이 수집한 입력값의 인코딩방식을 지정한다.
      - 지정하지 않으면 ```enctype="application/x-www-form-urlencoded"```이 기본값이다.
        ```html
        <form enctype="application/x-www-form-urlencoded">
        <!-- 
        폼이 수집한 값이 name=value&name=value&name=value의 형식으로 변환되어 서버로 전송된다. 
        첨부파일을 전송할 수 없다.
        -->
        ```
        ```html
        <form method="POST" enctype="multipart/form-data">
        <!-- 
        폼이 수집한 입력값과 첨부파일을 서버로 전송할 때 사용하는 인코딩 방식이다. 
        첨부파일 업로드가 없는 경우에는 지정하지 않는다.
        -->
        ```

- ```<input>``` 태그
  + 사용자로부터 데이터를 입력받기 위해서 사용된다.
  + ```<input>``` 태그가 있다.
  + ```<input>``` 태그의 type 속성값에 따라서 다양한 종류의 입력필드를 정의할 수 있다.
  + 주요 속성
    * type
      + 입력필드의 타입을 지정한다.
      + type속성을 지정하지 않으면 기본값은 ```type="text"```다.
        |속성 값|설명|
        |--|--|
        |```<input type="text" />```|텍스트 입력필드|
        |```<input type="password" />```|비밀번호 입력필드|
        |```<input type="checkbox" />```|복수개 체크가 가능한 체그박스|
        |```<input type="radio" />```|하나만 선택가능한 라디오버튼|
        |```<input type="date" />```|날짜 입력필드|
        |```<input type="datetime" />```|날짜와 시간 입력필드|
        |```<input type="file" />```|첨부파일 등록 필드|
        |```<input type="number" />```|숫자 입력 필드|
        |```<input type="reset" />```|폼 입력값을 초기화하는 버튼|
        |```<input type="submit" />```|폼 입력값을 서버로 전송시키는 버튼|
        |```<input type="hidden" />```|숨김필드|
        |```<input type="email" />```|이메일 입력필드|
        |```<input type="url" />```|url 입력필드|
    * ```value```
      - 입력필드의 값을 지정한다.
      - 체크박스, 라디오버튼은 value 속성으로 값을 미리 지정해야 한다.
      - 첨부파일 필드는 value 속성으로 값을 지정할 수 없다.
        ```html
        <input type="text" name="username" value="홍길동" />

	<input type="radio" name="gender" value="male" /> 남자
        <input type="radio" name="gender" value="female" /> 여자
        ```
    * ```name``
      - 입력필드의 값이 서버로 전송될 때 값의 이름을 지정한다.
      - 입력필드에서 name 속성은 꼭 설정해야되는 속성값이다.
      - 입력필드에 name 속성이 없으면 해당 입력필드의 값이 서버로 전달되지 않는다.
        ```html
        <input type="text" name="userId" />
        * 위의 입력필드에 값을 입력하면, "userId=값"의 형태로 서버로 전달된다.
        ```
    * ```checked```
      - 체크박스와 라디오버튼에서 사용가능한 속성이다.
        ```html
        <input type="checkbox" name="skill" value="java" checked="checked"/> 자바
        <input type="checkbox" name="skill" value="python" /> 파이썬

        <input type="radio" name="gender" value="male" /> 남자
        <input type="radio" name="gender" value="female" checked="checked"/> 여자
        ```
    * ```placeholder```
      - 입력값에 대한 힌트를 지정한다.
    * ```minlegth, maxlength```
      - 입력필드에 입력가능한 최소 문자길이, 최대 문자길이를 지정한다.
    * ```min, max, step``` 
      - 입력필드가 type="number"인 경우, 최소값, 최대값, 한번에 증가감소되는 값을 각각 지정한다.
        ```html
        <input type="number" name="amount" min="0" max="1000" step="10" />
        ```

- select 태그
  * 콤보박스 생성하는 태그다.
  * 복수개의 아이템 중에서 하나 혹은 여러개를 선택할 수 있다.
  * ```<select>``` 태그는 여러 개의 옵션 태그를 포함한다.
  * ```<option>``` 태그는 콤보박스의 아이템을 정의한다.
  * ```<optgroup>``` 태그는 옵션들을 그룹화 한다.

  ```html
  <select name="city">
  	<option value=""> -- 선택하세요 --</option>
	<option value="seoul">서울</>
	<option value="pusan">부산</>
	<option value="daegu">대구</><option value="incheon">인천</>
			<option value="tadjeon">대전</>
			<option value="Gwangju">광주</>
			<option value="ulsan">울산</>
			<option value="sejong">세종특별시</>
		</select>
  ```





























