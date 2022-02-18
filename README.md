# JavaScript-Web-Front-End

## window object
#### window 객체
Javascript 실행시 가장 상위에 존재하는 객체<br>
변수를 선언하거나 함수 선언시 window 객체안에 선언됨<br>
표시된 웹 페이지의 정보에 접근하거나 변경을 할 수 있음<br>
window.location : 현재 브라우저 창의 주소를 나타내는 객체<br>
window.location.href : 브라우저 창에 입력된 주소, 변경 가능<br>
window.navigator : 브라우저 자체에 대한 정보<br>
window.screen : 디스플레이의 사이즈<br>
window.document : 웹 페이지 문서의 HTML, CSS 등에 대한 접근 가능<br>


## DOM 소개 및 탐색
#### DOM, Document Object Model
컴퓨터가 문서를 잘 처리할 수 있도록 문서의 구조를 약속한 것<br>
Tree 형태를 따름 : 족보나 가계도와 비슷함<br>

#### document object
javascript에서 document로 접근 가능<br>
children에는 문서의 최상위 엘리먼트인 html이 존재<br>
#### Element API
자식, 부모 엘리먼트에 접근하는 방법<br>
.children : 해당 object의 자식 노드에 대한 배열<br>
.parentNode : 부모 노드<br>
.firstElementChild : 첫 자식 엘리먼트<br>
.lastElementChild : 마지막 자식 엘리먼트<br>
#### 같은 레벨의 형제 엘리먼트에 접근하는 방법
.nextElementSibling<br>
.previousElementSibling<br>


## 단일 Element 선택
### Document API
#### DOM API를 활용해 문서에서 엘리먼트를 선택하는 방법
document.getElementBy~ : 단일 엘리먼트를 선택하는 메소드<br>
document.getElementsBy~ : 다중 엘리먼트를 선택하는 메소드<br>
document.getElementById 메소드<br>
인자로 HTML element 태그의 id를 전달하면 해당 엘리먼트가 반환됨<br>

### Element API
#### .innerHTML 속성
엘리먼트 안의 HTML코드를 변경<br>

#### .innerText 속성
엘리먼트 안의 텍스트를 변경<br>

#### .style 속성
css를 변경 가능<br>

#### getAttribute 메소드
element의 속성의 값을 얻어옴<br>
하나의 인자 : attribute 이름을 받음<br>
직접 객체에 동기화되지 않는 속성에 대해서도 접근이 가능<br>

#### setAttribute 메소드
element의 속성의 값을 설정함<br>
두개의 인자 : attribute 이름, 설정할 속성의 값을 받음<br>
직접 객체에 동기화되지 않는 속성에 대해서도 값 설정이 가능<br>'


## 다중 Element 선택
### Document API
document.getElementsBy~ : 다중 엘리먼트를 선택하는 메소드. 배열형태로 값을 반환함<br>

#### document.getElementsByTagName 메소드
인자로 HTML element 태그의 이름을 전달하면 해당 엘리먼트들이 반환됨<br>
#### document.getElementsClassName 메소드
인자로 class의 이름을 전달하면, 해당 class의 모든 엘리먼트가 배열로 반환됨<br>
#### document.getElementsByName 메소드
인자로 name을 전달하면, 해당 name 속성을 가진 모든 엘리먼트가 배열로 반환됨.<br>

### Element API
#### .value 속성
input element에 입력된 값은 .value를 통해 얻어올 수 있음
getAttribute 메소드로는 받아올 수 없다는 점 주의


## CSS Selector를 이용한 Element 선택
### Document API
document.querySelector : css selector를 기반으로 엘리먼트를 선택<br>
조건에 부합하는 element가 여러개인 경우 첫 엘리먼트만 반환.<br>
document.querySelectorAll : css selector를 기반으로 만족하는 모든 엘리먼트를 선택<br>

### CSS Selector
\# : id,name 기반으로 선택<br>
. : class 기반으로 선택<br>
, : 여러개의 셀렉터를 사용<br>


## Element 추가/삭제
### Document API
document.createElement() : 문자열 인자로 element tag를 입력하면 해당 엘리먼트가 생성돼 반환됨<br>

### Element API
.appendChild(인자) : 추가할 element를 인자로 받아 호출된 element의 자식으로 인자를 추가함<br>
.removeChild(인자) : 삭제할 element를 인자로 받아 호출된 element의 자식중에서 해당 element를 삭제<br>
.insertBefore(인자1, 인자2) : 인자1로 받은 element를 호출된 element의 자식중 인자2의 이전에 추가함<br>
.cloneNode() : 호출된 element를 복사해서 반환함<br>


## Callback function
### Callback Function
조건을 등록해 두고 그 조건을 만족한 경우, 나중에 호출되는 함수<br>
시간을 기반으로 콜백함수를 호출하는 명령<br>

#### setTimeout( function, time )
time 시간이 지난 경우 function 함수를 콜백하는 함수<br>
time 은 millisecond (1/1000초) 단위<br>
timerId를 반환함<br>

#### clearTimeout( timerId )
setTimeout 함수 호출의 결과로 반환된 timerId를 인자로 받아 예약되어 있던 function호출을 취소<br>
이미 function이 호출된 경우(시간이 지나 이벤트가 발생한 경우)에는 효과 없음<br>

#### setInterval( function, time )
time 시간이 경과할 때마다 function 함수를 콜백하는 함수<br>
timerId를 반환함<br>

#### clearInterval( intervalId )
setInterval 함수 호출의 결과로 반환된 intervalId를 인자로 받아 주기적으로 호출되던 function 호출을 취소<br>


## JSON
### JSON : Javascript Object Notification
자바스크립트의 객체를 문자열로 표현하는 방법
프로그램간에 전달하기 편리 (서버 -> 브라우저)<br>
### JSON API
#### JSON.stringify( object )
인자로 받은 객체를 JSON 문자열로 반환함<br>
#### JSON.parse( sring )
인자로 받은 문자열을 Javascript Object로 변경해 반환함<br>
var original_obj = { pi:3.14, str:"string" };<br>

var json_str = JSON.stringify( original_obj );<br>
// 반환 문자열 : {"pi":3.14,"str":"string"}<br>

var parsed_obj = JSON.parse( json_str );<br>

console.log( original_obj ); // {pi: 3.14, str: "string"}<br>
console.log( parsed_obj ); // {pi: 3.14, str: "string"}<br>

undefined, function 은 변환되지 않음에 주의!<br>


