# 2021-09-06 Today I Learned

## Box Model
![image](https://user-images.githubusercontent.com/58898466/132152099-6478ed96-d4b3-427a-a542-9720259fd88c.png)
* content : 콘텐츠가 표시되는 영역, width와 height로 영역의 크기를 정의한다.
* padding : 콘텐츠와 테두리사이의 여백
* border : padding과 margin 사이의 테두리
* margin : 가장 바깥 쪽 레이어로 콘텐츠와 패딩, 테두리를 둘러 싸면서 해당 박스와 다른 요소 사이의 공백 역할을 한다.
***

## width, height
* width는 가로 height는 세로 길이를 지정한다.
* inline 요소는 적용할 수 없다.
* width - https://developer.mozilla.org/ko/docs/Web/CSS/width
* height - https://developer.mozilla.org/ko/docs/Web/CSS/height
***

## max-width, max-height, min-width, min-height
* 요소의 최소 너비, 높이 및 최대 너비, 높이를 설정한다
* 속성의 사용값이 자신의 값보다 작아지는걸 방지합니다.
* 사용 방법은 width, height와 동일하다.
***

## margin
* 네 방향의 바깥 여백 영역을 설정한다.
* inline 요소는 좌/우만 설정이 가능하다.
* margin-top, margin-right, margin-bottom, margin-left의 단축 속성이다.
* margin: 10px;만 입력 시, 네 방향 모두 10px 여백을 설정한다.
* margin: 10px 20px;은 위/아래 10px, 좌/우 20px 여백을 설정한다.
* margin: 10px 20px 30px;은 위 10px, 좌/우 20px, 아래 30px 여백을 설정한다.
* 퍼센트로 입력 시 부모의 width 값의 퍼센트로 여백을 설정한다.
* https://developer.mozilla.org/ko/docs/Web/CSS/margin
***

## margin collapsing (마진 상쇄)
* 마진 상쇄, 겹침, 중복 등 으로 불린다.
* 여러 블록요소들이 위/아래 margin인 경우 가장 큰 크기를 가진 margin으로 상쇄되는 현상이다.
* 음수도 사용이 가능하다.
  - 인접 형제
    + 두 형제 요소의 위/아래 여백이 만나 상쇄된다.
  - 부모-자식요소 간
    + 부모 블록에 padding, border, inline content가 없어서 부모와 자식의 margin-top이 만나는 경우
    + 부모 블록에 padding, border, inline content가 없고, 부모-자식을 분리할 height값이 지정되지 않아 부모와 자식의 margin-bottom이 만나는 경우
  - 빈 블록
    + border, padding, content가 없고, height 또한 존재하지 않으면, 해당 블록의 margin-top과 margin-bottom이 상쇄된다.
***

## padding
* 네 방향의 안쪽 여백 영역을 설정한다.
* margin과 사용 방법이 동일하지만 패딩 상쇄는 존재하지 않는다.
* 음수는 사용할 수 없다.
***

## border-style
* 테두리의 네 면의 스타일을 지정한다.
* https://developer.mozilla.org/ko/docs/Web/CSS/border-style

## border-width
* 테두리의 두께를 설정한다.
* https://developer.mozilla.org/ko/docs/Web/CSS/border-width

## border-color
* 테두리 색상을 지정한다.
* https://developer.mozilla.org/ko/docs/Web/CSS/border-color

## border
* border 단축 속성은 요소의 테두리를 설정한다.
* 순서는 상관없이 설정 가능하다.
* https://developer.mozilla.org/ko/docs/Web/CSS/border

## border-radius
* 테두리 경계의 꼭짓점을 둥글게 만든다.
* https://developer.mozilla.org/ko/docs/Web/CSS/border-radius
***

## box-sizing
* 요소의 너비와 높이를 계산하는 방법을 지정한다.
* content-box
  - 기본값이며, width와 height 속성이 콘텐츠 영역만 포함하여 계산한다.
* border-box
  - width와 height 속성이 콘텐츠 너비 + 테두리 + 패딩까지 포함한 상태이다.

