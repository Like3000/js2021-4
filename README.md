# 강태훈 [201840104]
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