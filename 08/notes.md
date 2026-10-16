## 8강 - 레이아웃 만들기 숙제 : Blog 글목록 만들기

### 7강 숙제를 float로 다시 만들기
- 같은 레이아웃을 `inline-block`이 아니라 `float`로 다시 만들었다
- 왼쪽 글 영역(80%)과 오른쪽 사진 영역(20%)을 모두 `float: left;`로 가로 배치한다
- 프로필 사진과 이름 덩어리도 `float: left;`로 나란히 놓는다

### inline-block 버전과 비교
- `inline-block`은 태그 사이 공백이 띄어쓰기로 계산되어, 태그를 붙여 써야 한다
- `float`는 태그 사이 줄바꿈이나 공백을 신경 쓰지 않아도 된다
- `inline-block`은 높이가 다른 요소를 맞추려면 `vertical-align`이나 `line-height` 같은 숫자 조정이 필요하다
- `float`는 요소들이 위쪽에서 시작해서 별도의 정렬 없이 나란히 놓인다

### 구조 나누기
- 프로필 영역(사진 + 이름)과 글 영역(제목 + 내용)을 나눠서 작성한다
- 글 영역에 `clear: both;`를 주면 위의 `float` 요소들 아래로 내려온다
- 이름과 시간의 간격은 `margin`으로 조절한다

### 정리
- 전체를 감싸는 `container`에 `width`를 주고 가운데 정렬한다 (`margin-left: auto; margin-right: auto;`)
- `div`는 원래 `display: block`이라 따로 쓰지 않아도 된다
- class 이름 앞에 `blog-`처럼 붙여서 이름이 겹치지 않게 한다
- 박스에 `height`를 고정하면 글이 길어질 때 넘칠 수 있다