<script>
  import downloadIconUrl from '$lib/assets/download.svg'
  import webIconUrl from '$lib/assets/web.svg'
  import updateIconUrl from '$lib/assets/update.svg'
  import settingIconUrl from '$lib/assets/setting.svg'
</script>

<style>
  .section-2 {
  display: flex;
  flex-direction: column;
}

.section-2-title {
  font-size: 30px;
  font-weight: bold;
  text-align: center;
  margin-top: 96px;
}

.section-2-content {
  margin-top: 64px;
  margin-bottom: 96px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 32px;
  align-self: center;
  width: calc(100% - 64px);
  max-width: 1600px;
}

@media (max-width: 900px) {
  .section-2-content {
      grid-template-columns: 1fr;
  }
}

.section-2-item {
  padding: 32px;
  border-radius: 8px;
  background: white;
}

.section-2-item-icon {
  height: 36px;
}

.section-2-item-title {
  margin-top: 16px;
  color: #111827;
  font-size: 20px;
  font-weight: 600;
  line-height: 28px;
}

.section-2-item-content {
  margin-top: 12px;
  font-size: 16px;
  font-weight: normal;
  line-height: 24px;
  letter-spacing: 0px;
  color: #4B5563;
}
</style>

<section id="section-2" class="section-2">
  <div class="section-2-title">
    <p>주요 기능</p>
  </div>
  <div class="section-2-content">
    <div class="section-2-item shadow">
      <img src="{downloadIconUrl}" alt="모드 설치" class="section-2-item-icon filter-black" />
      <p class="section-2-item-title">모드 설치</p>
      <p class="section-2-item-content">
        포지/패브릭, 모드, 리소스팩 설치와 옵션 세팅...<br />
        서버에 접속하기 위해 복잡하고 어려운 과정을 거쳐야만 했었습니다.<br />
        <strong
          >커스텀 런처에서는 서버 접속에 필요한 모든 파일을 자동으로 설치합니다.</strong
        >
      </p>
    </div>
    <div class="section-2-item shadow">
      <img src="{webIconUrl}" alt="서버 접속" class="section-2-item-icon filter-black" />
      <p class="section-2-item-title">서버 접속</p>
      <p class="section-2-item-content">
        서버 주소를 입력할 필요조차 없습니다!<br />
        <strong
          >커스텀 런처에서 게임을 실행하면 서버 접속까지 한번에 이루어 집니다.</strong
        ><br />
        + 멀티플레이 서버 목록에 서버 자동 추가<br />
        + 서버 주소 노출 없이 서버 접속
      </p>
    </div>
    <div class="section-2-item shadow">
      <img src="{updateIconUrl}" alt="모드 업데이트" class="section-2-item-icon filter-black" />
      <p class="section-2-item-title">모드 업데이트</p>
      <p class="section-2-item-content">
        서버 운영중에 모드를 교체하고 싶다면?<br />
        더 이상 유저들이 복잡하고 어려운 모드 설치를 다시 할 필요가 없습니다.<br
        />
        <strong
          >언제든지, 어떤 파일이든, 직접 업데이트가 가능하며 즉시 적용됩니다.</strong
        >
      </p>
    </div>
    <div class="section-2-item shadow">
      <img src="{settingIconUrl}" alt="게임 설정" class="section-2-item-icon filter-black" />
      <p class="section-2-item-title">게임 설정</p>
      <p class="section-2-item-content">
        리소스팩 적용, 쉐이더팩 적용, 언어 설정, 키 설정, 각종 그래픽 설정
        등등...<br />
        마인크래프트의 설정도 원하는 대로 바꿀 수 있습니다.
      </p>
    </div>
  </div>
</section>
