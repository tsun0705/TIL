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
  </head>
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

## 4번
~~~
<!DOCTYPE html>
<html>
  <head>
      <style>
    html,
    body {
      padding: 0;
      margin: 0;
    }

    main {
      width: calc(100% - 300px);
      float: left;
    }

    .main-title {
      background: blue;
      padding: 16px;
      color: white;
    }

    .main-content {
      padding: 24px;
      line-height: 1.5;
    }

    aside {
      width: 300px;
      float: right;
    }

    .aside-content {
      padding: 16px;
    }

    .aside-list > li {
      line-height: 36px;
      font-weight: bold;
      border-bottom: 1px solid;
    }

    @media only screen and (max-width: 720px) {
      main {
        width: 100vw;
        float: none;
      }

      aside {
        width: 100vw;
        float: none;
      }
    }
  </style>
  </head>

  <body>
    <main>
      <div class="main-title">
        <h1>삼성전자</h1>
        <span>종목코드: 005930</span>
      </div>
      <div class="main-content">
        <h3>회사소개</h3>
        <p>
          한국 및 CE, IM부문 해외 9개 지역총괄과 DS부문 해외 5개 지역총괄,
          Harman 등 241개의 종속기업으로 구성된 글로벌 전자기업임. 세트사업에는
          TV, 냉장고 등을 생산하는 CE부문과 스마트폰, 네트워크시스템, 컴퓨터
          등을 생산하는 IM부문이 있음. 부품사업(DS부문)에서는 D램, 낸드 플래쉬,
          모바일AP 등의 제품을 생산하는 반도체 사업과 TFT-LCD 및 OLED 디스플레이
          패널을 생산하는 DP사업으로 구성됨.
        </p>
      </div>
    </main>
    <aside>
      <div class="aside-content">
        <h3>시가총액 순위</h3>
        <ol class="aside-list">
          <li>삼성전자</li>
          <li>SK하이닉스</li>
          <li>NAVER</li>
          <li>카카오</li>
          <li>삼성바이오로직스</li>
          <li>삼성전자우</li>
          <li>삼성SDI</li>
          <li>LG화학</li>
          <li>현대차</li>
          <li>셀트리온</li>
        </ol>
      </div>
    </aside>
  </body>
</html>
~~~

## ✔ 5번
~~~
<!DOCTYPE html>
<html>
  <head>
    <style>
      .comment-list {
        max-width: 360px;
        margin: 0 auto;
      }

      .comment-container {
        padding: 18px 0;
        border-bottom: 1px solid #d3d3d3;
      }

      .title {
        font-size: 2em;
        font-weight: bold;
        margin: 0 auto;
        padding-bottom: 10px;
        border-bottom: 2px solid black;
      }

      .title > .count {
        color: #06a27d;
      }

      .date {
        color: #939393;
      }

      .content {
        line-height: 1.5;
        word-break: keep-all;
      }
    </style>
  </head>
  <body>
    <div class="comment-list">
      <div class="title">댓글 <span class="count">923</span></div>
      <div class="comment-container">
        <div>
          <b>정*석</b>
        </div>
        <span class="date">2021.03.16</span>
        <p class="content">
          1차 합격하고 실제 네이버간 본인입니다 ㅎㅎ 저는 전공자긴 하지만 학점은
          3.0 아래고 나이도 30세가 넘었습니다. 제가 가진건 끈기 단 하나였어요.
          목표를 잡고 일부는 성취하고, 일부는 실패하더라도 전략을 수정하여 계속
          도전해 결국엔 목표를 이루려고 하였습니다. '이쯤 했으면 됐다' 생각할 때
          포기하지 마시고 한발자국씩 더 나아가보세요. 분명히 좋은 결과가
          있을거에요! 화이팅입니다.
        </p>
      </div>
      <div class="comment-container">
        <div>
          <b>한*현</b>
        </div>
        <span class="date">2021.03.21</span>
        <p class="content">
          포기하기마시고 즐거운 개발하셔서 꽃길 걸을 수 있길 바랍니다!
        </p>
      </div>
      <div class="comment-container">
        <div>
          <b>이*자</b>
        </div>
        <span class="date">2021.03.21</span>
        <p class="content">
          능력있고 열심히 하는 분들에게 좋은 결과 있기를 바랍니다. 항상 좋은
          일만 가득하셨으면 좋겠습니다. 멋진 앞날을 기원하겠습니다.
        </p>
      </div>
      <div class="comment-container">
        <div>
          <b>이*윤</b>
        </div>
        <span class="date">2021.03.21</span>
        <p class="content">
          네카라쿠배 1기 모집 글을 본게 엊그제 같은데 벌써 최종 15명이네요. 꼭
          네카라쿠배 가셔서 즐겁게 개발일 하시면 좋겠습니다! 앞으로의 길을
          응원해요. 저도 2기 지원할게요~!!
        </p>
      </div>
      <div class="comment-container">
        <div>
          <b>박*호</b>
        </div>
        <span class="date">2021.03.21</span>
        <p class="content">
          최종 15분이 멋진 길을 이뤄주시면 다음에 시도하시는 분들도 앞선
          지원자들을 보고 더욱 열심히 공부를 하며 동기부여가 될거라고
          생각합니다. 최선을 다하신것에 보답이라고 생각하시면서 꽃길만 걸으시기
          바랍ㄴ디ㅏ.
        </p>
      </div>
      <div class="comment-container">
        <div>
          <b>김*성</b>
        </div>
        <span class="date">2021.03.21</span>
        <p class="content">존버필승입니다 화이팅하십쇼</p>
      </div>
    </div>
  </body>
</html>
~~~

~~~
