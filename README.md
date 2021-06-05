# 강태훈 [201840104]
## [06월 01일]
#### 사용할 수 없는 코드
>let,const,템플릿 문자열,화살표 함수,for of반복문 은 ECMAScript6에서 추가된 기능으로 구 버전의 웹 브라우저에서는 사용할 수 없다<br>
var와 function(),for in 반복문을 사용하여 표현할수 있다.<br>

#### 브라우저 객체 모델
>웹 브라우저와 관련된 객체를 브라우저 객체 모델(BOM,Browser Objext Model)이라고 한다.<br>

#### window 객체
>window 객체는 웹 페이지 자체를 나타냄<br>
>>arlert(메세지)    경고장을 출력<br>
>>prompt(메시지)    프롬프트 출력<br>

#### secreen 객체
>웹 브라우저 화면이 아니라 운영체제 화면의 속성을 가지므로 웹 브라우저마다속성이 다르다.<br>
모든 웹 브라우저에서 공통으로 쓸 수있는 속성을 아래와 같다.<br>
>>width         화면의 너비<br>
>>height        화면의 높이<br>
>>availWidth    실제 화면에서 사용가능한 너비<br>
>>availHeight   실제 화면엘서 사용가능한 높이<br>
>>colorDepth    사용 가능한 색상 수<br>
>>pixelDepth    한 픽셀당 비트 수<br>

#### location 객체와 history 객체
>location 객체는 웹 브라우저의 주소창과 관련됨<br>
location 객체는 프로토콜의 종류,호스트이름,문서 위치 등 정보가 있음.<br>
모든 웹 브라우저에서 공통으로 쓸 수있는 속성을 아래와 같다.<br>
>>href      문서의 URL 주소 <br>
>>host      호스트 이름과 포트 번호      localhost:52273<br>      
>>hostname  호스트 이름                 localhost<br>
>>port      포트 번호                   52273<br>
>>pathname  디렉터리 경로               /folder/HTMLpage.html<br>
>>hash      앵커 이름(#~)               #test<br>
>>search    요청 매개변수               ?param=10<br>
>>protocol  프로토콜 종류               http:<br>

>메소드는 아래와 같다<br>
>>assign(링크)  매개변수로 전달한 위치로 이동함<br>
>>reload()      새로고침<br>
>>replace()     매개 변수로 전달한 위치로 이동합니다(뒤로가기 불가능)<br>

#### navigator 객체
>navigator 객체에는 웹 페이지를 실행하는 웹 브라우저 정보가 들어 있음<br>
>>appCodeName       웹 브라우저의 코드 이름<br>
>>appName           웹 브라우저의 이름<br>
>>appVersion        웹 브라우저의 버전<br>
>>platform          사용중인 운영체제의 시스템 환경<br>
>>userAgent         웹 브라우저의 전체적인 정보<br>

#### 문서 객체 모델 관련 용어
>웹 브라우저에서 HTML파일을 끌어다 놓으면 웹 브라우저는 HTML파일을 분석해 화면에 출력함<br>
이때 웹 브라우저가 HTML파일을 분석하고 출력하는 방식을 문서 객체 모델이라고 함<br>

#### 웹 페이지 생성 순서
>처음 HTML 페이지를 실행하면 Process - 0 문자열을 출력함 -><br>
이어서 웹 브라우저가 코드를 읽으며 h1 태그 내부에 있는 Process - 1 문자열을 출력함.<br>
곧바로 아래의 script 태그를 실행하므로 Process - 2 문자열을 출력함 -><br>
경고창을 닫으면 다시 HTML 페이지를 읽으며 h2 태그 내부에 있는 Process - 2 문자열을 출력함<br>
아래의 태그를 읽으며 Process - 3 문자열을 출력<br>

#### 문서 객체 선택
>이미 있는 HTML 태그를 js에서 문서 객체로 변환하는 것을 문서 객체 선택이라고 함<br>
문서 객체를 선택하면 js로 실행중에 내부 글자를 변경하거나 스타일을 변경할 수 있다<br>
###### 1개의 문서 객체 선택
>>document.getElementByle(아이디)       아이디를 사용해 문서 객체를 선택함<br>
>>document.querySelector(선택자)        선택자를 사용해 문서 객체를 선택함<br>
###### 여러개의 문서 객체 선택
>>document.getElementsByName(이름)      name 속성으로 여러개의 문서 객체를 선택함<br>
>>document.getElementsByClassName(클래스)   class 속성으로 여러개의 문서 객체를 선택함<br>
>>document.querySelector(선택자)        선택자로 여러개의 문서 객체를 선택함<br>

#### 문서 객체 조작
>문서 객체는 문자,속성,스타일을 조작할수 있음<br>
문서 객체 내부의 문자를 조작할 때는 innerHTML 속성을 사용함<br>
>>innerHTML  문서 객체 내부의 글자를 나타냄<br>
###### 스타일 조작
- 스타일 시트의 스타일 속성      js의 스타일 속성<br>
>>background-color      backgroundColor<br>
border-radius           borderRadius<br>
border-bottom           borderBottom<br>
###### 속성 조작
>>setAttribute(속성 이름,속성 값)    속성을 지정함<br>
getAttribute(속성 이름)              속성을 추출함<br>

#### 이벤트
>자바는 기본적으로 다음이벤트를 지원함<br>
>- 마우스 이벤트<br>
>- 키보드 이벤트<br>
>- HTML 프레임 이벤트<br>
>- HTML 입력 양식 이벤트<br>
>- 사용자 인터페이스 이벤트<br>
>- 구조 변화 이벤트<br>
>- 터치 이벤트<br>

#### jQuery 객체
>jQuery 라이브러리는 $함수를 활용함<br>
>>$(<매개변수>)메소드(<매개변수>,<매개변수>)<br>
>- ex)<br>
window.jQuery - window.$ = jQuery;<br>

