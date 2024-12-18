# 내장객체(Built-in Object)
- 브라우저의 Javascript 엔진에 내장된 객체를 말한다.

- [Javascript 참고서](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference)


<br />
<br />


## 래퍼객체(Wrapper Object)
- 원시값을 필요에 따라서 관련된 빌트인 객체로 변환한다.
```javascript
const number = 123;
console.log(number); // 123(숫자), 원시 타입
// number 원시 타입을 감싸고 있는 Number 객체로 감싸진다.
// 평소에는 원시 타입으로 사용되다가 함수나 프로퍼티를 호출하게 되면 그 데이터 타입에 해당하는 객체로 변환이 된다.
console.log(number.toString()); // 123(문자열)
console.log(number); // 123(숫자), 그대로 원시 타입으로 사용되어질때는 원시 타입이다.

const text = 'text';
console.log(text); // text(문자열), string 원시 타입
console.log(text.length); // 4, String 객체

// 각 데이터 타입에 대응하는 객체가 제공된다.
// number - Number
// string - String
// boolean - Boolean
// symbol - Symbol
```

### Boolean
```javascript
// Boolean 객체
// const isTrue = true;
const isTrue = new Boolean(true); // 객체를 사용하면 메모리를 더 소비하기 때문에 좋지않다.
console.log(isTrue); // [Boolean: true]
console.log(isTrue.valueOf()); // true

// Falshy
// 0, -0, null, undefined, NaN, ''

// Truthy
// 1, -1, 'false', [], {}
```


<br />
<br />


## 전역객체(Global Object)
```javascript
console.log(globalThis); // 전역
console.log(this); // 전역
// 노드에서 this는 현재 모듈에 있는 정보를 출력한다.
// 출력 : {}, 현재 모듈에 아무것도 export된게 없기때문에 아무것도 나오지 않는다.
// 자바스크립트에서 this란 전역 객체를 가르킨다.
// 브라우저의 경우는 window가 전역 객체이다.
console.log(Infinity);
console.log(NaN);
console.log(undefined);

// 자바스크립트를 한줄씩 표현할 수 있는 함수
eval('const num = 2; console.log(num);');

// 숫자가 유한한지 무한한지 확인할 수 있는 함수 
console.log(isFinite(1)); // true(유한)
console.log(isFinite(Infinity)); // false(무한)

// 문자열인데 숫자를 나타내고 있다면 숫자로 변환해줄 수 있다.
console.log(parseFloat('12.34')); // 12.34(숫자)

// 문자열 안에 있는 숫자를 정수로 변환해준다.
console.log(parseInt('12.34')); // 12(숫자)
console.log(parseInt('12')); // 12(숫자)

// URL (URI, Uniform Resource Identifier 하위 개념)
// 어떤 리소스를 나타낼 수 있는 단 하나의 고유한 주소나 아이디를 가르킨다.
// 아스키 문자로만 구성되어야 한다.
// 한글이나 특수문자는 이스케이프 처리해야한다.
const URL = 'https://자바스크립트.com'
const encoded = encodeURI('https://자바스크립트.com');
console.log(encoded); 
// https://%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8.com

const decoded = decodeURI(encoded);
console.log(decoded); // https://자바스크립트.com

// 전체 URL이 아니라 부분적인 것을 사용할 때는 Component를 이용
const part = '자바스크립트.com';
console.log(encodeURIComponent(part)); 
// %EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8.com
```


<br />
<br />


## 숫자 함수들
```javascript
const num1 = 123;
const num2 = new Number(123);

console.log(typeof num1); // 123, 
console.log(typeof num2); // [Number: 123]


// Number 클래스에는 스태틱한 프로퍼티가 있다. (즉, 객체를 만들지 않고 클래스 레벨에서 접근이 가능하다.)
// 정수에서 사용할 수 있는 최대값
console.log(Number.MAX_VALUE); // 1.7976931348623157e+308 (e+308 = 10의 308승)
// 정수에서 사용할 수 있는 최소값
console.log(Number.MIN_VALUE); // 5e-324
// 정수에서 안전하게 사용할 수 있는 최대값
console.log(Number.MAX_SAFE_INTEGER); // 9007199254740991
// 정수에서 안전하게 사용할 수 있는 최소값
console.log(Number.MIN_SAFE_INTEGER); // -9007199254740991
// 숫자가 아닌 것
console.log(Number.NaN); // NaN
// 무한
console.log(Number.NEGATIVE_INFINITY); // -Infinity
console.log(Number.POSITIVE_INFINITY); // Infinity

// 사용 예제
if (num1 === Number.NaN) { // num1이 숫자인지 아닌지 확인
}
if (Number.isNaN(num1)) { // 정적 함수를 이용
}
if (num1 < Number.MAX_SAFE_INTEGER) { // num1이 숫자범위안에 있는지 없는지 확인
}

// 지수표기법 (매우 크거나 작은 숫자를 표기할 때 사용, 10의 n승으로 표기)
const num3 = 102;
console.log(num3.toExponential()); // 1.02e+2

// 실수를 반올림하여 문자열로 변환
const num4 = 1234.56;
console.log(num4.toFixed()); // 1235(문자열)

// 숫자 자체를 문자열로 반환
console.log(num4.toString()); // 1234.56(문자열)

// 나라에 맞는 언어로 숫자를 변환
console.log(num4.toLocaleString('ar-EG')); // ١٬٢٣٤٫٥٦(이집트 아랍어)

// 원하는 자릿수까지 유효하도록 반올림
console.log(num4.toPrecision(5)); // 1234.6
console.log(num4.toPrecision(2)); // 1.2e+3 // 전체 자릿수 표기가 안될때는 지수표기법으로 반환

// EPSILON // 0과 1사이에서 나타낼 수 있는 가장 작은 숫자
if (Number.EPSILON > 0 && Number.EPSILON < 1) {
  console.log(Number.EPSILON); // 2.220446049250313e-16
}

const num = 0.1 + 0.2 - 0.2;
console.log(num); // 0.10000000000000003
// 10진수로 계산을 할때는 0.1이 맞다.
// 자바스크립트에서 내부적으로 계산을 할때에는 10진수를 2진수로 각 각 변환을 하여 계산을 하여 다시 10진수로 값을 반환한다.
// 이런 과정에서 정확하게 부동소수점까지 계산이 되지 않아 작은 오차가 발생할 수 있다.
// 이런 작은 오차를 나타내는 것이 EPSILON 이라고 볼 수 있다.

function isEqual(original, expected) {
  return original === expected;
}
console.log(isEqual(1, 1)); // true
console.log(isEqual(0.1, 0.1)); // true
console.log(isEqual(num, 0.1)); // false

// 작은 차이도 같다고 간주하고 싶다면
function isEqual(original, expected) {
  return Math.abs(original - expected) < Number.EPSILON; // Math.abs(original - expected) - 절대값(-가 되지 않도록)
}
console.log(isEqual(1, 1)); // true
console.log(isEqual(0.1, 0.1)); // true
console.log(isEqual(num, 0.1)); // true
```