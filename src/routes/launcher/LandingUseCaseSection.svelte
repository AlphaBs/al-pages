<section id="section-usecase" class="section">
  <p class="section-3-title">포트폴리오</p>
  <div class="section-3-subtitle">
    <p>5년간 120건 이상의 런처 개발</p>
    <p>국내외 대규모 모드 서버 런처, 유튜버/스트리머 컨텐츠용 런처까지</p>
  </div>
  <div class="section-content">
    <enhanced:img src="$lib/assets/1.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/2.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/3.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/4.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/5.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/6.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/7.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/8.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/9.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/10.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/11.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/12.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/13.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/14.png" alt="examples" class="section-image" />
    <enhanced:img src="$lib/assets/15.png" alt="examples" class="section-image" />
  </div>
  <a
  href="https://cafe.naver.com/ArticleList.nhn?search.clubid=29270508&search.menuid=14&search.boardtype=I"
  target="_blank"
>
  모든 포트폴리오 보러가기
</a>
</section>

<style>
  .section {
    display: flex;
    flex-direction: column;
    color: white;
    align-items: center;
    background-color: #111827;
    padding-top: 128px;
    padding-bottom: 128px;
  }

  .section-3-title {
    font-size: 2rem;
    font-weight: bold;
    text-align: center;
    margin-bottom: 1.5rem;
  }

  .section-3-subtitle {
    font-size: 1.125rem;
    text-align: center;
    color: #9ca3af;
    line-height: 160%;
  }

  a {
    font-size: 1.2rem;
    text-align: center;
    color: #9ca3af;
    line-height: 160%;
  }

  .section-content {
    margin-top: 5rem;
    margin-bottom: 64px;
    width: 90%;
    max-width: 1400px;
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 equal columns */
    gap: 30px; /* space between grid items */
  }

  .section-image {
    width: 100%;
    height: auto; /* maintain aspect ratio */
    object-fit: cover; /* ensure images cover the grid cell */
  }

  @media (max-width: 768px) { /* Adjust the max-width as needed for your mobile breakpoint */
    .section-content {
      grid-template-columns: 1fr; /* 1 column for mobile */
    }
  }
</style>
