# CSS Basics


<br />
<br />


## CSS 란
- 웹 페이지의 스타일링을 담당
- 기본 문법
  
  ```css
  div { /* Selector(태그, .클래스, #아이디) */
    color: pink; /* Property : Value; */
  }
  ```
- Cascading Style Sheets
  - Cascading : 폭포 같은, 연속 되는, 우선순위가 있는
  - Style Sheets : 스타일 시트
  - 두가지 이상의 스타일이 있을 때 어떤 우선순위에 따라 적용할지 결정한다.
  - 우선순위
    - !important
      - 모든 우선순위를 무시하고 우선시해야 할 때 사용한다.
      - 왠만하면 사용하지 않는게 좋다.
    - 동일한 레벨에서는 나중에 작성한 스타일이 우선순위가 높다.
  ```
  !important >>> inline >>> #id >>> .class >>> HTML tag
  ```


<br />
<br />


## CSS 정의 방법
- 태그 안에 style 속성을 사용한 `Inline` 방식
  ```html
  <div style="color: pink; font-size: 26px;"></div>
  ```

- HTML 파일 안에 `<style>` 태그 안에 작성
  ```html
  <head>
      <style>
          div {
            color: pink;
            font-size: 26px;
          }
      </style>
  </head>
  ```
  
- CSS 파일에 작성 후 HTML 파일에서 `<link>` 
  ```html
  <head>
      <link rel="stylesheet" href="/css/style.css" />
  </head>
  ```


<br />
<br />


## CSS 선택자


<br />
<br />


## CSS 상속


<br />
<br />


## 크기 단위