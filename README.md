<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>디지털 명함</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
      background: #fff;
      color: #333;
    }
    a {
      color: inherit;
      text-decoration: none;
    }
    .container {
      max-width: 1000px;
      margin: 40px auto;
      padding: 30px 20px;
      animation: fadeInUp 0.8s ease-out forwards;
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(50px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .logo {
      width: 150px;
      margin: 20px auto 10px;
      display: block;
    }
    h1 {
      font-size: 28px;
      margin: 10px 0;
    }
    .survey-list {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 16px;
      margin-top: 25px;
    }
    .survey-card {
      background: #fafafa;
      padding: 16px 14px;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.04);
      min-height: 150px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
    .survey-card h3 { margin-bottom: 8px; font-weight: bold; }
    .survey-card p { margin: 4px 0; line-height: 1.5; font-size: 15px; }
    .highlight { color: #f0961f; font-weight: bold; }
    .black-bold { font-weight: bold; color: #000; }

    .board-container {
      max-width: 1000px;
      margin: 30px auto 20px;
      background: #f9f9f9;
      padding: 25px 20px;
      border-radius: 8px;
      color: #333;
    }
    .board-title { font-size: 20px; font-weight: bold; margin-bottom: 15px; }
    .board {
      width: 100%;
      border-collapse: collapse;
    }
    .board th, .board td {
      border-bottom: 1px solid #ccc;
      padding: 12px 10px;
      text-align: left;
    }
    .board th {
      background-color: #eee;
      font-weight: bold;
      text-align: center;
    }
    .board td:first-child {
      font-weight: bold;
      text-align: center;
      width: 100px;
    }

    .lang-btn {
      position: fixed;
      top: 20px;
      right: 20px;
      background: #f0961f;
      color: white;
      border: none;
      border-radius: 20px;
      padding: 10px 18px;
      font-weight: bold;
      cursor: pointer;
    }

    footer {
      background-color: #f5f3ef;
      padding: 30px 20px;
      text-align: center;
      font-size: 14px;
    }
    .footer-info {
      color: #000;
      margin-bottom: 20px;
    }
    .footer-info p {
      margin: 6px 0;
    }
    .family-site {
      margin-top: 10px;
    }
    .family-site select {
      padding: 6px 10px;
      font-size: 14px;
      border-radius: 5px;
    }

    @media (min-width: 768px) {
      footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
        text-align: center;
      }
      .footer-info {
        flex: 1;
        text-align: center;
        margin-bottom: 0;
      }
      .family-site {
        position: absolute;
        right: 30px;
        transform: translateY(0%);
      }
    }
  </style>
</head>
<body>
  <button class="lang-btn" onclick="toggleLang()">ENGLISH</button>

  <div class="container">
    <img src="https://i.imgur.com/QOzO5Ye.png" alt="로고" class="logo" />
    <h1 id="title">민산이네 디지털 명함</h1>
    <p id="subtitle">
      <strong class="black-bold">민산이네(MSstudio)</strong>는 <span class="highlight">공감</span>으로 함께 살아가는 세상을 꿈꾸는 콘텐츠 스튜디오입니다.
    </p>

    <div class="survey-list">
      <div class="survey-card">
        <h3 id="contact-title">연락처</h3>
        <p id="contact-phone"><strong>Tel</strong>: <a href="tel:07079385705">070-7938-5705</a></p>
        <p id="contact-email"><strong>이메일</strong>: <a href="mailto:biz@minsanine.co.kr">biz@minsanine.co.kr</a></p>
        <p id="contact-fax"><strong>팩스</strong>: 0504-284-5705</p>
      </div>
      <div class="survey-card">
        <h3 id="hour-title">영업시간</h3>
        <p id="hour-weekday"><strong>월/화/목/금</strong> 10:00 ~ 18:30</p>
        <p id="hour-wed"><strong>수요일</strong> 10:00 ~ 17:30</p>
        <p id="hour-weekend"><strong>주말 및 공휴일</strong> 휴무</p>
      </div>
      <div class="survey-card">
        <h3 id="info-title">회사정보</h3>
        <p id="company-desc"><span class="highlight">공감, 존중, 배려</span>의 가치를 기반으로 콘텐츠 생태계를 만들어갑니다.</p>
      </div>
    </div>

    <div class="board-container">
      <div class="board-title" id="board-title">개요 · 비전 · 미션</div>
      <table class="board">
        <thead>
          <tr>
            <th id="th-category">구분</th>
            <th id="th-content">내용</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td id="td-summary">개요</td>
            <td id="desc-summary">
              <strong class="black-bold">민산이네(MSstudio)</strong>는 <span class="highlight">공감</span>으로 함께 살아가는 세상을 꿈꾸는 콘텐츠 스튜디오입니다.
            </td>
          </tr>
          <tr>
            <td id="td-vision">비전</td>
            <td id="desc-vision">
              모두가 함께 즐기고 서로의 삶을 이해하는 <span class="highlight">공감의 콘텐츠 플랫폼</span>이 되는 것
            </td>
          </tr>
          <tr>
            <td id="td-mission">미션</td>
            <td id="desc-mission">
              공감 기반 콘텐츠로 세대를 연결하고 소외된 목소리를 대변합니다.
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

  <footer>
    <div class="footer-info">
      <p>민산이네(MSstudio)</p>
      <p>사업자등록번호: 842-98-01735</p>
      <p>Tel: 070-7938-5705</p>
      <p>Email: biz@minsanine.co.kr</p>
      <p>Copyright © 민산이네(MSstudio). All rights reserved.</p>
    </div>
    <div class="family-site">
      <select id="familySite" onchange="goToSite()">
        <option value="">패밀리 사이트</option>
        <option value="https://www.minsanine.co.kr">민산이네(MSstudio)</option>
        <option value="https://www.msstudio.site">민산이네 설문지</option>
        <option value="https://name.msstudio.site">민산이네 명함</option>
        <option value="https://www.minsan.me">김민산</option>
      </select>
    </div>
  </footer>

  <script>
    function goToSite() {
      const url = document.getElementById("familySite").value;
      if (url) window.open(url, "_blank");
    }

    let isEnglish = false;
    const userLang = navigator.language || navigator.userLanguage;
    if (!userLang.startsWith('ko')) {
      isEnglish = true;
      document.addEventListener('DOMContentLoaded', toggleLang);
    }

    function toggleLang() {
      isEnglish = !isEnglish;
      document.querySelector('.lang-btn').textContent = isEnglish ? '한국어' : 'ENGLISH';
      document.getElementById('title').textContent = isEnglish ? 'MSstudio Digital Card' : '민산이네 디지털 명함';
      document.getElementById('subtitle').innerHTML = isEnglish
        ? '<strong class="black-bold">MSstudio</strong> is a content studio dreaming of a world where everyone lives together with <span class="highlight">empathy</span>.'
        : '<strong class="black-bold">민산이네(MSstudio)</strong>는 <span class="highlight">공감</span>으로 함께 살아가는 세상을 꿈꾸는 콘텐츠 스튜디오입니다.';

      document.getElementById('contact-title').textContent = isEnglish ? 'Contact' : '연락처';
      document.getElementById('contact-phone').innerHTML = isEnglish ? '<strong>Tel</strong>: <a href="tel:07079385705">070-7938-5705</a>' : '<strong>Tel</strong>: <a href="tel:07079385705">070-7938-5705</a>';
      document.getElementById('contact-email').innerHTML = isEnglish ? '<strong>Email</strong>: <a href="mailto:biz@minsanine.co.kr">biz@minsanine.co.kr</a>' : '<strong>이메일</strong>: <a href="mailto:biz@minsanine.co.kr">biz@minsanine.co.kr</a>';
      document.getElementById('contact-fax').innerHTML = isEnglish ? '<strong>Fax</strong>: 0504-284-5705' : '<strong>팩스</strong>: 0504-284-5705';

      document.getElementById('hour-title').textContent = isEnglish ? 'Business Hours' : '영업시간';
      document.getElementById('hour-weekday').textContent = isEnglish ? 'Mon/Tue/Thu/Fri 10:00 ~ 18:30' : '월/화/목/금 10:00 ~ 18:30';
      document.getElementById('hour-wed').textContent = isEnglish ? 'Wednesday 10:00 ~ 17:30' : '수요일 10:00 ~ 17:30';
      document.getElementById('hour-weekend').innerHTML = isEnglish
        ? '<strong>weekends & holidays</strong> Closed' : '<strong>주말 및 공휴일</strong> 휴무';

      document.getElementById('info-title').textContent = isEnglish ? 'Company Info' : '회사정보';
      document.getElementById('company-desc').innerHTML = isEnglish
        ? 'We build a content ecosystem based on the values of <span class="highlight">empathy, respect, and consideration</span>.'
        : '<span class="highlight">공감, 존중, 배려</span>의 가치를 기반으로 콘텐츠 생태계를 만들어갑니다.';

      document.getElementById('board-title').textContent = isEnglish ? 'Overview · Vision · Mission' : '개요 · 비전 · 미션';
      document.getElementById('th-category').textContent = isEnglish ? 'Category' : '구분';
      document.getElementById('th-content').textContent = isEnglish ? 'Details' : '내용';
      document.getElementById('td-summary').textContent = isEnglish ? 'Overview' : '개요';
      document.getElementById('desc-summary').innerHTML = isEnglish
        ? '<strong class="black-bold">MSstudio</strong> is a content studio dreaming of a world where everyone lives together with <span class="highlight">empathy</span>.'
        : '<strong class="black-bold">민산이네(MSstudio)</strong>는 <span class="highlight">공감</span>으로 함께 살아가는 세상을 꿈꾸는 콘텐츠 스튜디오입니다.';

      document.getElementById('td-vision').textContent = isEnglish ? 'Vision' : '비전';
      document.getElementById('desc-vision').innerHTML = isEnglish
        ? 'To become a <span class="highlight">content platform of empathy</span> where everyone enjoys together and understands each other’s lives.'
        : '모두가 함께 즐기고 서로의 삶을 이해하는 <span class="highlight">공감의 콘텐츠 플랫폼</span>이 되는 것';

      document.getElementById('td-mission').textContent = isEnglish ? 'Mission' : '미션';
      document.getElementById('desc-mission').textContent = isEnglish
        ? 'To connect generations through empathy-based content and amplify the voices of the underrepresented.'
        : '공감 기반 콘텐츠로 세대를 연결하고 소외된 목소리를 대변합니다.';
    }
  </script>
</body>
</html>
