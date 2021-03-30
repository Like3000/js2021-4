# 강태훈 [201840104]
## [03월 23일]
#### 논리 연산자<br/>

>! 	논리부정 연산자<br/>
ex)<br/>
console.log(!true);		false<br/>
console.log(!false);		true<br/>
console.log(!(123>13))	false<br/>
console.log(!(123<12))	true<br/>

>||	논리합 연산자<br/>
ex)<br/>
true true = true<br/>
true flase = true<br/>
false true = true<br/>
false false = false<br/>

>&&	논리곱 연산자<br/>
ex)<br/>
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
>let 	변수를 바꿀수 잇음<br/>
const	변수 못바꿈<br/>
일단 상수(const)를 사용하고 오류가 발생하면 변수(let)로 교체<br/>

#### if조건문<br/>
>표현식이 true면 문장을 실행하고 false면 문장 무시<br/>
조건문을 만족해 실행되는 문장이 한 행이면 중괄호 생략가능<br/>
여러행이라면 중괄호로 감싸야함<br/>

>if else 조건문<br/>
두가지로 분명하게 나뉘는 상황에서 편리하게 사용할 수 있다<br/>

>중첩 조건문<br/>
조건문 안에 조건문을 중첩해 사용하는것<br/>
여러번 중첩 가능<br/>

>if else if 조건문<br/>
중첩 조건문의 중관호를 생략했을 때 만든 조건문<br/>
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