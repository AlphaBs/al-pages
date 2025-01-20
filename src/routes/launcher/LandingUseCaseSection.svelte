<script lang="ts">
  import "@splidejs/svelte-splide/css";
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  import i1 from "$lib/assets/1.png";
  import i2 from "$lib/assets/2.png";
  import i3 from "$lib/assets/3.png";
  import i4 from "$lib/assets/4.png";
  import i5 from "$lib/assets/5.png";
  import i6 from "$lib/assets/6.png";
  import i7 from "$lib/assets/7.png";
  import i8 from "$lib/assets/8.png";
  import i9 from "$lib/assets/9.png";
  import i10 from "$lib/assets/10.png";
  import i11 from "$lib/assets/11.png";
  import i12 from "$lib/assets/12.png";
  import i13 from "$lib/assets/13.png";
  import i14 from "$lib/assets/14.png";
  import i15 from "$lib/assets/15.png";

  const slides = [
      { src: i1, alt: "case 1"},
      { src: i2, alt: "case 2"},
      { src: i3, alt: "case 3"},
      { src: i4, alt: "case 4"},
      { src: i5, alt: "case 5"},
      { src: i6, alt: "case 6"},
      { src: i7, alt: "case 7"},
      { src: i8, alt: "case 8"},
      { src: i9, alt: "case 9"},
      { src: i10, alt: "case 10"},
      { src: i11, alt: "case 11"},
      { src: i12, alt: "case 12"},
      { src: i13, alt: "case 13"},
      { src: i14, alt: "case 14"},
      { src: i15, alt: "case 15"},
    ];
</script>

<section id="section-usecase" class="section">
  <p class="section-3-title">포트폴리오</p>
  <div class="section-3-subtitle">
    <p>5년간 120건 이상의 런처 개발</p>
    <p>국내외 대규모 모드 서버 런처, 유튜버/스트리머 컨텐츠용 런처까지</p>
  </div>
  <div class="section-content">
    {#each slides as slide}
      <img src={ slide.src } alt={ slide.alt } class="section-image">
    {/each}
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
