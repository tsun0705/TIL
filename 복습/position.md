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
* position이 static (기본값)이 아니면 상하좌우로 이동이 가능하다.
* top: 50px로 지정할 경우 자기 자신의 기준으로 위에서 아래로 50px 만큼 이동한다.  
* 음수 값도 사용이 가능하다. 

![image](https://user-images.githubusercontent.com/58898466/133396685-6c566f2b-bb11-4bec-8e36-52b839f8bd42.png)
