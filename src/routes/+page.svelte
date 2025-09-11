<script lang="ts">
	import Title from './Title.svelte';
	import Subtitle from './Subtitle.svelte';
	import Overtitle from './Overtitle.svelte';

	import BigStarButton from './BigStarButton.svelte';
</script>

<div class="page">
    <div class="content">
        <Overtitle text="Léo Bernard • 曹宇" />
        <Title text="Yolwoocle"/>
        <Subtitle text="Game dev & artist from France" />
    </div>
    
    <div class="nav nav-main">
        <BigStarButton href="#" buttonStyle="1" text="Art"/>
        <BigStarButton href="#" buttonStyle="2" text="Games"/>
    </div>
    
    <div class="nav nav-other">
        <BigStarButton href="#" buttonStyle="3" text="Other"/>
    </div> 
</div>

<!-- <div class="nav">
    <button> About </button>
</div>

<div class="nav">
    <div>
        <button>E-mail</button>
        <button>itch.io</button>
        <button>Twitter</button>
        <button>Bluesky</button>
        <button>Instagram</button>
        <button>GitHub</button>
        <button>LinkedIn</button>
    </div>
</div> -->

<style>
    .content {
        text-align: center;
    }

    .nav {
        display: flex;
        justify-content: center;
    }
    
    .nav-main {
        display: flex;
        gap: 60px;

        margin-top: 40px;
    }

    .nav-other {
        position: relative;
        top: -20px;
    }


    @keyframes constantMovement {
        0%{
            background-position: 0px 0px;
        }
        100% {
            background-position: 0px 181.02px;
        }
    }

    .page {
        /* Thanks to https://stripesgenerator.com/ */
        margin: 0;

        width: 100%;
        height: 100vh;

        background-position: 0px;
        background-image: linear-gradient(135deg, var(--green-main) 25%, var(--green-sec) 25%, var(--green-sec) 50%, var(--green-main) 50%, var(--green-main) 75%, var(--green-sec) 75%, var(--green-sec) 100%);
        background-size: 90px 90px;
        
        animation: constantMovement 5s linear infinite;
    }
</style>