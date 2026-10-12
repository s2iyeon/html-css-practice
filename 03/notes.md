## 3강 - 기본적인 웹페이지 스타일링

### style 속성
- 거의 모든 HTML 태그에는 `style` 속성을 넣을 수 있다
- `스타일명: 값;` 형태로 작성하며, 여러 개를 쓸 때는 `;`로 구분한다 (예: `<p style="font-size: 16px; color: red;">`)
- `width`: 가로폭
- `margin`: 여백이며 `margin-top`, `margin-bottom`, `margin-left`, `margin-right`로 방향별 지정이 가능하다

### 이미지 가운데 정렬
- 아래 세 줄을 함께 사용한다 (자세한 원리는 나중에 다시 배운다)
- `display: block;`
- `margin-left: auto;`
- `margin-right: auto;`

### 글자 스타일링
- `font-size: 16px;`: 글자 크기
- `font-family: '폰트명';`: 글자 종류이며 시스템에 설치된 폰트명을 쓸 수 있다
- `color: 색상명;` 또는 `color: #컬러코드;`: 글자 색상
- `letter-spacing: 값;`: 자간 조절
- `text-align: center;`: 글자 가운데 정렬 (`left`는 왼쪽, `right`는 오른쪽)
- `font-weight: 100~900;`: 글자 굵기이며 숫자가 클수록 굵다

### 단위
- `px`: 화면 픽셀 기준의 고정 크기이다
- `vw`: 브라우저 창 너비 기준이며 1vw는 창 너비의 1%이다 (예: `50vw`는 창 너비의 절반)
- `%`: 부모 태그(나를 감싸고 있는 태그) 크기 기준이다 (예: 부모 너비가 800px일 때 `50%`는 400px)
- 이 외에도 여러 단위가 있다

### span과 strong
- `<span></span>`: 글자 일부만 스타일링할 때 감싸서 사용하며, 특별한 의미가 없는 태그이다
- `<strong></strong>`: 글자를 굵게 표시하는 태그이며, 기본적으로 `font-weight: 700` 정도로 보인다