#### 문서 객체 선택
>>parent()      부모 태그를 선택함<br>
>>find()        후손 태그를 찾음<br>

#### 문서 객체 개별 조작
>$() 함수를 사용하면 여러개의 문서 객체를 선택할 수 있음<br>
>>length        선택된 문서 객체의 수를 구함<br>
>>get()         선택한 문서 객체 중 하나를 선택함<br>
>>each()        선택한 문서 객체에 반복을 적용함<br>

#### 문서 객체 조작
>>text()        html 태그 내부의 문서를 조작함<br>
>>html()        html 태그 내부의 문자를 조작함<br>
###### 스타일 조작
>>css()         스타일을 조작함<br>

#### 문서 객체 생성
>>$(<A>.prependTo(<B>))     A를 B안쪽 앞에 추가함<br>
$(<A>.apendTo(<B>))         A를 B안쪽 뒤에 추가함<br>
$(<A>.insertBefore(<B>))    A를 B앞에 추가함<br>
$(<A>.insertAfter(<B>))     A를 B뒤에 추가함<br>

#### 이벤트
>>on()      이벤트를 연결함<br>
>>off()     이벤트를 제거함<br>
###### 이벤트직접연결
>$(<선택자>).on(<이벤트 이름>,<콜백 함수>)<br>
>- 키보드 이벤트<br>
>ketdown()      키보드 키를 눌렀을때<br>
keypress()      키가 입력되었을 때<br>
ketup()         키보드 키를 떼었을 대<br>
>- 마우스 이벤트<br>
click()         마우스를 클릭했을때<br>
dbclick()         마우스를 더블클릭 했을때<br>
mousedown()     마우스 버튼을 눌렀을 때<br>
mouseenter()    마우스 커서가 해당 태그로 들어갔을 때<br>
mouseleave()    마우스 커서가 해당 태그를 나갔을 때<br>
mousemove()     마우스가 움직일 때<br>
mouseup()       마우스 버틀을 땔 때<br>
>- 입력 양식 이벤트<br>
blur()      입력 양식에 값 입력을 종료할 때<br>
change()    입력 양식의 값이 변경될 때<br>
focus()     입력 양식에 값 입력을 시작할 때<br>
select()    type 속성이 select인 입력 양식의 목록에서 값을 선택했을 때<br>
submit()    type 속성이 submit인 입력 양식을 클릭했을 때<br>
>- 웹 브라우저 이벤트<br>
resize()    웹 브라우저 크기를 변경할 때<br>
scroll()    웹 브라우저를 스크롤할 때<br>

#### 애니메이션
>>animate()     애니메이션을 적용함
>>$(<선택자>).animate(<속성>,<시간>,<콜백 함수>)<br>

## [05월 25일]
#### 요청과 응답
>웹 서버가 하는일은 요청과 응답의 연속으로 웹 브라우저에 웹페이지 주소를 입력하면 웹서버는 입력한 주소에 맞는 웹페이지를 제공함<br>
- 스트림<br>
>프로그램이 외부와 통신할 때는 컴퓨터 속에 흐르는 물길로 비유할 수 있는 스트림을 사용<br>
웹에서 데이터가 전송될 때 스트림을 사용<br>

#### express 모듈을 사용한 서버 생성과 실행
>express 모듈을 사용해 서버를 생성할 때는 아래의 메소드를 사용함<br>
>>express()     서버 애플리케이션 객체를 생성<br>
>>app.use()     요청이 왔을 때 실행할 함수를 지정함<br>
>>app.listen()  서버를 실행함<br>
- 포트<br>
>포트는 컴퓨터와 컴퓨터를 연결하는 정보의 출입구 같은 역할을 함<br>
0번부터 65535번까지 포트가 있음<br>

#### 페이지 라우팅
>express 모듈은 페이지 라우팅을 지원함<br>
페이지 라우팅은 클라이언트 요청에 적절한 페이지를 제공하는 기술<br>
express 모듈은 app객체의 다음 메소드를 활용해서 페이지 라우팅함<br>
>>get(path,callback)    GET요청이 발생했을 때 이벤트 리스너를 지정함<br>
>>post(path,callback)   POST요청이 발생했을 때 이벤트 리스너를 지정함<br>
>>put(path,callback)    PUT요청이 발생했을때 이벤트 리스너를 지정함<br>
>>delete(path,callback) DELETE요청이 발생했을 때 이벤트 리스너를 지정함<br>
>>all(path,callback)    모든 요청이 발생했을 때 이벤트 리스너를 지정함<br>
- GET,POST,PUT,DELETE<br>
>웹 요청을 할때에 여러정보를 서버에 전달하는데 이때 메소드 값을 전달함<br>
GET은 값을 확인할때,POST는 값을 전달할때,PUT은 값을 수정할때,DELETE는 값을 제거할때 사용함<br>

