<script lang="ts">
    let { text } = $props();
</script>

<p>{text}</p>

<style>
    p {
        color: var(--main-dark);
        
        font-size: 60px;
        font-weight: 700;

        margin-top: 0px;
        margin-bottom: 10px;

        text-shadow:
            0px 2px 0 var(--main-dark-shad),
            0px 4px 0 var(--main-dark-shad),
            0px 6px 0 var(--main-dark-shad),
            2px 9px 0 var(--transp-shad);
    }
</style>