## 8. 폼과 폼 요소

- ```<form>``` 태그
  * 사용자가 입력한 데이터를 수집하고, 서버 전송하기 위해서 사용되는 태그다.
  * form 태그가 있다.
  * form 태그는 다양한 입력 양식 태그를 포함할 수 있다.
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
      
        ```<form enctype="application/x-www-form-urlencoded">```
	  * 폼이 수집한 값이 name=value&name=value&name=value의 형식으로 변환되어 서버로 전송된다.
	  * 첨부파일을 전송할 수 없다.
	
        ```<form method="POST" enctype="multipart/form-data">```
          * 폼이 수집한 입력값과 첨부파일을 서버로 전송할 때 사용하는 인코딩 방식이다.
          * 첨부파일 업로드가 없는 경우에는 지정하지 않는다.

- ```<input>``` 태그
  + 사용자로부터 데이터를 입력받기 위해서 사용된다.
  + input 태그가 있다.
  + input 태그의 type 속성값에 따라서 다양한 종류의 입력필드를 정의할 수 있다.
  + 주요 속성
    * type
      + 입력필드의 타입을 지정한다.
      + type속성을 지정하지 않으면 기본값은 ```type="text"```다.
        |속성 값|설명|
	|--|--|
	|<input type="text" />|텍스트 입력필드|
	|<input type="password" />|비밀번호 입력필드|
	|<input type="checkbox" />|복수개 체크가 가능한 체그박스|
	|<input type="radio" />|하나만 선택가능한 라디오버튼|
	|<input type="date" />|날짜 입력필드|
	|<input type="datetime" />|날짜와 시간 입력필드|
	|<input type="file" />|첨부파일 등록 필드|
	|<input type="number" />|숫자 입력 필드|
	|<input type="reset" />|폼 입력값을 초기화하는 버튼|
	|<input type="submit" />|폼 입력값을 서버로 전송시키는 버튼|
	|<input type="hidden" />|숨김필드|
	|<input type="email" />|이메일 입력필드|
	|<input type="url" />|url 입력필드|
