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