#### 요청과 응답
>response.send() 메소드를 사용하면 문자열을 클라이언트에 제공할 수 있다는것을 알수있음<br>
express 모듈에서 사용하는 모든 콜백 함수의 매게 변수에는 request 객체와 response 객체가 들어감<br>
##### response 객체
>>send()    데이터 본문을 제공함<br>
>>status()  상태 코드를 제공함<br>
>>set()     헤더를 설정함<br>
###### 데이터 제공
>send()메소드는 가장 마지막에 실행해야 하며,두 번 실행할수 없음<br>
- send() 메소드의 매개변수
>>문자열    html을 제공함<br>
>>객체,배열 json을 제공함<br>
###### Content-Type
>서버가 클라이언트 웹 브라우저에 데이터를 제공하면, 웹 브라우저는 해당 데이터가 어떤 데이터인지 구분함<br>
서버가 Content-Type을 제공해 주면 웹 브라우저는 헤더를 확인하고, 제공된 데이터의 형태를 확인함<br>
이때 MIME라는 형태로 문자열을 제공 하며 대표적인 MIME형식은 아래와 같다<br>
>>test/plain        기본적인 텍스트를 의미함<br>
>>text/html         html 데이터를 의미함<br>
>>image/png         png데이터를 의미함<br>
>>audio/mpe         MP3음악 파일을 의미함<br>
>>video/mpeg        MPEG 비디오 파일을 의미함<br>
>>application/json  json 데이터를 의미함<br>
>>multipart/form-date   입력 양식 데이터를 의미함<br>

>이러한 MIME형식을 지정할 때는 type()메소드를 사용함<br>
>>type() Content-Type을 MIME 형식으로 지정함<br>
###### HTTP상태코드
>>1xx   처리중      100Continue<br>
>>2xx   성공        200ok<br>
>>3xx   리다이렉트  300 Multiple Choices<br>
>>4xx   클라이언트오류  400 Bad Request<br>
>>5xx   서버 오류   500 Internal Server Error<br>

>상태 코드를 지정할 때는 status() 메소드를 사용함<br>
>>status()  상태 코드를 지정함<br>
###### 리다이렉트
>상태코드 중에는 3xx는 리다이렉트라는 특수한상태 코드로 웹 브라우저가 리다이렉트를 확인하면 화면을 출력하지않고<br>
응답 헤더에 있는 Location 속성을 확인해서 해당 위치로 이동함<br>
>>rediect() 리다이렉트함<br>

##### request 객체
###### 요청매개변수
>요청 매개 변수를 추출할 때는 query 객체를 사용함<br>
요청 매개 변수는 URL뒤에 ? 기호를 삽입하고 <키>=<값> 형태로 &로 구분해서 입력함
>>프로토콜      HTTPs               통신에 사용되는 규칙을 의미함<br>
>>호스트        (search).naver.com  애플리케이션 서버(또는 분산 장치 등)의 위치를 의미함<br>
>>URL           search.naver        애플리케이션 서버 내부에서 라우트 위치를 나타냄<br>
>>요청 매개변수 ?where=nexearch     추가적인 정보를 의미함<br>

#### 미들웨어
>express 모듈은 이것들을 쉽게 활용할 수 있도록 여러가지 기능을 제공하는데 이를 미들웨어라고 함<br>
>>use() 미들웨어를 제공<br>
##### 정적 파일 제공
>웹 페이지를 만들때 굉장히 자주 사용하는 기능으로 '정적파일 제공'이 있고 이는 웹 페이지에서 변경되지 않는 요소를 쉽게 제공해주는 기능<br>
##### morgan 미들웨어
>다른 사람이 만든 미들웨어도 가져와서 사용할 수 있음<br>
로그는 관련된 정보를 가진 글자를 의미하며, 로그 출력 미들웨어는 웹 요청과 관련된 내용을 출력하는 미들웨어<br>
웹 서버를 운용할 때는 여러 보안 위협들과 마주하며 이러한 위협을 검출할수 있는 가장 기본적인 방법<br>
로그 출력을 실시간으로 감시해서 특정한 오류가 여러번 발생하는 상황이 생기면 경보등을 함<br>
##### body-parser 미들웨어
###### 클라이언트에서 서버로 데이터 전송
>클라이언트가 서버로 데이터를 전송하는 방법은 굉장히 많음<br>
URL형태,요청매개변수 사용 등이 있음<br>
서버에서 클라이언트로 데이터를 전송할때는 응답 본문을 사용하는데 요청할때도 요청본문을 사용할 수 있음<br>
이를 활용하면 주소에 기록을 남기지 않고 데이터를 전달할 수 있음<br>
###### 요청 본문
>대표적인 요청본문의 종류는 아래와 같음<br>
>>application/x-www-form-urlencoded     웹 브라우저에서 입력 양식을 POST,PUT,DELETE방식으로 전달할때 사용하는 기본적인 요청방식<br>
>>application/json                      JSON 데이터로 요청하는 방식<br>
>>mulipart/form-data                    대용량 파일을 전송할 때 사용하는 요청 방식<br>

#### RESTful 웹 서비스 개요
>RESTful 웹 서비스는 REST규정에 맞게 만든ROA를 따르는 웹 서비스 디자인 표준<br>
자원을 다루는 방법과 특정 웹 페이지로 접근하는 방법을 비슷한 형태로 구성함<br>
- RESTful 웹 서비스의 구조<br>
>>GET       컬렉션을 조회함             컬렉션의 특정 요소를 조회<br>
>>POST      컬렉션에 새로운 데이터 추가 사용x<br>
>>PUT       컬렉션 전체를 한번에 변경   컬렉션에 특정 요소를 수정<br>
>>DELETE    컬렉션 전체를 삭제          컬렉션의 특정 요소를 삭제<br>
>>          /collection                 //collection/d<br>
- RESTful 웹 서비스<br>
>>GET       /user           모든 사용자 정보를 조회함<br>
>>POSt      /user           사용자를 추가<br>
>>GET       /user/:id       특정 사용자 정보를 조회<br>
>>PUT       /user/:id       특정 사용자 정보를 수정<br>
>>DELETE    /user/:id       특정 사용자 정보를 제거<br>

