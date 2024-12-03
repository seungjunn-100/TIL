# HTML Basics


<br />
<br />


## HTML 이란
- Hyper Text Markup Language의 약자
  - `Hyper Text`
    - (내, 외부)링크에 따라 다양한 문서들로 넘어갈 수 있는 형태이다.
  - `Markup Language`
    - 태그를 이용하여 문서의 구조를 표기하는 형태이다.
    - content(제목, 글, 이미지, 버튼 등)의 성격을 표시해주는 기능만 있다.
  
- 웹 브라우저상에서 보여지도록 디자인된 문서이다.

- 웹 페이지를 구조화 하기 위해 마크업 언어를 사용한다.


<br />
<br />


## HTML 역사
- 1990년 팀 버너스리에 의해 개발되었다.

- 1993년 HTML 1.0이 IETF(Internet Engineering Task Force)에 의하여 표준으로 등장했다.

- 1995년 HTML 2.0이 IETF에 의하여 표준으로 등장했다.

- 1997년 HTML 3.2이 W3C(World Wide Web Consortium)에 의해 권고안으로 등장했다.

- 1999년 HTML 4.0이 W3C에 의해 권고안으로 등장했다.
  - 안정된 표준의 HTML 버전
  - CSS(Cascading Style Sheet)로 디자인적인 요소를 구분하게 되었다.
  - HTML로는 웹페이지의 전반적인 구조만을 명시하도록 원칙을 정하였다.

- 2000년 XHTML이 W3C의 새로운 표준 권고안으로 등장했다.
  - XML(Extensible Markup Language)의 엄격함을 주요 내용으로 HTML을 합성한 웹 표준
  - W3C는 시장 요구에 부응하지 못했다.
  - 그로 인해 대중적인 브라우저를 가지고 있던 기업들(Apple, Mozilla, Opera)이 WHATWG(Web Hypertext Application Technology Working Group)라는 단체를 만드는 계기가 됐다.
  - WHATWG이 HTML에 기초하여 웹 기술과 시장의 요구를 분석하여 HTML5 작업을 착수했다.

- 2008년 HTML 5.0이 W3C에 의해 초안으로 등장했다.
  - W3C의 HTML5 수용

- 2014년 HTML 5.0이 W3C에 의해 표준안으로 등장했다.
  - WHATWG는 W3C와 협업을 진행하면서도 W3C와는 별도로 독자적인 HTML 표준의 작업을 시작했다.
  - HTML Living Standard라는 이름으로 발표했다.
  - HTML Living Standard는 W3C의 HTML5와는 달리 버전 없이 그때그때 업데이트된다.

- 2019년 HTML Living Standard가 표준화가 되었다.
  - 표준이 2개면 혼란이 발생하기 때문에 W3C와 WHATWG는 논의를 통해 HTML 표준을 HTML Living Standard로 단일화하였다.


<br />
<br />


## HTML 작성 규칙
- HTML 문서는 요소(elements)들로 구성된다.

- 태그를 통해 어떤 요소인지 (제목, 본문, 이미지, 비디오 등) 명시한다.

- 여는 태그와 닫는 태그로 요소의 범위를 지정한다.
  ```html
    <p>내용(content)</p>
  ```

- 요소의 속성은 속성명 = "속성값" 형식으로 기술한다.
  ```html
    <img src="image.png" alt="profile">
  ```

- 중첩 요소(Nesting elements)
  ```html
    <p><strong>내용(content)</strong></p>
  ```

- 빈 요소(Void Elements)
  - 종료 태그 없이 단독으로 사용되는 요소
  - XHTML에서 빈 요소인 경우에는 뒤에 슬래쉬(/)를 넣어줘야지만 브라우저가 Closing tag를 찾지 않고 동작을 하는 형태이다.
  - HTML5 에서는 빈 요소의 슬래쉬(/) 작성은 자유지만 한가지의 형태로 일관성있게 코드를 작성해야한다.
  ```html
    <hr>, <br>, <img>, <meta>
  ```

- Element Tag와 Container Tag
  - Element Tag : 태그 자체가 UI를 나타내는것들이 있다.
  - Container Tag : 태그 자체로 UI가 표시되는 것이 아니라 다른 UI 요소를 담는다.

