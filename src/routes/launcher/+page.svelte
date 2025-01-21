<script lang="ts">
  import iconUrl from "$lib/assets/icon-al.svg";
  import LandingMainSection from "./LandingMainSection.svelte";
  import LandingKeyFeatureSection from "./LandingKeyFeatureSection.svelte";
  import LandingUseCaseSection from "./LandingUseCaseSection.svelte";
  import LandingFeatureSection from "./LandingFeatureSection.svelte";
  import LandingPlanSection from "./LandingPlanSection.svelte";
  import LandingApplicationSection from "./LandingApplicationSection.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import { onMount } from "svelte";

  function onscroll() {
    const navbar = document.getElementById("navbar");

    if (!navbar) return;
    if (window.scrollY > 120) {
      navbar.classList.add("nav-shadow");
    } else {
      navbar.classList.remove("nav-shadow");
    }
  }

  onMount(() => {
    const links = document.querySelectorAll(".smooth-section");
    links.forEach((link) => {
      link.addEventListener("click", (event) => {
        event.preventDefault(); // Prevent default anchor behavior
        const targetId = link.getAttribute("href")?.substring(1); // Get the target id
        if (!targetId) return;

        const targetSection = document.getElementById(targetId);
        targetSection?.scrollIntoView({
          behavior: "smooth",
        });
      });
    });
  });
</script>

<svelte:window {onscroll} />

<svelte:head>
    <title>주문제작 - 마인크래프트 커스텀 런처</title>

    <meta name="description" content="마인크래프트 런처, 설치기, 접속기를 만들어 드립니다. 모드 설치, 서버 접속, 다양한 기능 포함">
    <meta name="robots" content="index,follow">
</svelte:head>

<nav id="navbar" class="nav">
  <div class="nav-shadow" style="display: none;"></div>

  <div class="nav-logo">
    <a href="../"><img src={iconUrl} alt="Icon" /></a>
    <a href="../"><p>마인크래프트 커스텀 런처</p></a>
  </div>

  <div class="nav-links">
    <a class="smooth-section" href="#section-keyfeature">
      <p>기능</p>
    </a>
    <a class="smooth-section" href="#section-usecase">
      <p>포트폴리오</p>
    </a>
    <a target="_blank" href="https://isk162534.github.io/AlphaLauncherDocs/">
      <p>기술지원</p>
    </a>
    <a class="smooth-section button button-action" href="#section-application"
      >제작 신청</a
    >
  </div>
</nav>

<LandingMainSection />
<LandingKeyFeatureSection />
<LandingUseCaseSection />
<LandingFeatureSection />
<LandingPlanSection />
<LandingApplicationSection />

<Footer />

<style>
  .nav {
    position: sticky;
    top: 0;
    overflow: hidden;
    height: 64px;
    padding-left: 32px;
    padding-right: 32px;
    background-color: white;
    z-index: 1000;
    transition: box-shadow 0.3s ease-in-out;
  }

  .nav-shadow {
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.4);
  }

  .nav-logo {
    height: 100%;
    display: flex;
    align-items: center;
    float: left;
  }

  .nav-logo img {
    margin-top: 6px;
    height: 32px;
  }

  .nav-logo > a {
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: bold;
    margin-left: 12px;
    color: black;
  }

  .nav-links {
    height: 100%;
    display: flex;
    align-items: center;
    float: right;
    gap: 24px;
  }

  .nav-links > a {
    text-decoration: none;
    font-size: 1rem;
    color: #4b5563;
  }

  .nav-links > .button {
    width: 94px;
    height: 36px;
    font-size: 1rem;
    font-weight: normal;
    background-color: black;
    color: white;
    box-shadow: none;
  }
</style>