#### Postman 크롬 애플리케이션 
>RESTful 웹 서비스는 클라이언트 프로그램에서 활용함<br>
POStman 크롬 애플리케이션은 서버만으로 테스트를 할수 있도록 많이 사용하는 테스트 프로그램<br>

## [05월 18일]
#### 전역 변수
>자바스크립트에서 아무런 변수를 선언하지않고 모든 고셍서 사용할 수 있는 것들을 전역 OO라고 함<br>

>>__filename     현재 실행중인 코드와 파일경로를 나타냄<br>
>>__dirname      현재 실행중인 코드의 폴더 경로를 나타냄<br>

```jsx 
ex)
console.log(__filename);
console.log(__dirname);
```

#### process 객체의 속성과 이벤트
>node.js는 process객체라는 전역 객체를 제공함<br>
프로세스 정보를 제공하며, 제어할 수 있게 하는 객체<br>
- 객체의 속성<br>
>>env       컴퓨터 환경 정보를 나타냄<br>
>>version   Node.js 버전을 나타냄<br>
>>versions  Node.js와 종속된 프로그램 버전을 나타냄<br>
>>arch      프로세서의 아키텍처를 나타냄<br>
>>platform  플랫폼을 나타냄<br>
- 객체의 메소드<br>
>>exit([exitCode = 0])  프로그램 종료<br>
>>memoryUsage()         메모리 사용 정보 객체를 리턴<br>
>>uptime()              현재 프로그램이 실행된 시간을 리턴<br>

#### 객체와 이벤트 개요
>JS는 이벤트를 많이 활용함<br>
- Node.js 이벤트 연결 메소드<br>
>>on(<이벤트이름>,<이벤트 핸들러>)    이벤트를 연결함<br>
- process 객체에 있는 이벤트<br>
>> exit                 프로세스가 종료될때 발생함<br>
>> uncaughtException    예외가 일어날때 발생함<br>

#### os모듈
```jsx const os = require('os')```
- os 모듈 메소드 <br>
>>hostname()    운영체제의 호슽르 이름을 리턴<br>
type()          운영체제의 이름을 리턴<br>
flatform()      운영체제의 플랫폼을 리턴<br>
arch()          운영체제의 아키텍처를 리턴<br>
release()       운영체제의 버전을 리턴<br>
uption()        운영체제가 실행된 시간을 리턴<br>
loadavg()       로드 에버리지 정보를 담은 배열을 리턴<br>
totalmem()      시스템의 총 메모리를 리턴<br>
freemem()       시스템의 사용 가능한 메모리를 리턴<br>
cpus()          CPU의 정보를 담은 객체를 리턴<br>
getNetworkInterfaces() 네트워크 인터페이스의 정보를 담은 배열을 리턴<br>

#### url 모듈
```jsx const url = require('url')```
- url 모듈의 메소드
>>parse(urlStr[.parseQeryString = flase.slashesDenoteHost = flase]) URL문자열을 URL객체로 변환해 리턴<br>
format(urlObi)      URL객체를 URL 문자열로 변환해 리턴함<br>
resolve(from,to)    매개변수를 조합하여 완전한 URL 문자열을 생성해 리턴함<br>

#### File System 모듈
```jsx const fs = require('fs')```
###### 파일읽기
>>fs.readFileSync(<파일이름>)       동기적으로 파일을 읽어 들임<br>
fs.readFile(<파일이름>,<콜백함수>)  비동기적으로 파일을 읽어 들임<br>
###### 비동기 처리의 장점
>js는 c++,java보다 느리지만 프로그램을 개발하는 과정에서 Node.js를 사용하면 손쉽게 비동기 처리를 구현할수 있음<br>
기존의 웹 서버보다 10배 이상 빠르고 가볍다 라는 말도 여기서 나온 것<br>
###### 파일쓰기
>>fs.writeFileSync(<파일이름>,<문자열>)     동기적으로 파일을 씀<br>
fs.writeFile(<파일이름>,<콜백함수>)         비동기적으로 파일을 씀<br>
###### 파일처리와 예외 처리
>동기 코드를 예외처리할때는 try catch 구문을 활용하고 , 비동기 코드를 예외 처리할 때는 콜백 함수로 전달된 첫 번째 매개 변수 error를 활용<br>

#### 노드 패키지 매니저
>어떤 프로그래밍 플랫폼이 기본적으로 제공하는 모듈을 '내부 모듈'이라고 함<br>
반면 개인 개발자가 내부 모듈을 조합해서 사용하기 쉬운 형태로 만들거나 새로운 기능을 구현해서 제공하는 것을 '외부 모듈'이라고 함<br>
Node.js는 npm(Node.js Package Manager)을 사용하는데 Node.js가 설치될때 함께 설치됨<br>
```jsx npm install <모듈이름>@<버전> ```

#### request 모듈
>웹 요청을 쉽게 만들어 주는 모듈<br>
다음 명령어로 설치함<br>
```jsx npm install request```
설치한 외부 모듈은 내부 모듈처럼 require()함수로 사용함<br>
```jsx const request = require('request')```
request 모듈 설명은 GitHub 페이지에서 확인가능<br>

