# HTML의 문법
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
- 모든 요소(엘리먼트)는 속성을 가질 수 있으며, 속성은 요소에 추가적인 정보를 제공한다.
    ```html
    <input type="text" name="username" value="홍길동" />
    <img src="sample.png" width="100" height="60" alt="샘플사진"/>
    <a href="home.html">홈</a>
    
    * 속성명과 속성명을 정의할 때는 속성명="속성값" 혹은 속성명='속성값'의 형식으로 작성할 수 있다.
    * 속성명과 속성값 사이에 공백을 추가하지 않는다.
    * 속성값은 반드시 쌍따옴표나 홑따옴표로 감싼다.
    * 속성을 작성하는 정해진 순서는 존재하지 않는다. 보통 중요한 값이 앞에 온다.
    * 요소에 속성을 중복해서 정의할 수 없다.
    ```
    
    - 어떤 속성은 속성값에 사용할 수 있는 값이 미리 정해져 있기도 한다.
      ```html
      <input type="속성값" />
      * input요소의 type 속성의 속성값은 text, password, radio, checkbox, date, file, ... 중에서 하나다.
      ```
      
    - 어떤 속성은 기본값이 지정되어 있다.
      ```html
      <input type="속성값">
       * input요소의 type 속성의 기본값은 text다.
      ```
      
- 글로벌 속성(HTML Global Attibute)
  * 글로벌 속성은 모든 HTML 요소가 공통으로 사용할 수 있는 속성이다.
  * 자주 사용되는 글로벌 속성
    |속성명|설명|
    |---|---|
    |id|        요소에 유일한 식별자를 지정한다.|
    |class|     스타일시트에 정의된 class를 요소에 지정한다. 중복지정이 가능하다.|
    |style|     요소에 스타일을 지정한다.|
    |tabindex|  사용자가 키보드로 페이지를 내비케이션할 때 이동 순서를 지정한다.|
    |title|     요소에 대한 제목(풍선도움말)을 지정한다.|
    
## 3. HTML Basic 태그

```html 
<!doctype> 태그
  문서형식정의 태그다.
  출력할 웹 페이지의 형식을 웹 브라우저에게 전달한다.
  <!doctype html>
      html5 문서형식이다.
  <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
      html4 문서형식이다.
  <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
      xhtml 문서형식이다.
   ```

```html
<html> 태그
  모든 html 태그의 부모태그다.
  웹 페이지에 단 하나만 존재한다.
  모든 태그는 html 태그 내부에 기술한다.
  주요 속성
    <html lang="ko"> 
      한국어를 사용하는 경우 ko로 설정한다.
```

```html 
<head> 태그
   메타 데이터의 요소를 포함하는 태그다.
   title, style, link, script에 대한 데이터를 포함한다.
   화면에 표시되지 않는다.
 ```

```html
 <meta> 태그
    브라우저, 검색엔진에서 참조하는 메타데이터를 정의한다.
 <meta charset="utf-8">
    브라우저가 사용하는 문자세트를 지정한다.
 <meta name="keywords" content="강의, 웹강의, 웹개발강의">
    검색엔진을 위한 키워드를 정의한다.
 <meta http-equiv="refresh" content="30">
    웹페이지를 30초마다 refresh한다.
 <meta name="viewport" content="width=device-width, initial-scale=1">
    뷰표트의 너비를 장치의 너비의 지정한다.
    모든 장치에서 올바른 렌더링 및 터치 확대 조절을 할 수 있다.
```
## 4. HTML Text 태그
  - 제목 (Headings) 태그

















