# literate-memory
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>time paradox</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      background: #e8f5ff;
      font-family: 'Noto Sans KR', sans-serif;
      margin: 0;
      padding: 2rem;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      min-height: 100vh;
    }

    .container {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 1.5rem;
      width: 100%;
      max-width: 1200px;
    }

    .left {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
    }

    .right {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1.5rem;
    }

    .window {
      background: #ffffff;
      border: 1px solid #b3e0f5;
      border-radius: 10px;
      box-shadow: 0 8px 20px rgba(0, 140, 190, 0.08);
      display: flex;
      flex-direction: column;
      overflow: hidden;
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .window:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 30px rgba(0, 140, 190, 0.15);
    }

    .header-bar {
      background: #cceeff;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.5rem 0.8rem;
      border-bottom: 1px solid #a3d6eb;
    }

    .window-controls {
      display: flex;
      align-items: center;
    }

    .heart-icon {
      width: 14px;
      height: 14px;
      background-color: white;
      -webkit-mask: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="%23000000"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 6 4 4 6.5 4c1.74 0 3.41 1.01 4.13 2.44h1.74C14.09 5.01 15.76 4 17.5 4 20 4 22 6 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>') no-repeat center;
      mask: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="%23000000"><path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 6 4 4 6.5 4c1.74 0 3.41 1.01 4.13 2.44h1.74C14.09 5.01 15.76 4 17.5 4 20 4 22 6 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z"/></svg>') no-repeat center;
      -webkit-mask-size: contain;
      mask-size: contain;
    }

    .header-title {
      font-weight: bold;
      color: #007aa8;
      font-size: 0.9rem;
    }

    .content {
      padding: 1rem;
      overflow-y: auto;
      font-size: 0.9rem;
      line-height: 1.5;
      color: #333;
    }

    .avatar {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      object-fit: cover;
      display: block;
      margin: 0 auto;
    }

    .main-name {
      text-align: center;
      font-size: 2rem;
      font-weight: 700;
      color: #0099cc;
      margin-top: 1rem;
    }

    .alias {
      text-align: center;
      font-size: 0.9rem;
      color: #777;
      margin-bottom: 1rem;
    }

    .bottom-image {
      text-align: center;
      margin-top: 1rem;
    }

    .bottom-image img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
    }

    .image-credit {
      font-size: 0.75rem;
      color: #888;
      margin-top: 0.3rem;
    }

    ul {
      list-style: none;
      padding-left: 0;
      margin: 0.5rem 0;
    }

    ul li {
      position: relative;
      padding-left: 1rem;
      margin-bottom: 0.3rem;
    }

    ul li::before {
      content: "";
      position: absolute;
      left: 0;
      top: 0.4em;
      width: 6px;
      height: 6px;
      background-color: #33aadd;
      border-radius: 50%;
    }

    .note {
      font-size: 0.8rem;
      color: #888;
      margin-top: 0.3rem;
    }

    .ng-section {
      background: #d3edfa;
    }

    a {
      color: #0077aa;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="left">
      <div class="window">
        <div class="header-bar">
          <div class="window-controls">
            <div class="heart-icon"></div>
          </div>
          <div class="header-title">Profile</div>
        </div>
        <div class="content">
          <img class="avatar" src="img/낫또님2.png" alt="아바타">
          <div class="main-name">물곡</div>
          <div class="alias">무기력, 물곡, 빵, 상자 등등... 편하신 대로 불러주세요</div>
          <div class="bottom-image">
            <img src="img/염소탕후루님 투명.png" alt="관련 이미지">
            <div class="image-credit">©염소탕후루님</a></div>
          </div>
        </div>
      </div>
    </div>
    <div class="right">
      <!-- 기본 정보 -->
      <div class="window">
        <div class="header-bar">
          <div class="window-controls"><div class="heart-icon"></div></div>
          <div class="header-title">기본 정보</div>
        </div>
        <div class="content">
          <ul>
            <li>비계 인용 多</li>
            <li>저급한 말, 원색적인 비난 多</li>
            <li>마작: <a href="https://twitter.com/054702_" target="_blank">@054702_</a></li>
          </ul>
        </div>
      </div>

      <!-- NG -->
      <div class="window ng-section">
        <div class="header-bar">
          <div class="window-controls"><div class="heart-icon"></div></div>
          <div class="header-title">NG / 불호</div>
        </div>
        <div class="content">
          <ul>
            <li>남자</li>
            <li>리키치 + 도이 CP</li>
            <li>타컾 / 리버스 (2D)</li>
          </ul>
          <div class="note">불호 발언 많습니다. 팔로우 재고 부탁드립니다.</div>
          <div class="note">트친이 판다면 단어 뮤트/흐린눈 가능</div>
        </div>
      </div>

      <!-- 좋아하는 것 -->
      <div class="window">
        <div class="header-bar">
          <div class="window-controls"><div class="heart-icon"></div></div>
          <div class="header-title">♥ 좋아하는 것</div>
        </div>
        <div class="content">
          <ul>
            <li>흡툭죽: 사교우</li>
            <li>은혼: 야마자키 & 사가루 / 야마히지</li>
            <li>사이키 쿠스오: 토리사이토리</li>
            <li>프로세카: 츠카에무, 카이미쿠, 카이메이</li>
            <li>혈계전선: 재프레오재프</li>
            <li>닌타마: 리코마(메인), 도이손</li>
          </ul>
          <div class="note">기타: 따로 안 적은 장르는 올캐러</div>
        </div>
      </div>

      <!-- 2.5D -->
      <div class="window">
        <div class="header-bar">
          <div class="window-controls"><div class="heart-icon"></div></div>
          <div class="header-title">2.5D</div>
        </div>
        <div class="content">
          <p>우고 언급 多 (에라이보다는 우고 개인 활동 위주)</p>
          <div class="note">에라이 팀 자체를 좋아하는 건 아닙니다</div>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
