<script>
  import launcherImageUrl from '$lib/assets/launcher.png'
  import launcherVideoUrl from '$lib/assets/launcher.webm'
</script>

<section id="section-main" class="section-1">
  <div class="section-1-title">
    <p>마인크래프트 커스텀 런처</p>
    <p>주문제작</p>
  </div>
  <div class="section-1-subtitle">
    <p>클릭 한번으로 모드 설치부터 서버 접속까지 한번에!</p>
    <p>서버에 접속하기 위한 복잡한 과정들을 아주 쉽게 만들어 드립니다</p>
  </div>
  <div class="section-1-action">
    <a
      class="button button-action smooth-section"
      href="#section-application">제작 신청</a>
  </div>
  <div class="section-1-content">
    <div class="section-1-content-video-holder">
      <video muted autoplay loop>
        <source src="{launcherVideoUrl}" type="video/mp4" />
        <img src="{launcherImageUrl}" alt="launcher" />
      </video>
    </div>
  </div>
</section>

<style>
  .section-1 {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.section-1-title {
  margin-top: 64px;
  width: 100%;
}

.section-1-title > p {
  text-align: center;
  font-size: 60px;
  font-weight: bold;
  margin: 0;
}

.section-1-subtitle {
  margin-top: 20px;
}

.section-1-subtitle>p {
  margin: 0px;
  font-size: 20px;
  text-align: center;
  color: #6B7280;
}

.section-1-action {
  margin-top: 40px;
}

.section-1-action a {
  width: 200px;
  height: 48px;
}

.section-1-content {
  margin-top: 64px;
  margin-bottom: 96px;
  width: 90%;
  max-width: 900px;
}

.section-1-content-video-holder>* {
  width: 100%;
  box-shadow: 0 3px 12px rgba(0, 0, 0, 0.8);
  border-radius: 6px;
}
</style>