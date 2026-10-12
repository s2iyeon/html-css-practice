## 4강 - CSS 파일 만들고 첨부하는 법

### CSS 파일을 쓰는 이유
- `style` 속성에 스타일을 많이 넣으면 코드가 1~20줄로 길어져서 HTML이 지저분해진다
- 태그가 그림인지 글자인지 한눈에 파악하기 어려워진다
- 스타일이 길어지면 `.css` 파일로 따로 뺄 수 있다
- 파일명 끝에 `.css`를 붙이면 CSS 파일이 된다
- CSS는 Cascading Style Sheets의 약자이며, 스타일을 모아두는 파일이다 (Cascading은 폭포처럼 떨어진다는 뜻이며 나중에 자세히 배운다)

### CSS 파일 연결
- `<link href="CSS 파일 경로" rel="stylesheet">`로 연결한다
- 닫는 태그가 없다
- `<head>` 안에 작성하며, `<title>` 아래에 두면 된다
- 파일 경로는 상대경로와 절대경로로 쓸 수 있다
  - 상대경로: 지금 파일 위치를 기준으로 한 경로 (예: `css/main.css`)
  - 절대경로: 어디서 열어도 같은 전체 주소 (예: 내 컴퓨터의 전체 폴더 경로, 또는 `https://...` 같은 인터넷 주소)
  - 내 프로젝트 안의 파일은 보통 상대경로를 쓴다 (절대경로는 다른 컴퓨터에서 파일을 못 찾을 수 있다)

### class 선택자
- CSS 파일에서 `.class이름 { 스타일 }` 형태로 작성한다
- 예시: `.profile { width: 100px; display: block; margin-left: auto; margin-right: auto; }`
- 긴 스타일을 `.profile`이라는 이름으로 묶은 것이며, 이 이름을 쓰면 안의 속성 4개가 함께 적용된다
- HTML 태그에 `class="profile"`을 넣어서 사용한다
- class는 스타일을 묶는 단위이다
- 점(`.`)은 CSS 파일에서만 붙이고, HTML의 `class=""` 안에는 점 없이 이름만 쓴다
- 서로 다른 용도의 class에 같은 이름을 쓰지 않도록 주의한다 (같은 class를 여러 태그에 붙여서 재사용하는 것은 가능하다)

### tag 선택자
- 태그 이름으로 스타일을 지정한다 (예: `p { text-align: center; }`)
- 해당 태그 전체에 스타일이 적용된다

### id 선택자
- CSS 파일에서 `#special { text-align: center; }`로 작성하고, HTML 태그에 `id="special"`을 넣는다
- id는 자바스크립트에서 주로 사용하기 때문에 CSS에서는 `.class`를 쓰는 것을 추천한다

### 선택자와 우선순위
- 이런 방식을 통틀어 CSS selector(선택자)라고 부른다
- 같은 속성이 겹치면 우선순위가 높은 스타일이 적용된다
- 우선순위 점수: `style=""` 속성 1000점 > id 선택자 100점 > class 선택자 10점 > tag 선택자 1점
- 예: `.content`가 `color: red;`, `p`가 `color: green;`, `#special`이 `color: blue;`이면 id 선택자가 이긴다

### VSCode 팁
- 화면 분할은 파일 탭을 드래그해서 끌어오면 된다