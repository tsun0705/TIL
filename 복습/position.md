# 2021-09-15 Today I Learned

## position - relative
~~~
  <style>
    div {
      width: 200px;
      height: 200px;
      border: 5px solid orangered;
      margin-left: 150px;
    }

    #box {
      background-color: peachpuff;
      position: relative;
      top: 50px;
    }
  </style>
  <body>
    <div></div>
    <div id="box"></div>
    <div></div>
  </body>
~~~
![image](https://user-images.githubusercontent.com/58898466/133396685-6c566f2b-bb11-4bec-8e36-52b839f8bd42.png)

* position이 static (기본값)이 아니면 상하좌우로 이동이 가능하다.
* top: 50px로 지정할 경우 자기 자신의 기준으로 위에서 아래로 50px 만큼 이동한다.  
* 음수 값도 사용이 가능하다. 
* 상하좌우 동시에 사용하면 top, left만 적용된다.


## position - absolute
~~~
  <style>
    div {
      width: 200px;
      height: 200px;
      border: 5px solid orangered;
    }

    #box {
      width: 150px;
      height: 100px;
      border-radius: 30px;
      border-color: blue;
      background-color: cadetblue;
      position: absolute;
    }
  </style>
  <body>
    <div></div>
    <div id="box"></div>
    <div></div>
  </body>
~~~
![image](https://user-images.githubusercontent.com/58898466/133399094-84d5a1c0-595c-4ac3-bde1-346653728337.png)

* 일반적인 문서 흐름을 제거하고, 가장 가까운 위치의 부모 요소에 대해 상대적으로 배치한다.
* 상하좌우 값을 입력하면 absolute 요소는 조상 중에서 position이 static이 아닌 요소를 찾아 기준점을 삼고, 없으면 body 태그 기준으로 삼는다.
* 둥둥 떠다니는 것 처럼 보여진다.
