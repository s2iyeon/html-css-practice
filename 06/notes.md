## 6강 - 레이아웃 만들기 1 : 호환성 좋은 float

### 레이아웃 만드는 방법
- 레이아웃을 만드는 방법은 4~5가지가 있다
- 그중 첫 번째로 `float`를 배운다 (전통적이고 호환성이 좋은 방법이다)
- `float`로 박스를 가로로 배치하는 법만 알면 원하는 레이아웃을 대부분 만들 수 있다

### wrapper (container)
- 레이아웃 전체를 감싸는 박스를 하나 만들어두면 유용하다
- 이름은 보통 `wrapper` 또는 `container`를 class명으로 쓴다
- 최대 너비(`max-width`) 같은 것을 미리 지정할 수 있어서 박스들이 삐져나가지 않게 해준다
- 꼭 필요한 것은 아니지만 있으면 레이아웃을 관리하기 편하다

### float로 가로 배치하기
- `div`는 `display: block`이라서 가로 한 줄을 다 차지한다
- 박스를 옆으로 나란히 놓으려면 `float`를 사용한다
- `float: left`는 요소를 대열에서 빼서 왼쪽으로 붙이는 속성이다
- 한 박스에만 주면 다음 박스가 빠진 박스가 없는 것처럼 위로 올라와 같은 위치에서 시작한다
- 그래서 나란히 놓으려면 두 박스 모두 `float: left;`를 준다
- `float: right`는 오른쪽으로 붙이는 속성이다

### float의 부작용과 clear
- `float`를 준 박스는 대열에서 빠져서 떠 있기 때문에, 그 아래 박스(예: `footer`)가 위로 올라와 가려진다
- `float` 다음에 오는 요소에 `clear: both;`를 주면 이 현상이 해결된다
- `clear`에는 `left`, `right`, `both`가 있으며, 어느 쪽 float를 해제할지 헷갈리면 `both`를 사용한다

```html
<div class="left-menu"></div>
<div class="right"></div>
<div class="footer"></div>
```

```css
.left-menu {
  width: 20%;
  height: 400px;
  background-color: cornflowerblue;
  float: left;
}

.right {
  width: 80%;
  height: 400px;
  background-color: coral;
  float: left;
}

.footer {
  width: 100%;
  height: 100px;
  background-color: grey;
  clear: both;
}
```

### float: none
- `float`의 기본값이며, "float를 적용하지 않는다"는 뜻이다
- `float` 다음에 오는 요소(예: `footer`)에 `clear: both;`와 함께 적어두면 나중에 생길 수 있는 버그를 예방하는 데 도움이 될 수 있다 (강사님 자료 기준, 필수는 아니다)