#### cheerio 모듈
>가져온 웹 페이지의 특정 위치에서 손쉽게 데이터 추출 가능<br>
다음 명령어로 설치함<br>
```jsx npm install cheerio```
설치한 외부 모듈은 내부 모듈처럼 require()함수로 사용함<br>
```jsx const cheerio = require('cheerio') ```
cheerio 모듈 설명은 GitHub 페이지에서 확인가능<br>

#### async 모듈
>Node.js는 대부분의 메소드가 비동기적으로 구성되므로 실행순서를 정의하기가 어렵고 들여쓰기도 많음<br>
이 문제를 어느정도 해결해 줄수 있는 모듈<br>
다음 명령어로 설치함<br>
```jsx npm install async ```
다음 방법으로 추출함<br>
```jsx const async = require('async')```

## [05월 11일]
#### DATA 객체
>new Date()             현재 시간으로 Date 객체를 생성<br>
new Date(유닉스 타임)    1970/01/01 00시00분00초 부터 경과한 밀리초 로 Date 객체 생성<br>
new Date(<시간 문자열>)  문자열로 Date 객체 생성<br>
new Date(<년>,<월-1>,<일>,<시간>,<분>,<초>,<밀리초>) 시간요소를 기반으로 Date 객체를 생성<br>
Date 객체는 get oo () 형태의 메소드와 set oo ()형태의 메소드만 가짐.<br>
이때 oo에 들어가는 문자는 FullYear,Month,Day,Hours,Minutes,Seconds 등 이있다.<br>

#### Array 객체
>Array 객체는 js에서 여러 자료를 다룰 때 사용하는 자료형이다.<br>

###### 기본 메소드
>concat()    매개변수로 입력한 배열의 요소를 모두 합쳐 배열을 만들어 리턴함<br>
join()      배열 안의 모든 요소를 문자열로 만들어 리턴함<br>
pop()*      배열의 마지막 요소를 제거하고 리턴함<br>
push()*     배열의 마지막 부분에 새료운 요소를 추가함<br>
reverse()*  배열의 요소 순서를 뒤집음<br>
slice()     배열요소의 지정한 부분을 리턴함<br>
sort()*     배열의 요소를 정렬함<br>
splice()*   배열 요소의 지정한 부분을 삭제하고 삭제한 요소를 리턴함<br>

#### ECMASCRIPT5에서 추가된 메소드
>forEach()   배열의 요소를 하나씩 뽑아 반복을 돌림<br>
map()       콜백 함수에서 리턴하는 것을 기반으로 새로운 배열을 만듬<br>
filter()    콜백 함수에서 true를 리턴하는 것으로만 새로운 배열을 만들어 리턴함<br>

#### 프로토 타입에 메소드 추가
>프로토타입에 메소드를 추가하면 해당 자료형 전체에 추가할 수 있음. 예를들어 String 생성자 함수의 prototype 속성에 contain()메소드 추가<br>

###### JSON객체
>JavaScript Object Notation 의 약어로 'js객체를 사용한 데이터 표현방법'<br>
2010년 이후로 가장많이 사용하는 데이터 표현방법<br>
-문자열은 큰따옴표로 만들어야함<br>
-모든 키는 큰따옴표로 감싸야함<br>
-숫자,문자열,불 자료형만 사용가능<br>

###### JSON객체의 메소드
>JSON.stringfy(<객체>,<변환 함수>,<공백 개수>)  자바스크립트 객체를 문자로 만듬<br>
JSON.parse(<문자열>)                           문자열을 자바스크립트 객체로 파싱함<br>

#### 예외처리
>프로그램을 실행하는 동안 문제가 발생하면 프로그램이 자동으로 중단됨.<br>
이렇게 발생한 오류를 예외(Exception)이라고 하며, 이러한 오류에 대처할수 있게해주는것이 예외처리<br>

###### 고급예외처리
>try 키워드,catch 키워드,finally 키워드로 예외를 처리하는 방법<br>
이를 try catch finally구문이라고도 함<br>
ex)<br>
try{<br>
    //예외 발생하면<br>
}catch (exception){<br>
//여기서 처리<br>
}finally{<br>
//여기는 무조건 실행<br>
}<br>

#### 예외 객체
>예외가 발생하면 어떤 예외가 발생했는지 정보를 함께 전달받을수 있게 해주는 것<br>
위의 예제에서 catch괄호 안에 들어있는 변수를 나타냄<br>

#### 예외 강제 발생
>예외를 강제로 발생시킬때는 throw 키워드 사용<br>
throw 키워드 뒤에는 문자열 또는 Error 객체를 입력<br>
-throw '강제 예외';<br>
자세하게 예외를 출력하고싶을때는 Error 객체 사용<br>
ex)<br>
const error = new Error('메시지')<br>
error.name = '내 마음대로 오류'<br>
error.message = '오류의 메시지'<br>
//예외발생<br>
throw error;<br>

-문자열을 사용할 때는 catch구문의 예외 객체에 간단한 문자열만 전달됨<br>
-반면 Error 객체를 사용하면 예외객체로 지금까지 살펴봤던 예외 객체 전달됨<br>

## [05월 04일]
#### 생성자 함수
>객체를 만드는 함수<br>
ex)<br>
function Product(name,price){<br>
this.name = name;<br>
this.price = price;<br>
}<br>

