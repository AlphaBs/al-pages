<script>
  import updateIconUrl from "$lib/assets/update.svg";
  import thunderIconUrl from "$lib/assets/thunder.svg";
  import settingIconUrl from "$lib/assets/setting.svg";
  import securityIconUrl from "$lib/assets/security.svg";
  import usersIconUrl from "$lib/assets/users.svg";
  import paletteIconUrl from "$lib/assets/palette.svg";

  const features = [
    {
      image: updateIconUrl,
      alt: "아이콘",
      title: "모드 설치",
      subtitle: "모든 게임 파일을 자동으로 설치합니다",
      content: `포지/패브릭, 모드, 리소스팩, 옵션, 등등<br>
                설치할 파일은 실시간 교체 가능합니다.`,
    },
    {
      image: thunderIconUrl,
      alt: "아이콘",
      title: "서버 접속",
      subtitle: "게임 실행 즉시 서버로 접속합니다",
      content: `더 이상 서버 주소를 유저들에게 알려줄 필요가 없습니다.`,
    },
    {
      image: settingIconUrl,
      alt: "아이콘",
      title: "게임 설정",
      subtitle: "모든 설정을 미리 원하는 대로 수정할 수 있습니다",
      content: `리소스팩, 쉐이더팩, 언어, 각종 그래픽 설정 등등...`,
    },
    {
      image: paletteIconUrl,
      alt: "아이콘",
      title: "맞춤 기능",
      content: `공지사항 표시, 서버 상태 (ON/OFF) 표시, 디스코드 바로가기 버튼 등등...<br>
                원하는 어떤 기능이든 추가 가능합니다.`,
    },
    {
      image: usersIconUrl,
      alt: "아이콘",
      title: "유저별 설정",
      content: `유저마다 어떤 파일을 설치할 지, 어떤 서버를 접속할 지 설정할 수 있습니다.<br>
                허가하지 않은 유저는 게임 파일 설치와 서버 접속을 런처에서 차단할 수 있습니다.`,
    },
    {
      image: securityIconUrl,
      alt: "아이콘",
      title: "치트 방지",
      content: `설정한 모드 이외의 추가적인 모드 설치를 차단하고, 런처로만 서버에 접속할 수 있습니다.`,
    },
  ];
</script>

<section id="section-keyfeature" class="section">
  <div class="section-content">
    {#each features as feature}
      <div class="section-item">
        <img class="section-item-image" src={feature.image} alt={feature.alt}>
        <p class="section-item-title">{feature.title}</p>
        {#if feature.subtitle}
          <p class="section-item-subtitle">{feature.subtitle}</p>
        {/if}
        <p class="section-item-content">
          {@html feature.content}
        </p>
      </div>
    {/each}
  </div>
</section>

<style>
  .section {
    margin-bottom: 128px;
    padding-left: 5%;
    padding-right: 5%;
  }

  .section-content {
    justify-self: center;
    max-width: 1400px;
    margin-top: 96px;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 2rem;
    row-gap: 6rem;
  }

  .section-item {
    display: flex;
    justify-self: stretch;
    flex-direction: column;
    line-height: 1.5;
  }

  .section-item-image {
    width: 42px;
    height: 42px;
    margin-bottom: 1.5rem;
  }

  .section-item-title {
    font-size: 1.5rem;
    font-weight: bold;
    letter-spacing: 0px;
    margin-bottom: 1rem;
  }

  .section-item-subtitle {
    color: black;
    font-weight: bold;
  }

  .section-item-content {
    color: black;
  }

  /* Medium screens: 2x2 grid */
  @media (max-width: 1024px) {
    .section-content {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  /* Mobile screens: 4x1 grid */
  @media (max-width: 600px) {
    .section-content {
      grid-template-columns: 1fr;
    }
  }
</style>
