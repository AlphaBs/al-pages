<script>
  import feature1ImageUrl from "$lib/assets/feature-1.png";
  import feature2ImageUrl from "$lib/assets/feature-2.png";
  import feature3ImageUrl from "$lib/assets/feature-3.png";
  import feature4ImageUrl from "$lib/assets/feature-4.png";

  const features = [
    {
      image: feature1ImageUrl,
      alt: "모드 설치",
      title: "모드 설치",
      content: `<strong>서버 접속에 필요한 모든 파일을 자동으로 설치합니다</strong><br>
                포지/패브릭, 모드, 리소스팩 설치와 옵션 세팅...<br>
                서버에 접속하기 위해 복잡하고 어려운 과정을 거쳐야만 했었습니다.<br>
                모든 파일은 관리자가 직접 언제든지 원하는 파일로 실시간 교체 가능합니다.`
    },
    {
      image: feature2ImageUrl,
      alt: "서버 접속",
      title: "서버 접속",
      content: `<strong>게임 실행 즉시 설정한 서버로 접속합니다</strong><br>
                멀티플레이 서버 목록에 서버를 자동으로 추가합니다.<br>
                더 이상 서버 주소를 유저들에게 알려줄 필요가 없습니다.`
    },
    {
      image: feature3ImageUrl,
      alt: "게임 설정",
      title: "게임 설정",
      content: `리소스팩 적용, 쉐이더팩 적용, 언어 설정, 키 설정, 각종 그래픽 설정 등등...<br>
                마인크래프트의 설정도 원하는 대로 적용할 수 있습니다.`
    },
    {
      image: feature4ImageUrl,
      alt: "오잉",
      title: "맞춤 기능",
      content: `공지사항 표시, 서버 상태 (ON/OFF) 표시, 디스코드 바로가기 버튼 등등...<br>
                서버 운영을 위한 다양한 기능들이 있습니다.`
    },
  ];
</script>

<section id="section-keyfeature" class="section">
  <div class="section-content">
    {#each features as feature, index}
    <div class="{index % 2 === 0 ? "section-item" : "section-reverse-item"}">
      <div class="section-item-image">
        <img src="{feature.image}" alt="{feature.alt}" class="section-item-image shadow" />
      </div>
      <div class="section-item-content">
        <p class="section-item-title">{feature.title}</p>
        <p>
          {@html feature.content}
        </p>
      </div>
    </div>
    {/each}
  </div>
</section>

<style>
.section {
  width: 100%;
  margin-bottom: 64px;
}

.section-content {
  width: 100%;
  max-width: 1400px;
  margin-top: 96px;
  display: flex;
  flex-direction: column;
  justify-self: center;
  gap: 128px;
}

.section-item {
  display: flex;
  align-items: center;
  justify-self: stretch;
  flex-direction: row;
  gap: 64px;
  margin-left: 96px;
  margin-right: 96px;
}

.section-reverse-item {
  display: flex;
  align-items: center;
  justify-self: stretch;
  flex-direction: row-reverse;
  gap: 64px;
  margin-left: 96px;
  margin-right: 96px;
}

.section-item-image {
  width: 60vw;
  max-width: 600px;
  min-width: 300px;
  aspect-ratio: 5 / 3;
  border-radius: 8px;
  overflow: hidden;
}

.section-item-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top;
}

.section-item-title {
  font-size: 30px;
  font-weight: bold;
  line-height: 36px;
  letter-spacing: 0px;
  color: #000000;
  margin-bottom: 24px;
}

.section-item-content {
  width: 100%;
  font-size: 18px;
  font-weight: normal;
  line-height: 29.25px;
  letter-spacing: 0px;
  color: #4B5563;
}

@media screen and (max-width: 1200px) {
.section-item {
  flex-direction: column;
  text-align: center;
  margin-left: 8px;
  margin-right: 8px;
}

.section-reverse-item {
  flex-direction: column;
  text-align: center;
  margin-left: 8px;
  margin-right: 8px;
}
}
</style>