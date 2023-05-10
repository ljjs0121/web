# HTML
HTML (HyperText Markup Language)은 웹페이지를 기술하기 위한 마크업 언어이다.

### HTML문서는 반드시 ```<!DOCTYPE html>```로 시작한다.
- HTML 4버전을 사용할 때는 아래처럼 ```<!DOCTYPE html>``` 안에 버전 설정을 해줘야한다.
- ```<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">```
- ```<!DOCTYPE html> ```로 작성하면 **HTML5로 자동 설정**된다.

### ```<html>과</html>```사이에 HTML 문서가 기술된다.
- ```<html>```태그는 HTML문서의 루트 엘리먼트(최상위 태그)다.
- 모든 HTML문서는 ```<html>```태그가 루트 엘리먼트다.
- 모든 HTML문서는 오직 하나의 루트 엘리먼트만 가진다. 
- ```<head>, <body>```를 자식태그로 포함한다.

### ```<head>```와 ```</head>```사이에는 html문서의 제목, 외부파일에 대한 참조, 메타데이터 설정이 위치한다.
- ```<head>```와 ```</head>```에 설정된 내용은 브라우저에 표시되지 않는다.
- ```<mata>, <title>, <script>, <link>``` 등의 태그를 자식태그로 포함한다.

### ```<body>```와 ```</body>```사이에는 웹브라우저에 출련되는 요소가 위치한다.
- 제목, 내용, 목록, 표 그림, 링크 등의 실제 문서내용이 위치한다.

## HTML의 문법
### 1. 요소(Element)
- HTML 요소는 시작태그와 종료태그 그리고 태그 사이의 content로 구성된다.
  ```html
  <p>안녕하세요</p>
  <p> : 시작태그
  </p> : 종료태그
  안녕하세요 : 컨텐츠
  ```
- 태그명은 소문자로 작성한다.
- 태그에서 ```<p>```의 <p 와 ```</p>```의 </p 는 공백없이 적는다.  
- 요소는 중첩될 수 있다.
  * 요소는 다른 요소를 포함할 수 있다.
  * 요소가 다른 요소를 포함하면 부모-자식 관계가 성립된다.  
  * 다른 요소에 포함된 요소는 가독성을 위해서 들여쓰기 한다.
    ```html
      <body>
        <h1>연습</h1>
        <p>html 태그 연습입니다.</p>
      </body>
    
    * body는 h1과 p의 부모요소다.
    * h1과 p는 형제 요소다.
    ```
- 컨텐츠를 포함하지 못하는 요소가 있다.
  * meta,link, img, input, br, hr는 컨텐츠를 포함하지 못하는 요소다.
  * ```<meta></meta>, <input></input>```와 같이 작성하지 않는다. 
  * 일반적인 작성법
    + 컨텐츠 없이 시작 요소만 작성해도 된다.
    ```html
    <meta>
    <input>
    ```
    + Self-Closing 요소의 형태로 작성해도 된다. 
    ```html
    <input />
    <br />
    ```

### 2. 속성(Attribute)
- 속성의 요소(엘리먼트)의 성질, 특징을 정의하는 명세다.
  ```html
    <img src="sample.png" width="100" height="60" alt="샘플사진"/>
    * 속성은 시작 태그에 위치한다.
    * 속성은 속성명과 속성값으로 구성된다.
      속성명   속성값
      src      sample.png
      width    100
      height   60
      alt   
    * 속성명과 속성명을 정의할 때는 속성명="속성값" 혹은 속성명='속성값'의 형식으로 작성할 수 있다.
    * 속성명과 속성값 사이에 공백을 추가하지 않는다.
    * 속성값은 반드시 쌍따옴표는 홑따옴표로 감싼다.
    * 속성을 작성하는 정해진 순서는 존재하지 않는다.
    * 요소에 속성을 중복해서 정의할 수 없다.
    * 어떤 속성은 속성값에 사용할 수 있는 값이 미리 정해져 있기도 한다.
      <input type="속성값" />
      * input요소의 type 속성의 속성값은 text, password, radio, checkbox, date, file, ... 중에서 하나다.
    * 어떤 속성은 기본값이 지정되어 있다.
      <input type="속성값">
      * input요소의 type 속성의 기본값은 text다.
  ```
- 모든 요소(엘리먼트)는 속성을 가질 수 있으며, 속성은 요소에 추가적인 정보를 제공한다.
   ```html
   <input type="text" name="username" value="홍길동" />
   <img src="sample.png" width="100" height="60" alt="샘플사진"/>
   <a href="home.html">홈</a>
  ```


