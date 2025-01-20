<script>
    const { children } = $props();
</script>

{@render children()}

<style>
    :global {
        body.fontLoaded {
            font-family:
                "Pretendard Variable",
                Pretendard,
                -apple-system,
                BlinkMacSystemFont,
                system-ui,
                Roboto,
                "Helvetica Neue",
                "Segoe UI",
                "Apple SD Gothic Neo",
                "Noto Sans KR",
                "Malgun Gothic",
                "Apple Color Emoji",
                "Segoe UI Emoji",
                "Segoe UI Symbol",
                sans-serif !important;
        }

        body {
            background: white;
            margin: 0px;
            font-size: 18px;
        }

        p {
            margin: 0;
            word-break: keep-all;
            word-wrap: break-word;
        }

        .filter-black {
            filter: brightness(0) saturate(100%);
        }

        .button {
            display: block;
            box-shadow: 0 4px 16px 0 rgba(0, 0, 0, 0.4);
            cursor: pointer;
            font-size: 1rem;
            border: none;
            border-radius: 4px;
            text-align: center;
            align-content: center;
            text-decoration: none;
        }

        .button-action {
            box-shadow: 0 4px 16px 0 rgba(0, 0, 0, 0.4);
            font-weight: bold;
            color: white;
            background-color: black;
        }

        .shadow {
            box-shadow:
                0px 4px 8px -4px rgba(0, 0, 0, 0.1),
                0px 1px 3px 0px rgba(0, 0, 0, 0.1);
        }
    }
</style>
