<script>
  import checkIconUrl from "$lib/assets/check-fill.svg";

  const features1 = [
    `정품 마인크래프트 계정으로 로그인 <span style="color: red;">(복돌 런처는 개발하지 않습니다!)</span>`,
    `바닐라, 포지, 패브릭 등등 모든 마인크래프트 버전 설치 및 실행`,
    `모드, 리소스팩, 쉐이더팩, 설정파일 등등 모든 파일 설치 및 자동 업데이트`,
    `서버 자동 접속`,
    `자바 설치`,
    `자바 설정 (XMX, XMS 램 설정, JVM 인수 설정 등등)`,
    `실행 설정 (전체화면으로 실행, 창 크기 설정)`,
    `디스코드, 카페 등등 커뮤니티 링크 바로가기`,
  ];

  const features2 = [
    `공지사항 표시`,
    `게임 설정 (리소스팩 설정, 그래픽 설정, 비디오 설정, 언어 설정, 키 설정 등등)`,
    `서버 상태 (ON/OFF, 플레이어 수, Motd) 실시간 표시`,
    `설정한 유저만 런처 사용 가능하도록 / 설정한 유저는 런처 사용 차단`,
  ];

  const features3 = [
    `​전용 런처로만 서버 접속 가능하도록 보안 설정`,
    `서버 DB, 플러그인 연동, 외부 API 연동`,
    `필요한 모든 기능 개발 가능합니다`,
  ];
</script>

<section id="section-4" class="section-4">
  <div class="section-4-title">
    <p>기능 목록</p>
  </div>
  <div class="section-4-content shadow">
    <p class="feature-title">기본 포함 기능</p>
    {#each features1 as feature}
      <div class="section-4-item">
        <img src={checkIconUrl} alt="check icon" class="section-4-item-icon" />
        <p>
          {@html feature}
        </p>
      </div>
    {/each}
    <p class="feature-title">무료 추가 기능</p>
    {#each features2 as feature}
      <div class="section-4-item">
        <img src={checkIconUrl} alt="check icon" class="section-4-item-icon" />
        <p>
          {@html feature}
        </p>
      </div>
    {/each}
    <p class="feature-title">유료 추가 기능</p>
    {#each features3 as feature}
      <div class="section-4-item">
        <img src={checkIconUrl} alt="check icon" class="section-4-item-icon" />
        <p>
          {@html feature}
        </p>
      </div>
    {/each}
  </div>
</section>

<style>
  .section-4 {
    background-color: #f6eee3;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .section-4-title {
    font-size: 30px;
    font-weight: bold;
    text-align: center;
    margin-top: 96px;
    margin-bottom: 32px;
  }

  .section-4-content {
    width: 90%;
    max-width: 800px;
    margin-bottom: 64px;
    border-radius: 8px;
    padding-top: 24px;
    padding-bottom: 24px;
    background: white;
  }

  .feature-title {
    text-align: left;
    font-weight: bold;
    text-decoration: underline;
    margin-left: 24px;
  }

  .section-4-item {
    margin: 24px;
    display: flex;
    font-size: 16px;
    font-weight: 600;
    line-height: 24px;
    letter-spacing: 0px;
  }

  .section-4-item-icon {
    margin-right: 8px;
  }
</style>
