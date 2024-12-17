<script>
  import planAImageUrl from "$lib/assets/plan-a.png";
  import planBImageUrl from "$lib/assets/plan-b.png";
  import planFreeImageUrl from "$lib/assets/plan-free.png";

  const plans = [
    {
      "title": "템플릿 A",
      "price": "₩40,000 ~ ",
      "image": planAImageUrl,
      "features": [
        "가운데 들어갈 아이콘만 있으면 됩니다.",
        "모든 기능 사용 가능합니다."
      ],
      "link": "https://cafe.naver.com/alphacml/144"
    },
    {
      "title": "템플릿 B",
      "price": "₩60,000 ~ ",
      "image": planBImageUrl,
      "features": [
        "가운데 들어갈 배경사진이 필요합니다.",
        "모든 기능 사용 가능합니다."
      ],
      "link": "https://cafe.naver.com/alphacml/147"
    },
    {
      "title": "자유 디자인",
      "price": "₩60,000 ~ ",
      "image": planFreeImageUrl,
      "features": [
        "화면 구성, 디자인 요소 모두 원하시는대로 제작 가능합니다.",
        "디자인은 의뢰자분이 직접 준비해 주셔야 합니다.",
        "모든 기능 사용 가능합니다."
      ],
      "link": "https://cafe.naver.com/alphacml?iframe_url=/MyCafeIntro.nhn%3Fclubid=29270508"
    },
  ];
</script>

<section id="section-plan" class="section">
  <p class="section-title">가격</p>
  <div class="section-content">
    {#each plans as plan}
    <div class="section-plan-item shadow">
      <p class="section-plan-title">{plan.title}</p>
      <p><span class="section-plan-price">{plan.price}</span></p>
      <img
        class="section-plan-image"
        src={plan.image}
        alt="screenshot"
      />
      <ul>
        {#each plan.features as feature}
        <li>{feature}</li>
        {/each}
        <li><a href="{plan.link}" target="_blank">예시 런처 보러가기</a></li>
      </ul>
    </div>
    {/each}
</section>

<style>
  a {
    color: black
  }

  .section {
    display: flex;
    flex-direction: column;
  }

  .section-title {
    margin-top: 48px;
    font-size: 30px;
    font-weight: bold;
    line-height: 36px;
    text-align: center;
    letter-spacing: 0px;
    color: black;
  }

  .section-content {
    display: flex;
    flex-direction: row;
    margin: 64px 32px 32px 32px;
    gap: 26px;
    max-width: 1200px;
    align-self: center;
  }

  .section-plan-item {
    flex-grow: 1;
    flex-shrink: 1;
    flex-basis: 0;
    display: flex;
    flex-direction: column;
    background-color: white;
    border-radius: 8px;
    padding: 36px;
  }

  .section-plan-title {
    font-size: 24px;
    font-weight: bold;
    line-height: 32px;
    letter-spacing: 0px;
    color: #111827;
    margin-bottom: 16px;
  }

  .section-plan-price {
    font-size: 36px;
    font-weight: bold;
    line-height: 40px;
    letter-spacing: 0px;
    color: #000000;
  }

  .section-plan-image {
    display: none;
    width: 100%;
    max-width: 500px;
    max-height: 500px;
    margin-top: 24px;
    margin-bottom: 24px;
    object-fit: contain;
  }

  ul, li {
    font-size: 16px;
    font-weight: normal;
    line-height: 24px;
    letter-spacing: 0px;
    color: #4b5563;
    margin-left: 0px;
    padding-left: 0px;
    list-style-position: inside;
  }

  @media screen and (max-width: 1100px) {
    .section-content {
      flex-direction: column;
    }
  }
</style>