#### 프로토타입
>생성자 함수로 만든 객체에는 프로토 타입이라는 공간에<br> 
메소드를 지정해서 모든 객체가 공유 하도록 만들수 있음<br>
프로토타입은 모든 함수가 가지고 있는 속성으로 해당 함수를 생성자 함수로 사용했을 때만 의미가있음<br>
ex)<br>
funtion Product(name,price){<br>
    this.name=name<br>
    this.price=price<br>
}<br>
Product.prototype.print = function(){<br>
    console.log('${this.name}의 가격은 ${this.price}원입니다.')<br>
} <br>
let products = {<br>
    new Product("바나나",1200)<br>
    new Product("사과",2000)<br>
    new Product("배",3000)<br>
    new Product("고구마",700)<br>
    new Product("감자",600)<br>
    new Product("수박",500)<br>
    }<br>
for (let product of products){<br>
    product.print()<br>
}<br>

#### 기본 자료형과 객체 자료형의 차이
>js에서는 문자열,숫자,불을 기본자료형이라고 함<br>
기본 자료형의 속성 또는 메소드를 사용할 때 기본 자료형이 자동으로 객체로 변환됨<br>
기본 자료형은 객체가아니므로 속성과 메소드를 추가할 수 없음<br>
method() 라는 이름의 메소드를 추가하면 사용가능<br>

#### Number객체
>js에서 숫자를 표현할 때 사용<br>
메소드 와 생성자 함수의 속성으로 생성할수 있음<br>
-생성자 함수의 속성<br>
MAX_VALUE   JS에서 나타낼수 있는 최대 숫자<br> 
MIN_VALUE   JS에서 나타낼수 있는 최소 숫자<br>
NaN         JS에서 나타낼수 없는 숫자<br>
POSITIVE_INFINITY   양의 무한대 숫자<br>
NEGATIVE_INFINITY   음의 무한대 숫자<br>

#### String 객체
>String 객체는 length 속성을 가짐<br>
자기자신을 변화시키는 메소드를 '파괴적 메소드'라고하며<br>
자기자신을 변화시키지 않고 리턴하는 메소드를 '비파괴적 메소드'라고함<br>
-String 객체의 메소드<br>
charAt(position)        position에 위치하는 문자를 리턴<br>
chatCodeAt(position)    position에 위치하는 문자의 유니코드 번호를 리턴<br>
concat(args)            매개변수로 입력한 문자열을 이어 리턴<br>
indexOf(searchString,position) 앞에서부터 일치하는 문자열의 위치를 리턴<br>
lastIndexOf(searchString,position) 뒤에서부터 일치하는 문자열의 위치를 리턴<br>
match(regExp)           문자열 안에 regExp가 있는지 확인<br>
replace(regExp, replacement) regExp를 replacement로 바꾼 후 리턴<br>
search(regExp)          regExp와 일치하는 문자열의 위치를 리턴<br>
slice(start,end)        특정 위치의 문자열을 추출해 리턴<br>
split(separator,limit)  separator로 문자열을 잘라 배열을 리턴<br>
substr(start,count)     start부터 count만큼 문자열을 잘라서 리턴<br>
substring(start,end)    start부터 end까지 문자열을 잘라서 리턴<br>
toLowerCase()           문자열을 소문자로 바꾸어 리턴<br>
toUpperCase()           문자열을 대문자로 바꾸어 리턴<br>


## [04월 27일]
#### 객체
>여러개의 자료형을 한번에 저장하는 자료형<br>
배열과 객체는 상당히 유사하지만 차이점으로는 배열은 요소에 접근할때 인덱스를 사용<br>
객체는 키를 사용<br>

#### 객체와 반복문
>생성한 객체에 for in 반복문으로 반복을 적용할수 있음<br>
for of 반복문도 적용할 수 있지만 일반적인 개발에서는 거의 사용하지 않으므로 생략<br>
ex)<br>
let obj={ name:'바나나',price:1200}<br>
for (let key in obj){<br>
    console.log('${key}:${obj[key]}');<br>
}<br>
name:바나나<br>
price:1200<br>

#### 속성과 메소드
>요소 : 배열 내부에 있는값<br>
속성 : 객체 내부에 있는 값<br>
메소드 : 객체의 속성중 자료형이 함수인 속성<br>
자신이 가지고 있는 속성이라는것을 표시할때 this 키워드 사용<br>
ex)<br>
let=obj{<br> //객체 선언
    name:'바나나',<br>
    price:1200, <br>
    print:function(){<br>
        console.log('${this.name}의 가격은 ${this.price}원입니다)<br>
    }<br>
}<br>
obj.print();<br> //메소드 호출

## [04월 13일]
#### 익명 함수
>leg <함수이름> =function(){ };<br>
함수가 코드의 집합이라는 의미는 중괄호 내부에 코드를 넣으라는 것<br>

#### 선언적 함수
>function<함수 이름>() { }<br>

#### 화살표 함수
>() => { }<br>
하나의 표현식을 리턴하는 함수<br>

#### 함수의 기본형태
>function <함수이름> (<매개 변수>){<br>
    <함수코드> <br>
    return<리턴 값> <br>
}<br>
매개변수를 넣으면 메소드 내부에서 특정한 처리를 수행하고 값을 반환하는 것 <br>
아무것도 리턴하지 않아도 가능<br>   
--메소드 내부에 일어나는 처리에 비중을 둠<br>

#### 함수 매개 변수 초기화
>js는 매개변수를 입력하지 않아도 함수가 호출됨<br>

#### 콜백함수
>함수를 변수에 저장할수 있어 함수의 매개 변수로 전달할 수 있음.<br>

#### 표준 내장 함수
###### 숫자 변환함수
>parselnt() -문자열을 정수로 변환함<br>
parseFloat() - 문자열을 실수로 변환함<br>

###### 타이머 함수
>setTimeout(함수,시간) - 특정 시간후에 함수를 실행함<br>
setInterval(함수,시간) -특정 시간마다 함수를 실행함<br>
이때 시간은 밀리초로 지정<br>
clearinterval(아이디) - 특정 시간마다 실행하던 함수 호출을 정지함<br>


## [04월 06일]
#### 역 for 반복문
>배열을 뒤에서부터 실행할때 사용<br>
ex)<br>
let array = [1,2,3,4,5,6];<br>
for(let i = array.length -1;i>=0;i--){<br>
    console.log(array[i]);<br>
}<br>

