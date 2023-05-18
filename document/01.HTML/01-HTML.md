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