- 블록(Block)과 인라인(Inline)
  - 블록 레벨 요소 : 요소 하나당 한 줄을 꽉 차지한다.
  - 인라인 레벨 요소 : 요소의 컨텐츠만큼 자리를 차지한다.

- 태그의 경우 대소문자를 구분하지 않는다.

- HTML5 에서는 모두 소문자로 작성하는 것을  권장한다.

- 참고 사이트
  - [HTML](https://developer.mozilla.org/ko/docs/Learn/HTML/Introduction_to_HTML/Getting_started)
  - [HTML Element](https://developer.mozilla.org/ko/docs/Web/HTML/Element)
  - [HTML Standard](https://html.spec.whatwg.org/) - 예제를 통한 태그 사용법 참고 ⭐️


<br />
<br />


## HTML 문서의 구조
- HTML5의 표준을 지키는 HTML의 기본 골격
  ```html
    <!DOCTYPE html>
    <html>
      <head>
        <!-- HEAD 영역 -->
      </head>
      <body>
        <!-- BODY 영역 -->
      </body>
    </html>
  ```

- `<!DOCTYPE html>`
  - Document Type(문서의 타입)을 명시한다.
  - HTML5 표준 이전에는 버전을 명시하여 브라우저가 명시된 버전에 맞는 문법으로 해석하였다.
  - 현재는 대부분의 브라우저가 HTML5의 표준을 준수하고 있기때문에 html이라고만 적어도 해석이 가능하다.

- `<html lang="ko">`
  - 페이지 전체의 컨텐츠를 감싸는 최상위(root) 요소
  - lang 속성 : 문서에서 사용하는 주언어 language 명시

- `<head>`
  - 문서의 메타데이터(웹사이트에 대한 설명)
  - CSS, script 링크(외부 파일 연결)

- `<body>`
  - 문서의 UI 구성 요소들


<br />
<br />


## `<head>` 설정

### 문자 인코딩
- HTML 파일의 인코딩 방식을 명시하는 태그이다.

- 유니코드인 UTF-8의 charset으로 다양한 언어를 모두 표현할 수 있다.

```html
<meta charset="UTF-8" />
```

<br />

### `<title>`
- HTML 파일의 제목으로 웹 브라우저 타이틀에 나타난다.

<br />

### 메타데이터
- 웹사이트에 대한 설명

- SEO (Search Engine Optimization) 검색 엔진 최적화를 위해서는 meta tag, semantic tag 등을 통한 markup을 효과적으로 할 필요가 있다.

```html
<title>SEO</title>
<meta name="description" content="metadata를 알아보자!" />
<meta name="keywords" content="title, meta, SEO" />
<meta name="author" content="BBaek" />
```

<br />

### OG ( Open Graph Data )
- Facebook에서 만들었으며 웹 사이트에 더 풍부한 메타 데이터를 제공한다.

```html
<meta property="og:title" content="BBaek’s의 포트폴리오" />
<meta property="og:type" content="website" />
<meta property="og:url" content="url" />
<meta property="og:image" content="url" />
```

<br />

### 외부 리소스 연결
```html
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon" />
<link rel="stylesheet" href="css/style.css" />
<script src="js/script.js></script>
```

**중요한 POINT ⭐️**
- 브라우저에서 HTML을 읽는 방법
  - 브라우저에서 HTML을 다운 받는다.
  - HTML을 처음부터 끝까지 읽어보면서 필요한 리소스가 있는지 없는지 다운로드를 받아야하는지 확인을 한다.
  - 만약 `<script>`가 있다면 브라우저가 HTML을 읽는 도중에 `<script>`를 다운받을 때 까지 동작을 멈추고 다운로드가 완료 된 후에야 HTML을 다시 읽기 시작한다.
  - HTML을 모두 읽은 후 브라우저에 UI를 보여준다.

- defer 옵션을 명시해주면 이러한 현상을 해결할 수 있다.
  - HTML을 읽을 때 JavaScript 파일은 넘어가고 나중에 다운로드 받아도 된다고 명시해주는 옵션이다.

```html
<script src="js/script.js" defer></script>
```