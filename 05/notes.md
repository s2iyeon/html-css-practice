## 5강 - 웹레이아웃의 기초 : div를 이용한 네모네모 박스 디자인

### div
- 네모난 박스를 만들고 싶을 때 `<div></div>` 태그를 사용한다
- `div`는 division(구역)의 약자이다

### 박스 색상과 크기
- 박스에 색을 줄 때는 `background-color`를 사용한다
- `color`는 박스 안의 글자 색을 바꾸는 속성이라서 박스 색은 바뀌지 않는다
- `width`만 주면 높이가 0이라서 박스가 보이지 않는다
- `height`만 주면 가로 너비는 화면을 꽉 채워서 보인다
- `div` 안에 글자를 넣으면 글자 높이만큼 박스 높이가 생겨서 `height` 없이도 보인다

### margin (바깥 여백)
- `margin: 30px;`처럼 쓰면 상하좌우에 30px씩 여백이 생긴다
- `margin: 5px 6px 7px 8px;`처럼 쓰면 상, 우, 하, 좌 순서(시계 방향)로 한 번에 지정한다
- 음수 값(예: `-20px`)도 가능하며, 여백이 줄어드는 것이 아니라 요소가 그 방향으로 당겨져서 위치가 움직이고 주변 요소와 겹칠 수 있다

### padding (안쪽 여백)
- 박스 테두리와 안쪽 내용 사이의 여백이다 (안쪽 마진이라고 생각하면 된다)

### border (테두리)
- 두께, 종류, 색상을 함께 지정해야 한다 (예: `border: 1px solid black;`)
- `solid`는 직선, `dotted`는 점선이다

### border-radius
- 테두리를 둥글게 만든다

### 박스 가운데 정렬과 display
- 이미지 가운데 정렬과 같은 방법을 쓴다 (`display: block; margin-left: auto; margin-right: auto;`)
- `div`는 원래 `display: block` 성질을 갖고 있어서 `display: block;`은 생략해도 된다
- 가로 폭이 화면 전체가 아니어야(`width`를 지정해야) 가운데 정렬이 눈에 보인다
- `display: block`은 가로 한 줄을 전부 차지하라는 뜻이다
- `div`, `p`, `h1`~`h6`, `li` 등이 기본적으로 `block`이다
- 이 성질이 싫으면 `display`에 다른 값(`inline`, `inline-block`, `flex` 등)을 줄 수 있으며, 아직 배우지 않았다

### 상속 (inherit)
- 부모 태그에 준 스타일을 자식 태그가 자동으로 물려받는 것을 상속이라고 한다
- 예: `<div class="box"><p>안녕하세요</p></div>`에서 `p`에 `class`를 주지 않고 `div`에 글자 스타일을 줘도 안의 `p`에 적용된다
- 상속되는 스타일은 정해져 있다 (`font-size`, `color`, `font-family`, `text-align` 등)
- 주로 글자와 관련된 스타일이 상속되며, 모든 스타일이 상속되는 것은 아니다

### 숙제 - box-shadow
- `box-shadow: offset-x offset-y blur-radius spread-radius color;` 순서로 작성하며, 값은 쉼표 없이 띄어쓰기로 구분한다 (예: `box-shadow: 5px 5px 10px 0 gray;`)
- `offset-x`: 양수면 그림자가 오른쪽, 음수면 왼쪽에 생긴다
- `offset-y`: 양수면 그림자가 아래쪽, 음수면 위쪽에 생긴다
- `blur-radius`: 숫자가 클수록 그림자가 흐려진다
- `spread-radius`: 숫자가 클수록 그림자 크기가 커진다
- `color`: 그림자 색을 지정한다
- `inset`: 키워드를 쓰면 그림자가 박스 바깥이 아니라 안쪽에 생긴다
- 웹 화면은 왼쪽 위 모서리가 기준(0, 0)이며 아래로 갈수록 y 값이 커진다 (수학 그래프와 y 방향이 반대이다)