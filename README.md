<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>Scentory</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #faf0e5;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }
        header {
            background-color: #fccaca;
            color: #fff;
            padding: 10px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
            padding: 10px 20px;
            transition: height 0.3s ease;
            position: relative;
        }

        header h1 {
            margin-top: 0;
        }

        header h1 a {
            color: #fff;
            text-decoration: none;
        }

        .header-form {
            flex: 1;
            display: flex;
            justify-content: center;
            margin-left: -130px;
            margin-top: 15px;
        }

        .search-wrapper {
            display: flex;
            align-items: center;
            position: relative;
            width: 100%;
            max-width: 300px;
        }

        .search-box {
            padding: 8px 40px 8px 10px;
            border-radius: 50px;
            border: 1px solid #949494;
            font-size: 12px;
            width: 100%;
            background-color: transparent;
        }

        .search-wrapper .search-icon {
            position: absolute;
            top: 50%;
            right: 10px;
            transform: translateY(-50%);
            cursor: pointer;
            background-color: transparent;
            border: none;
            width: 20px;
            height: 20px;
            padding: 0;
        }

        .search-wrapper .search-icon img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

        /* 헤더 이미지 */
        .ejqhrl {
            width: 34px;
            height: auto;
            margin-bottom: 20px;
        }

        nav {
            background-color: #fccaca;
            padding: 10px 0;
        }

        nav ul {
            list-style-type: none;
            padding: 0;
            text-align: center;
            margin: 0;
        }

        nav ul li {
            display: inline-block;
            margin: 0 15px;
            position: relative;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-size: 18px;
        }

        nav ul li a:hover {
            font-weight: bold;
        }

        /* 서브 메뉴 */
        .sub-menu {
            display: none;
            position: absolute;
            top: 30px;
            left: -15px;
            background-color: rgba(255, 192, 192, 0.8);
            padding: 5px 0;
            list-style-type: none;
            width: 100px;
            text-align: center;
            font-size: 16px;
            z-index: 20;
        }

        .sub-menu li {
            display: block;
            margin: 0;
        }

        .sub-menu li a {
            color: #fff;
            text-decoration: none;
            padding: 6px 10px;
            display: block;
        }

        .sub-menu li a:hover {
            background-color: transparent;
        }

        /* 메뉴 hover 시 서브 메뉴 보이기 */
        nav ul li:hover .sub-menu {
            display: block;
        }

        footer {
            background-color: #fccaca;
            color: #fff;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        .image-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin-top: 30px;
            flex-grow: 1;
        }

        .image-container img {
            width: 100%;
            height: 100%;
            max-width: 250px;
            margin: 10px 0;
            object-fit: cover;
        }

        .bold-text {
            font-weight: bold;
        }

        /* 화면을 줄였을 때 header의 height을 35px로 변경 */
        @media (max-width: 768px) {
            header {
                height: 40px;
                padding: 5px 20px;
            }
            header h1 {
                margin-top: 26px;
                line-height: 1.2;
            }

            .search-wrapper {
                display: none;
            }

            nav ul li a {
                display: none;
            }
        }
    </style>
</head>
<body>
  <header>
      <h1><a href="file:///C:/Users/k9952/OneDrive/%EB%B0%94%ED%83%95%20%ED%99%94%EB%A9%B4/%EC%B2%AB%ED%99%94%EB%A9%B4.html">Scentory</a></h1>
      
      <div class="header-form">
          <div class="search-wrapper">
              <input class="search-box" id="search-input" type="text" placeholder="검색어를 입력해주세요." name="query">
              <button class="search-icon" id="search-btn">
                  <img src="search_transparent.png" alt="검색 아이콘">
              </button>
          </div>
      </div>

      <!-- 헤더 이미지 추가 -->
      <img class="ejqhrl" src="ejqhrl.png" alt="이미지">
  </header>

  <nav>
      <ul>
          <li class="menu-item" id="all-products">
              <!-- 전체상품 메뉴를 클릭하면 새 파일로 이동 -->
              <a href="file:///C:/Users/k9952/OneDrive/%EB%B0%94%ED%83%95%20%ED%99%94%EB%A9%B4/%EC%A0%84%EC%B2%B4%EC%83%81%ED%92%88.html">전체상품</a>
              <!-- 서브 메뉴 삭제 -->
          </li>
          <li class="menu-item" id="skincare-item">
              <a href="#">스킨케어</a>
              <ul class="sub-menu">
                  <li><a href="#">스킨</a></li>
                  <li><a href="#">토너</a></li>
                  <li><a href="#">로션</a></li>
              </ul>
          </li>
          <li class="menu-item" id="makeup-item">
              <a href="#">메이크업</a>
              <ul class="sub-menu">
                  <li><a href="#">파운데이션</a></li>
                  <li><a href="#">립스틱</a></li>
              </ul>
          </li>
          <li class="menu-item" id="haircare-item">
              <a href="#">헤어케어</a>
              <ul class="sub-menu">
                  <li><a href="#">샴푸</a></li>
                  <li><a href="#">컨디셔너</a></li>
              </ul>
          </li>
          <li class="menu-item" id="perfume-item">
              <a href="#">퍼퓸</a>
              <!-- 서브 메뉴 제거 -->
          </li>
          <li class="menu-item" id="other-item">
              <a href="#">기타</a>
              <!-- 서브 메뉴 제거 -->
          </li>
      </ul>
  </nav>

  <main>
      <section style="text-align: center; margin-top: 40px;">
          <h2>Best</h2>
          <hr style="border: 1px solid #fccaca; width: 60%; margin: 20px auto;">
      </section>
  
      <section class="image-container">
          <div class="image-item">
              <img src="img.jpg" alt="Best Product 1">
              <div class="bold-text">제품 1</div>
              <div>이 제품은 뛰어난 성능을 제공합니다.</div>
          </div>
          <div class="image-item">
              <img src="img.jpg" alt="Best Product 2">
              <div class="bold-text">제품 2</div>
              <div>이 제품은 뛰어난 성능을 제공합니다.</div>
          </div>
          <div class="image-item">
              <img src="img.jpg" alt="Best Product 3">
              <div class="bold-text">제품 3</div>
              <div>이 제품은 뛰어난 성능을 제공합니다.</div>
          </div>
          <div class="image-item">
              <img src="img.jpg" alt="Best Product 4">
              <div class="bold-text">제품 4</div>
              <div>이 제품은 뛰어난 성능을 제공합니다.</div>
          </div>
      </section>
  </main>

  <footer>
      <p>&copy; 2024 Scentory. All rights reserved.</p>
  </footer>

</body>
</html>
