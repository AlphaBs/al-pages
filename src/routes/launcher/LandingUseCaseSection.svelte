<script>
  import "@splidejs/svelte-splide/css";
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  import { onMount } from "svelte";
  import i1 from "$lib/assets/1.png";
  import i2 from "$lib/assets/2.png";
  import i3 from "$lib/assets/3.png";
  import i4 from "$lib/assets/4.png";
  import i5 from "$lib/assets/5.png";
  import i6 from "$lib/assets/6.png";
  import i7 from "$lib/assets/7.png";
  import i8 from "$lib/assets/8.png";

  const slides = [
      { src: i1, alt: "case 1"},
      { src: i2, alt: "case 2"},
      { src: i3, alt: "case 3"},
      { src: i4, alt: "case 4"},
      { src: i5, alt: "case 5"},
      { src: i6, alt: "case 6"},
      { src: i7, alt: "case 7"},
      { src: i8, alt: "case 8"},
    ];

  let mainSlide;
  let thumbnailSlide;

  const mainOptions = {
    type: "fade",
    rewind: true,
    pagination: false,
    arrows: false,
  };

  const thumbnailOptions = {
    fixedWidth: 160,
    fixedHeight: 100,
    isNavigation: true,
    gap: 10,
    rewind: true,
    pagination: false,
    autoplay: true,
  };

  onMount(() => {
    if (mainSlide && thumbnailSlide) {
      mainSlide.sync(thumbnailSlide.splide);
    }
  });
</script>

<section id="section-usecase" class="section-3">
  <p class="section-3-title">사용 사례</p>
  <div class="section-3-subtitle">
    <p>5년간 120건 이상의 런처 개발</p>
    <p>국내외 대규모 모드 서버 런처, 유튜버/스트리머 컨텐츠용 런처까지</p>
    <a
      href="https://cafe.naver.com/ArticleList.nhn?search.clubid=29270508&search.menuid=14&search.boardtype=I"
      target="_blank"
    >
      모든 포트폴리오 보러가기
    </a>
  </div>
  <div class="section-3-content">
    <Splide options={ mainOptions } bind:this={ mainSlide } aria-labelledby="thumbnails-example-heading">
      {#each slides as slide}
        <SplideSlide>
          <img src={ slide.src } alt={ slide.alt } class="carousel-main">
        </SplideSlide>
      {/each}
    </Splide>
  
    <Splide options={ thumbnailOptions } bind:this={ thumbnailSlide } style="margin-top: 32px;">
      {#each slides as slide}
        <SplideSlide>
          <img src={ slide.src } alt={ slide.alt } class="carousel-thumbnail">
        </SplideSlide>
      {/each}
    </Splide>
  </div>
</section>

<style>
  .section-3 {
    display: flex;
    flex-direction: column;
    color: white;
    align-items: center;
    background-color: #111827;
  }

  .section-3-title {
    font-size: 30px;
    font-weight: bold;
    text-align: center;
    margin-top: 96px;
  }

  .section-3-subtitle {
    margin-top: 20px;
    font-size: 20px;
    text-align: center;
    color: #9ca3af;
    line-height: 160%;
  }

  .section-3-subtitle a {
    margin-top: 20px;
    font-size: 20px;
    text-align: center;
    color: #9ca3af;
    line-height: 160%;
  }

  .section-3-content {
    margin-top: 76px;
    margin-bottom: 96px;
    width: 90%;
    max-width: 800px;
  }

  .carousel-main {
    width: 100%;
    height: 400px;
    object-fit: contain;
  }

  .carousel-thumbnail {
    width: 100%;
    height: auto;
    object-fit: cover;
  }
</style>
