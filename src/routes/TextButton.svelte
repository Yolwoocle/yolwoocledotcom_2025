<script lang="ts">
	let { text } = $props();
</script>

<button class="button"> 
    <span class="text">{text}</span>
</button>

<style>
	.button {
        position: relative;
        display: inline-flex;

        width: 200px;       /* size of the star button */
        height: 200px;

        /* background: gold; */
        color: black;
        text-decoration: none;
        font-weight: bold;

        width: 160;
        height: 160;

        top: 0;

        transition: 
            top 0.3s var(--ease-out-back);
	}
    

    .star-shape {
        height: 100%;

        transition: 
            top 0.3s var(--ease-out-back),
            filter 0.3s var(--ease-out-back);
    }
    
    .star-shape-group {
        top: 0;

        transition: 
            top 0.3s ease,
            transform 0.6s ease;
        transform-origin: 50% 50%;
    }
    
    .text {
        position: absolute;
        transform: translate(-50%, -50%);
        
        font-size: 30px;
        
        top: calc(50% - 2px);
        left: 50%;

        transition: 
            top 0.3s var(--ease-out-back),
            text-shadow 0.3s var(--ease-out-back-soft);
    }

    .star-shape-style-1 {
        filter: 
            drop-shadow( 0px 4px 0 var(--yellow-shad) )
            drop-shadow( 0px 4px 0 var(--yellow-shad) )
            drop-shadow( 0px 4px 0 var(--yellow-shad) )
            drop-shadow( 0px 4px 0 var(--yellow-shad) )
            drop-shadow( 0px 4px 0 var(--yellow-shad) )
            drop-shadow( 3px 11px 0 var(--transp-shad) );
    }

    .star-shape-style-2 {
        filter: 
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 0px 2px 0 var(--blue-shad) )
            drop-shadow( 3px 11px 0 var(--transp-shad) );
    }

    .star-shape-style-3 {
        filter: 
            drop-shadow( 0px 2px 0 var(--pink-shad) )
            drop-shadow( 0px 4px 0 var(--pink-shad) )
            drop-shadow( 0px 6px 0 var(--pink-shad) )
            drop-shadow( 2px 6px 0 var(--transp-shad))
        ;
    }

    .text-style-1 {
        color: var(--yellow-text);
        
        text-shadow: 
            1px 4px 0 var(--transp-shad);
    }
    
    .text-style-2 {
        color: var(--blue-text);
        
        text-shadow: 
            1px 4px 0 var(--transp-shad);
    }
    
    .text-style-3 {
        color: var(--pink-text);
        font-size: 20px;

        text-shadow: 
            1px 2px 0 var(--transp-shad);
    }

    /********************************/
    /* Animation */
    /********************************/

    .star-button:hover .star-shape-style-1, .star-button:hover .star-shape-style-2{
        top: -12px;
    }

    .star-button:hover .star-shape-style-3{
        top: -6px;
    }
    
    .star-button:hover .star-shape-group {
        transform: rotate(30deg);
    }
    
    .star-button:hover .star-shape-style-1 {
        filter: 
            drop-shadow( 0px 6px 0 var(--yellow-shad) )
            drop-shadow( 0px 6px 0 var(--yellow-shad) )
            drop-shadow( 0px 6px 0 var(--yellow-shad) )
            drop-shadow( 0px 6px 0 var(--yellow-shad) )
            drop-shadow( 0px 6px 0 var(--yellow-shad) )
            drop-shadow( 5px 16px 0 var(--transp-shad) );
    }
    
    .star-button:hover .star-shape-style-2 {
        filter: 
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 0px 3px 0 var(--blue-shad) )
            drop-shadow( 5px 16px 0 var(--transp-shad) );
    }
    
    .star-button:hover .star-shape-style-3 {
        filter: 
            drop-shadow( 0px 2px 0 var(--pink-shad) )
            drop-shadow( 0px 6px 0 var(--pink-shad) )
            drop-shadow( 0px 10px 0 var(--pink-shad) )
            drop-shadow( 3px 10px 0 var(--transp-shad))
        ;
    }

    .star-button:hover .text-style-1,.star-button:hover .text-style-2 {
        top: calc(50% - 18px);
        
        text-shadow: 
            2px 6px 0 var(--transp-shad);
    }

    .star-button:hover .text-style-3 {
        top: calc(50% - 12px);
        
        text-shadow: 
            1px 4px 0 var(--transp-shad);
    }
</style>
