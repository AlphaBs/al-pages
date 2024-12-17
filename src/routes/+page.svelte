<script lang="ts">
  import cmllibIcon from "$lib/assets/icon-cmllib.ico";
  import alIcon from "$lib/assets/icon-al.svg";
  import fishIcon from "$lib/assets/icon-fish.png";
  import Project from "./Project.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<div class="main">
  <div class="title">
    <h1>Minecraft Projects</h1>
    <p class="subtitle">마인크래프트 런처 제작을 위한 다양한 프로젝트를 진행하고 있습니다</p>
  </div>

  <Project icon="{alIcon}" title="AlphabetLauncher" href="launcher" target="">
    <p>마인크래프트 커스텀 런처를 주문제작합니다.</p>
    <p><a href="launcher">제작문의</a></p>
    <p><a target="_blank" href="https://isk162534.github.io/AlphaLauncherDocs/">기술지원</a></p>
  </Project>

  <Project icon="{cmllibIcon}" title="CmlLib Projects" href="https://github.com/CmlLib" target="_blank">
    <p>마인크래프트 커스텀 런처를 만들기 위한 오픈소스 프로젝트</p>
    <p><a target="_blank" href="https://github.com/CmlLib">GitHub</a></p>
    <p><a target="_blank" href="https://alphabs.gitbook.io/cmllib">Docs</a></p>
  </Project>

  <Project icon="{fishIcon}" title="FISH" href="https://fish.alphabeta.pw" target="_blank">
    <p>게임 파일을 서버와 동기화합니다.</p>
    <p><a target="_blank" href="https://fish.alphabeta.pw">사이트 바로가기</a></p>
    <p><a target="_blank" href="https://github.com/AlphaBs/FishSyncClient">.NET SDK</a></p>
  </Project>
</div>

<Footer/>

<style>
  a {
    color: #00000090;
    text-decoration: underline;
  }
  
  .main {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 64px;
    margin-bottom: 96px;
  }

  .title {
    text-align: center;
    margin-top: 128px;
    margin-bottom: 64px;
  }

  .subtitle {
    color: #000000A0;
  }
</style>
