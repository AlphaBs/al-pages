<script lang="ts">
    const { children } = $props();

    let button: HTMLElement;
    let tooltip: HTMLElement;
    let lastTimer: number | null;

    function onclick() {
        if (!button)
            return;

        navigator.clipboard.writeText(button.innerText.trim())
        tooltip.style.opacity = "1";

        if (lastTimer !== null) {
            clearTimeout(lastTimer);
        }

        lastTimer = setTimeout(() => {
            tooltip.style.opacity = "0";
        }, 1000);
    }
</script>

<div class="tooltip">
    <button bind:this={button} {onclick}>{@render children()}</button>
    <span bind:this={tooltip} class="tooltip-text">복사됨!</span>
</div>

<style>
    button {
        background: none;
        text-decoration: underline;
        cursor: pointer;
        border: none;
        padding: 0;
    }

    .tooltip {
        position: relative;
        display: inline-block;
    }

    .tooltip .tooltip-text {
        font-size: 14px;
        opacity: 0;
        transition: opacity 0.3s ease-in-out;
        width: 80px;
        top: 100%;
        left: 50%;
        margin-left: -40px;
        background-color: black;
        color: #fff;
        text-align: center;
        padding: 5px 0;
        border-radius: 6px;
        position: absolute;
        z-index: 1;
    }
</style>