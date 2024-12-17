<script>
    const { icon, title, href, target, children } = $props();
</script>

<div class="project shadow">
    <div class="project-title">
        <a target="{target}" href="{href}"><img src={icon} alt="Icon" /></a>
        <h2><a target="{target}" href="{href}">{title}</a></h2>
    </div>
    <div class="project-content">
        {@render children()}
    </div>
</div>

<style>
    a {
        color: black;
        text-decoration: underline;
    }

    .project {
        border: solid rgba(0, 0, 0, 0.4) 1px;
        border-radius: 4px;
        background-color: white;

        display: flex;
        flex-direction: column;
        width: calc(100% - 96px);
        max-width: 1000px;
        margin-left: 48px;
        margin-right: 48px;
    }

    .project-title {
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    .project-title img {
        margin: 24px;
        width: 48px;
        height: 48px;
    }

    .project-content {
        margin: 0px 0px 24px 24px;
        line-height: 140%;
    }
</style>
