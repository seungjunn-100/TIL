# 변수(Variable)
- 값을 저장하는 공간

- 자료를 저장할 수 있는 **이름이 주어진 기억 장소**

- 변수에 값을 할당하여 선언하면 메모리 어딘가의 주소에 값이 저장된다.

- `let`, `const`, `var`


<br />
<br />


## 변수 이름 짓는법
- 저장된 값을 잘 나타낼 수 있는 의미있는 이름

- 이름이 구체적일수록 좋다.

- 변수 규칙
  - 라틴문자(0-9, a-z, A-Z), _(underscore)
  - 대소문자를 구분한다.
  - 추천 : `recommendedName` - Camel Case 방식
  - 여러개의 변수를 숫자로 구분 ❌ (최대한 의미있고 구체적인 이름으로 작성)
  - 한국어 ❌
  - 숫자로 시작 ❌
  - 특수문자 ❌ (_, $ 두가지는 예외)
  - [예약어](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#keywords) ❌

```javascript
// 나쁜 예제
let number = 30;
let audio1; // 여러개의 변수를 숫자로 구분 ❌
let audio2; // 여러개의 변수를 숫자로 구분 ❌

// 좋은 예제
let myAge = 30;
let backgroundAudio; // 최대한 의미있고 구체적인 이름으로 작성
let windAudio; // 최대한 의미있고 구체적인 이름으로 작성

// 꿀팁
// 구체적인 부분을 뒤로 빼주면 나중에 관련 변수들을 찾을 때 용이하다.
let audioBackground;
let audioWind;
```


<br />
<br />


## 숫자 타입 (number)
```javascript
let integer = 126; // 정수
let negative = -126; // 음수
let double = 1.26; // 실수

let binary = 0b1111011; // 2진수
let octal = 0o173; // 8진수
let hex = 0x7b; // 16진수

console.log(0 / 123); // 0
console.log(123 / 0); // Infinity
console.log(123 / -0); // -Infinity
console.log(123 / 'text'); // NaN(Not a Number)
```


<br />
<br />


## 문자열 타입 (number)
```javascript
let string = '안녕하세요';
string = `안녕!` // Backtick(``) 사용 가능

// 특수 문자 출력하는법
string = "'안녕!'";
string = '"안녕!"';

// 이스케이프 표현
// https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/String
string = '안녕!\n내 이름은\t\t백이야\\\u09AC';

// 템플릿 리터럴 (Template Literal)
let id = '길동';
// ES6 이전에는 다음과 같이 작성하였다.
let greetings = "'안녕!, " + id + "👋🏻\n즐거운 하루 보내!'"
// ES6부터는 Backtick(``)을 사용하여 더 쉽게 작성할 수 있게 되었다.
greetings = `'안녕!, ${id}👋🏻
즐거운 하루 보내!'`;
```