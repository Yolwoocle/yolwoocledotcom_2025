<script lang="ts">
    export var mainColor, secColor, shadColor;
	let { icon="", alt="" } = $props();
</script>

<div class="container">
    <button class="button shape-round"> 
        {#if icon}
        <img class="icon" src={icon} alt="{alt}"/> 
        {/if}
    </button>
</div>

<style>
    .icon {
        min-width: 30px;
        width: 30px;
        height: 30px;
    }

	.button {
        border: none;
        border-radius: 100px;

        position: relative;
        display: inline-flex;
        
        width: 65px;
        height: 65px;

        align-items: center;
        justify-content: center;
        
        padding: 10px;
        
        /* background: gold; */
        color: black;
        text-decoration: none;
        font-weight: bold;
        
        -webkit-box-shadow:inset 0px 0px 0px 5px var(--secColor);
        -moz-box-shadow:inset 0px 0px 0px 5px var(--secColor);
        box-shadow:
            inset 0px 0px 0px 5px var(--secColor),
            0px 2px 0px var(--shadColor),
            0px 4px 0px var(--shadColor),
            0px 6px 0px var(--shadColor),
            0px 8px 0px var(--shadColor),
            0px 10px 0px var(--shadColor),
            2px 17px 0px var(--transp-shad)
        ;

        background-color: var(--mainColor);

        top: 0;

        transition: 
        top 0.3s var(--ease-out-back),
        box-shadow 0.3s var(--ease-out-back);
    }

    .container:hover .button {
        top: -6px;

        box-shadow:
            inset 0px 0px 0px 5px var(--secColor),
            0px 3.2px 0px var(--shadColor),
            0px 6.4px 0px var(--shadColor),
            0px 9.6px 0px var(--shadColor),
            0px 12.8px 0px var(--shadColor),
            0px 16px 0px var(--shadColor),
            4px 28px 0px var(--transp-shad)
        ;
    }
    
    .text {
        position: absolute;
        transform: translate(-50%, -50%);
        
        font-size: 25px;

        color: var(--shadColor);
        
        top: calc(50% - 2px);
        left: 50%;

        transition: 
            top 0.3s var(--ease-out-back),
            text-shadow 0.3s var(--ease-out-back-soft);
    }

    /********************************/
    /* Animation */
    /********************************/
</style>