#### for in 반복문과 for of 반복문
>객체에 쉽게 반복문을 적용할 때 사용<br>
사용과 역할이 같음<br>

#### 중첩 반복문
>중첩 조건문처럼 여러번 중첩해서 사용하는 반복문<br>
ex) 별찍기<br>
let star = "";<br>
for(let i =0; i< 10; i++){<br>
    for(let j =0; j< i+1;j++ ){<br>
        star += "*";<br>
    }<br>
    star +="\n";<br>
}<br>
console.log(star);<br>

#### break
>조건문이나 반복문을 벗어날때 사용<br>
무한반복문은 break를 사용해야 벗어날 수 있음<br>

#### continue
>반복문 내부에서 현재 반복을 멈추고 다음 반복을 진행하게 함<br>
ex)<br>
for(let i = 1;i < 10; i++){<br>
    if(i%2 ==0){<br>
        continue;<br>
    }<br>
    console.log(i)<br>
}<br>
---
1<br>
3<br>
5<br>
7<br>
9<br>

#### 스코프
>변수를 사용할 수 있는 범위 를 나타냄<br>
스코프 == 블록 <br>

## [03월 30일]
#### switch
>if문과 비슷하지만 사용방법1개에 변수 값이 여러개 있을때 사용<br>
범위를 표현한다면 if조건문을 사용<br>
ex)<br>
let a = 1;<br>
switch (a % 3){<br>
    case 0:<br>
        console.log("3의배수");<br>
        break;<br>
    case 1:<br>
        console.log("나머지 1");<br>
        break;<br>
    case 2:<br>
        console.log("나머지 2")<br>
}<br>
"나머지 1"<br>

#### 삼항 연산자
>if문과 switch문 이외에 조건을 구분할때 사용할 수 있는 문법<br>
###### 기본형태
><불 표현식>?<참>:<거짓><br>
ex)<br>
//참과 거짓 위치에 불 자료형<br>
console.log(number%2 == 0 ? true:false);<br>
//참과 거짓 위치에 문자열 자료형<br>
console.log(numbere%2 ==0?"짝수":"홀수");<br>

> 삼항 연산자를 사용하면 코드가 복잡해 보이므로 한줄로 표기할때 사용<br>
js는 삼항 연산자를 해당변수가 undefined 인지 확인할때 주로 사용<br>
###### 짧은 초기화 조건문
>A || B에서 A가 참이라면 A로 대치됨<br>
A || B에서 A가 거짓이라면 B로 대치됨<br>
#### 배열
>여러개의 자료를 한꺼번에 다룰수 있는 자료형<br>
대괄호 내부의 각 자료는 쉼표로 구분함<br>
배열안에는 여러 자료형이 섞일 수 있음<br>
배열 안에 들어있는 각 자료를 요소<br>
대괄호 안에 넣는 숫자를 인덱스<br>
#### while 반복문
>if 조건문과 형태가 비슷하지만 if조건문과 달리 <br>
불표현식이 참인동안에는 중괄호 안의 문장을 계속 실행함<br>
조건이 변하지 않으면 무한반복하므로 false로 만들수 있는 문장을 포함해야된다<br>
무한반복하는 while문을 무한루프라고 함<br>
#### for 반복문
>원하는 횟수만큼 반복하고 싶을때 사용함<br>
먼저 초기식을 실행하고 조건식을 확인<br>
조건식이 false이면 반복문을 빠져나가고,true면 문장과 종결식을 차례로 실행해<br>
다시 조건식이 true인지 확인<br>

## [03월 23일]
#### 논리 연산자<br/>

###### ! 	논리부정 연산자<br/>
>ex)<br/>
console.log(!true);		false<br/>
console.log(!false);		true<br/>
console.log(!(123>13))	false<br/>
console.log(!(123<12))	true<br/>

###### ||	논리합 연산자<br/>
>ex)<br/>
true true = true<br/>
true flase = true<br/>
false true = true<br/>
false false = false<br/>

###### &&	논리곱 연산자<br/>
>ex)<br/>
true true = true<br/>
true flase = false<br/>
false true = false<br/>
false false = false<br/>

#### 변수<br/>
>1.변수 선언	선언 = let,const<br/>
2.변수에 값을 할당<br/>
변수에 값을 저장하는것 = 변수에 값을 할당<br/>
변수를 선언한 후 처음 값을 할당 = 변수를 초기화<br/>
보통 선언과 초기화는 한번에 처리<br>
js는 다른 언어와 다르게 변수에 자료형을 지정하지않음<br/>
= int 나 string처럼 값을 따로 주지않아도 됨<br/>
하지만 실수가 잦아 오류(runtime error)가 발생할 확률 높음<br/>
따라서 하나의 변수에는 하나의 자료형을 넣을것<br/>

