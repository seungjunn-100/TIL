# 시맨틱 웹(Semantic Web)
- 요소의 의미를 고려하여 구조를 설계하고 코드를 작성하는게 좋다.

- 문서상으로 크게 의미 없는 UI 요소들은 CSS에서 작업해주는게 좋다.
  
- 의미론적인 마크업을 사용하면 좋은점
  - 검색 엔진은 의미론적 마크업을 분석하여 페이지의 검색 랭킹에 영향을 줄 수 있는 중요한 키워드로 간주한다.
  - 시각 장애가 있는 사용자가 스크린리더로 페이지를 탐색할 때 의미론적 마크업을 푯말로 사용할 수 있다.
  - 의미가 없는 끊임없는 div 들을 탐색하는 것보다 의미있는 코드 블록을 찾는 것이 훨씬 쉽다.
  - 개발자에게 태그 안에 채워질 데이터 유형을 제안한다.
  - 의미있는 이름짓기(Semantic naming)는 적절한 사용자 정의 요소 / 구성 요소의 이름짓기(naming)를 반영한다.


<br />
<br />


## 시맨틱 태그(Semantic Tag)
- `<header>`
  - 소개 및 탐색에 도움을 주는 콘텐츠
  - 제목, 로고, 검색 폼, 작성자 이름 등을 포함할 수 있다.
  - 전체 페이지를 대표하는 제목으로 들어갈 수 있다.
  - 한 기사, 논문의 글 제목으로 들어갈 수 있다.

- `<nav>`
  - 현재 페이지 내 또는 다른 페이지로의 링크를 보여주는 구획
  - Home > menu_1 > menu_1_1 > menu_1_1_1

- `<main>`
  - body 태그의 하위 자식으로 사용되며 단 하나만 사용이 가능하다.
  - 여러개 사용시에는 유일한 main 요소 외에 나머지 요소는 hidden 속성을 사용하여 눈에 보이지 않게 해야한다.

- `<article>`
  - 독립적으로 구분해 배포하거나 재사용할 수 있는 구획을 나타낸다.
  - 독립적인 컨텐츠라서 그것만의 의미를 갖고 있으므로 다른 곳에서도 사용이 가능하다.
  - 게시판과 블로그 글, 매거진이나 뉴스 기사 등에 사용이 된다.
  - 식별할 수단으로 주로 제목(`<h1>` ~ `<h6>`) 요소를 넣어준다.
  ```html
  <article>
    <header>
      <h2></h2>
    <header>

    <section><section>

    <footer><footer>
  </article>
  ```

- `<section>`
  - 문서의 독립적인 구획을 나타낸다.
  - `<article>`과는 다르게 단독적으로 사용 불가
  - 요소의 콘텐츠를 따로 구분해야 할 필요가 있으면 `<article>`요소로 사용하는걸 고려해봐야 한다.

- `<aside>`
  - 문서의 주요 내용과 간접적으로만 연관된 부분을 나타낸다.
  - 추가적인, 부가적인 정보지만 없다고 해서 본문에 크게 문제가 되지 않은 것들을 포함한다. 
  - 사이드바 혹은 콜아웃 박스

- `<footer>`
  - 구획의 작성자, 저작권 정보, 관련 문서 등을 포함할 수 있다.
  - 사이트의 전체를 아우를 수 있는 링크들을 포함할 수 있다.


<br />
<br />


### 웹 표준 ( Web Standards )
- HTML5는 W3C에서 2014년에 공식 표준화 되었다.

- 2019년에 WHATWG에 의해 HTML Living Standard가 표준화 되었다.

- HTML이 표준화 되기 이전에는, 익스플로러의 액티브X처럼 독자적인 플러그인이 존재하기도 했었다.

- 웹 표준을 준수하여 작성한다면 운영체제, 브라우저마다 의도된 대로 보여지는 웹 페이지를 만들 수 있다.


<br />
<br />


### 웹 접근성 ( Web Accessibility )
- 웹 접근성은 장애를 가진 사람과 장애를 가지지 않은 사람 모든 사용자들이 웹 사이트를 이용할 수 있게 하는 방식을 가리킨다.

- 웹 접근성은 장애를 갖지 않아도 특정 상황에 따라 문제가 있는 사용자들도 정보와 기능에 동등하게 접근할 수 있다.
  - 작은 화면, 다른 입력 모드 등을 가진 휴대폰, 스마트 워치, 스마트 TV 및 다른 디바이스를 사용하는 사람
  - 나이가 들어감에 따라 기능적 능력이 변한 연로한 사람
  - 팔이 부러지거나 안경을 잃어버려서 "일시적인 장애"를 겪는 사람
  - 밝은 햇빛이나 소리를 듣기 힘든 환경에 있어 "상황적 제약"을 겪는 사람
  - 느린 인터넷을 사용하거나 제한적이거나 비싼 대역폭을 사용하는 사람

- 웹 브라우징에 쓰이는 보조과학기술 : 스크린리더, 화면 돋보기, 음성 인식, 키보드 오버레이 등


<br />
<br />


### 웹 호환성 ( Cross Browsing )
- 크롬, 사파리, 엣지, 웨일 등 다양한 웹 브라우저가 있는데 브라우저 마다 화면을 보여주는 렌더링 엔진이 달라 브라우저에 따라서 다르게 보일 수 있기 때문에, 브라우저 버전, 종류와 상관 없이 똑같은 웹 페이지를 보여주기 위해서는 크로스 브라우징을 해야한다.

- 웹 표준 준수를 통한 브라우저 호환성 확보
  - HTML, CSS 문법 준수
  - 동작, 레이아웃, 플러그인 호환성