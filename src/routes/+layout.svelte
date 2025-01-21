<script>
    import '$lib/styles/global.css';
    const { children } = $props();
</script>

<svelte:head>
    <link rel="icon" type="image/png" href="/favicon-96x96.png" sizes="96x96" />
    <link rel="icon" type="image/svg+xml" href="/favicon.svg" />
    <link rel="shortcut icon" href="/favicon.ico" />
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
    <meta name="apple-mobile-web-app-title" content="MyWebSite" />
    <link rel="manifest" href="/site.webmanifest" />

    <script type="application/ld+json">
        {
          "@context" : "https://schema.org",
          "@type" : "WebSite",
          "name" : "마인크래프트 커스텀 런처 프로젝트",
          "alternateName": ["마인크래프트 커스텀 런처", "마인크래프트 런처", "마크런처"],
          "url" : "https://minecraft.alphabeta.pw/"
        }
      </script>
</svelte:head>

{@render children()}