<script>
  import checkIconUrl from "$lib/assets/check-fill.svg";
  import plusIconUrl from "$lib/assets/icon-plus.svg";

  const features1 = [
    `정품 마인크래프트 계정으로 로그인 <span style="color: #e6194b;">(복돌 런처는 개발하지 않습니다!)</span>`,
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
    `유저별로 설치할 파일과 접속할 서버 지정`,
  ];

  const features3 = [
    `치트 방지 - 클라이언트 수정 방지 및 서버 접속 차단`,
    `서버 DB, 플러그인 연동, 외부 API 연동`,
  ];
</script>

<section id="section-4" class="section-4">
  <p class="section-title">기능 목록</p>
  <div class="section-4-content shadow">
    {#each features1 as feature}
      <div class="section-4-item">
        <img src={checkIconUrl} alt="check icon" class="section-4-item-icon" />
        <p>
          {@html feature}
        </p>
      </div>
    {/each}
    {#each features2 as feature}
      <div class="section-4-item">
        <img src={plusIconUrl} alt="plus icon" class="section-4-item-icon" />
        <p>
          {@html feature}
        </p>
      </div>
    {/each}
    {#each features3 as feature}
      <div class="section-4-item">
        <img src={plusIconUrl} alt="check icon" class="section-4-item-icon" />
        <p>
          {@html feature}
          <span class="section-plus">*</span>
        </p>
      </div>
    {/each}
  </div>
  <p class="section-footer">목록에 없더라도 필요한 모든 기능 개발 가능합니다</p>
</section>

<style>
  .section-4 {
    background-color: #f9fafb;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 96px;
    padding-bottom: 96px;
  }

  .section-title {
    font-size: 2rem;
    font-weight: bold;
    text-align: center;
    margin-bottom: 76px;
  }

  .section-4-content {
    width: 90%;
    max-width: 800px;
    border-radius: 8px;
    padding-top: 2%;
    padding-bottom: 2%;
    background: white;
  }

  .section-4-item {
    margin: 24px;
    display: flex;
    font-size: 1.1rem;
    line-height: 1.25rem;
    letter-spacing: 0px;
    align-items: center;
  }

  .section-4-item-icon {
    height: 1.25rem; /* Match the line-height of the text */
    margin-right: 8px;
  }

  .section-plus {
    font-size: 1.125rem;
    font-weight: normal;
  }

  .section-footer {
    margin-top: 40px;
    font-size: 1.2rem;
    font-weight: bold;
    text-align: center;
    line-height: 160%;
  }
</style>
