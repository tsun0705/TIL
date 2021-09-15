# 2021-09-11 Today I Learned
## 1번
~~~
.content {
  width: 100px;
  height: 100px;
  margin: 10px 15px 20px 15px;
  padding: 10px;
  border: 1px black;
}
~~~

## ✔ 2번
~~~
<style>
    .wrap {
      width: 420px;
      margin: 0 auto;
    }
    nav {
      height: 64px;
      padding: 0 16px;
      background-color: white;
      border-bottom: 1px solid rgb(231, 231, 231);
    }
    .title {
      display: inline-block;
      width: 200px;
      line-height: 64px;
      font-size: 24px;
      font-weight: bold;
    }
    .menu {
      height: 100%;
      float: right;
    }
    .menu > span {
      line-height: 64px;
      margin: 0 10px;
    }
</style>

<nav>
    <span class="title">네카라쿠배</span>
    <span class="menu">
      <span>로그인</span>
      <span>회원가입</span>
      <span>마이페이지</span>
    </span>
</nav>
~~~

## ✔ 3번
~~~
<!DOCTYPE html>
<html>
  <head>
    <link href="HTML_CSS_모범답안_02.css" rel="stylesheet" />
  </head>
  <style>
    .wrapper {
      display: grid;
      grid-gap: 10px;
      grid-template-columns: repeat(3, 1fr);
      width: 400px;
    }

    .card {
      width: 100px;
      height: 100px;
      border-radius: 10px;
      border: 1px solid black;
      margin: 10px;
    }

    .card > img {
      width: 100%;
      height: 100%;
      border-radius: 10px;
    }
    .wrapper {
      display: flex;
      flex-wrap: wrap;
      width: 400px;
    }

    .card {
      width: 100px;
      height: 100px;
      border-radius: 10px;
      border: 1px solid black;
      margin: 10px;
    }

    .card > img {
      width: 100%;
      height: 100%;
      border-radius: 10px;
    }
  </style>
  <body>
    <div class="wrapper">
      <div class="card">
        <img
          src="https://play-lh.googleusercontent.com/ccWDU4A7fX1R24v-vvT480ySh26AYp97g1VrIB_FIdjRcuQB2JP2WdY7h_wVVAeSpg=s180-rw"
        />
      </div>
      <div class="card">
        <img
          src="https://play-lh.googleusercontent.com/h9jWMwqb-h9hjP4THqrJ50eIwPekjv7QPmTpA85gFQ10PjV02CoGAcYLLptqd19Sa1iJ=s180-rw"
        />
      </div>
      <div class="card">
        <img
          src="https://play-lh.googleusercontent.com/Ob9Ys8yKMeyKzZvl3cB9JNSTui1lJwjSKD60IVYnlvU2DsahysGENJE-txiRIW9_72Vd=s180-rw"
        />
      </div>
      <div class="card">
        <img
          src="https://play-lh.googleusercontent.com/PCpXdqvUWfCW1mXhH1Y_98yBpgsWxuTSTofy3NGMo9yBTATDyzVkqU580bfSln50bFU=s180-rw
    "
        />
      </div>
      <div class="card">
        <img
          src="https://play-lh.googleusercontent.com/lMoItBgdPPVDJsNOVtP26EKHePkwBg-PkuY9NOrc-fumRtTFP4XhpUNk_22syN4Datc=s180-rw"
        />
      </div>
      <div class="card">
        <img
          src="https://play-lh.googleusercontent.com/eN0IexSzxpUDMfFtm-OyM-nNs44Y74Q3k51bxAMhTvrTnuA4OGnTi_fodN4cl-XxDQc=s180-rw"
        />
      </div>
      <div class="card">
        <img
          src="https://play-lh.googleusercontent.com/z5nin1RdQ4UZhv6fa1FNG7VE33imGqPgC4kKZIUjgf_up7E-Pj3AaojlMPwNNXaeGA=s180-rw"
        />
      </div>
    </div>
  </body>
</html>
~~~