#### 복합 대입 연산자<br/>
>+= 숫자 덧셈 후 대입 연산자<br/>
-= 숫자 뺄셈 후 대입 연산자<br/>
*= 숫자 곱셈 후 대입 연산자<br/>
/= 숫자 나눗셈 후 대입 연산자<br/>
ex)<br/>
let output = 0;		<br/>
output = output + 52;	output += 52;<br/>
output = output * 3;	output *= 3;<br/>
output = output - 50;	output -= 50;<br/>
output = output / 2;	output /= 2;<br/>
console.log =(output); =53<br/>
문자도 가능<br/>

#### 증감 변산자<br/>
>변수++ 	기존변수 값에 1을 더함 (후위)<br/>
++변수 	기존변수 값에 1을 더함 (전위)<br/>
변수--	기존변수 값에 1을 뺌(후위)<br/>
--변수	기존변수 값에 1을 뺌(전위)<br/>
후위는 실행후 변경<br/>
전위는 실행전 변경<br/>

#### 자료형 검사<br/>
>typeof 	해당 변수의 자료형을 추출(자료형을 확인할때)<br/>
키워드이면서 연산자<br/>
int		숫자<br/>
string		문자열<br/>
boolean		참/불<br/>
function		함수<br/>
object		객체<br/>
underfined	초기화되지 않은 것을 표현하는 자료형<br/>
ex)<br/>
typeof(1)<br/>
'int'<br/>
typeof(true)<br/>
'boolean'<br/>

#### 강제 자료형 변환<br/>
>Number()		숫자형자료형으로 변환<br/>
String()		문자열로 자료형 변환<br/>
Boolean		불로 자료형 변환<br/>

>Number()함수와 NaN<br/>
ex)<br/>
console.log(Number("52"));		52<br/>
console.log(Number(52.123"));	52.123<br/>
console.log(Number(true));		1<br/>
console.log(Number(false));		0<br/>
console.log(Number("안녕하세요"));	NaN<br/>

>NaN(Not a Number) <br/>
숫자 자료형이지만 숫자가 아닌것<br/>
NaN은 무조건적으로 다름<br/>
NaN인지 확인할때는isNaN()함수를 사용<br/>

>Boolean()함수<br/>
0,NaN,""(빈문자열),null,underfined 이외는 모두 true로 치환<br/>

#### 자동자료형 변환<br/>
>숫자와 문자열에 + 연산자를 적용하면 자동으로 숫자가 문자열로 변환<br/>

#### 일치연산자<br/>
>===	자료형과 값이 같은지 비교함(int와 string이면 false)<br/>
!==	자료형과 값이 다른지 비교함<br/>

#### 상수<br/>
> let     변수를 바꿀수 있음<br/>
const	   변수 못바꿈<br/>
일단 상수(const)를 사용하고 오류가 발생하면 변수(let)로 교체<br/>

#### if조건문<br/>
>표현식이 true면 문장을 실행하고 false면 문장 무시<br/>
조건문을 만족해 실행되는 문장이 한 행이면 중괄호 생략가능<br/>
여러행이라면 중괄호로 감싸야함<br/>

###### if else 조건문<br/>
>두가지로 분명하게 나뉘는 상황에서 편리하게 사용할 수 있다<br/>

###### 중첩 조건문<br/>
>조건문 안에 조건문을 중첩해 사용하는것<br/>
여러번 중첩 가능<br/>

###### if else if 조건문<br/>
>중첩 조건문의 중관호를 생략했을 때 만든 조건문<br/>
중복되지 않는 세가지 이상의 조건을 구분할때 사용

## [03월 16일]
> 오늘 배운 내용 요약<br/>
 js2021-4 폴더 생성 -폴더 선택 -.git이 보이지 않으면 파일 보기에 숨긴 항목 체크 <br/>
README.md 생성(대문자)<br/> #이름[학번]<br/>##[날짜]<br/>>오늘 배운 내용 요약 <br/>>요약<br/>
최근 날짜를 위로 적는다(많아지면 전날배운내용까지 갈때 길어지기 떄문)<br/>
hello.js 생성 console.log('Hello world..!');<br/>
hello.html 생성<br/>
alert('Hello World..!'); - 알림(경고창)<br/>


>*출력 console.log('Hello World!');<br/>
*주석처리 \주석\ -한줄 주석    /*주석*/-여러줄 주석<br/>
*출력 console("문자역") -REPL을 사용한 출력<br/>
*계산   +   -   *   /   %<br/>
*문자열 \n -줄바꿈 \t-수평탭 \\'-작은따옴표 <br/>\\"-큰따옴표 \\\\-역슬래쉬<br/>

ex)<br/>
console.log("안녕하세요[0]); - 안<br/>
console.log("안녕하세요[1]); - 녕<br/>
console.log("안녕하세요[3]); - 세<br/>

>   식별자 함수 항상 대문자 시작<br/>
    실습환경 구축 <br/>
    1.Atome 에디터 <br/>
    2.Node.js -반드시 짝수 버전을 설치해야된다.<br/>
    기본 실습<br/>
    웹 브라우저 실습<br/>

 >   자바 스크립트로 할수있는일<br/>
    1.웹 클라이언트 어플리케이션 개발<br/>
    2.웹 서버 개발<br/>
    3.모바일 어플리케이션 개발<br/>
    4.데스크톱 어플리케이션 개발<br/>
    5.게임 개발<br/>
    6.데이터베이스 관리<br/>