<script lang="ts">
    import discordIconUrl from "$lib/assets/icon_discord_blue.svg";
    import emailIconUrl from "$lib/assets/mail.svg";
    import CopyText from "$lib/components/CopyText.svelte";
</script>
    
<section id="section-application" class="section">
    <p class="section-title">제작 신청</p>
    <p class="section-subtitle">
        편하신 방법으로 연락 주세요<br>
        제작 신청 뿐만 아니라 단순 문의도 가능하니 편하게 연락 주세요
    </p>
    <div class="section-content">
        <div class="section-item shadow">
            <img src="{discordIconUrl}" alt="discord">
            <div>
                <CopyText><p class="section-item-title">ksi123456ab</p></CopyText>
                <p class="section-item-description">디스코드 친구추가 후 DM 보내주세요.</p>
            </div>
        </div>
        <div class="section-item shadow">
            <img src="{discordIconUrl}" alt="discord">
            <div>
                <p class="section-item-title"><a target="_blank" href="https://discord.gg/FpYcEX8ej5">디스코드 서버</a></p>
                <p class="section-item-description">클릭하여 접속!</p>
            </div>
        </div>
        <div class="section-item shadow">
            <img src="{emailIconUrl}" alt="discord">
            <div>
                <CopyText><p class="section-item-title">ksi123456ab@gmail.com</p></CopyText>
                <p class="section-item-description">메일 보내주세요.</p>
            </div>
        </div>

        <a target="_blank" href="https://cafe.naver.com/ArticleList.nhn?search.clubid=29270508&search.menuid=14&search.boardtype=I">포트폴리오 보러가기</a>
    </div>
</section>

<style>
    a {
        color: black;
        text-decoration: underline;
    }

    .section {
        background-color: #f9fafb;
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-top: 96px;
        padding-bottom: 96px;
    }

    .section-title {
        font-size: 2rem;
        margin-bottom: 1rem;
        font-weight: bold;
        line-height: 36px;
        text-align: center;
        letter-spacing: 0px;
        color: black;
    }

    .section-subtitle {
        font-size: 1.125rem;
        text-align: center;
        color: #6B7280;
        line-height: 140%;
    }

    .section-content {
        width: calc(100% - 64px);
        display: flex;
        flex-direction: column;
        margin-top: 5rem;
        gap: 36px;
        align-items: center;
    }

    .section-item {
        width: 100%;
        display: flex;
        flex-direction: row;
        background-color: white;
        align-items: center;
        border-radius: 8px;
        padding: 0px;
        line-height: 140%;
        max-width: 400px;
    }

    .section-item img {
        width: 36px;
        height: 36px;
        margin: 24px 16px 24px 24px;
        object-fit: contain;
    }

    .section-item-title {
        font-size: 20px;
        font-weight: bold;
    }

    .section-item-description {
        font-size: 16px;
        color: #6B7280;
    }
</style>