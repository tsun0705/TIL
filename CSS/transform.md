# 2019-09-07 Today I Learned

## transform
* 요소에 회전, 크기 조절, 기울이기, 이동 효과를 부여할 수 있다.
* 요소에 변형을 오른쪽에서 왼쪽으로 순서대로 적용한다.

# transform - scale
~~~
img {
  width: 400px;
  transform: scale(0.5); /* 가로 세로가 1/2 만큼 줄어든다. */
  /* scale(1.5, 0.5) x축 1.5배 y축 0.5배 */
}
~~~
![image](https://user-images.githubusercontent.com/58898466/132282733-0a883184-f0f5-421f-8bda-80d2344066d2.png)

* 크기 조절을 담당한다.
* 괄호안에 한 개의 숫자 또는 두 개의 숫자를 넣을 수 있다.
* 공간은 그대로 갖고 사이즈만 줄어든다.
* scale을 크게 입력하면 아래 영역을 침범한다.
* x축만 조절하고 싶으면 scaleX, y축만 조절하고 싶으면 scaleY를 사용한다.

