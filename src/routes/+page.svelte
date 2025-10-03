<script lang="ts">
	import Title from './Title.svelte';
	import WavyTitle from './WavyTitle.svelte';
	import Subtitle from './Subtitle.svelte';
	import Overtitle from './Overtitle.svelte';

	import BigStarButton from './BigStarButton.svelte';
	import TextButton from './TextButton.svelte';
	import IconButton from './IconButton.svelte';
</script>

<div class="page">
    <div class="titles">
        <Overtitle text="Léo Bernard • 曹宇" />
        <WavyTitle text="Yolwoocle"/>
        <Subtitle text="Game dev & artist from France" />
    </div>
    
    <div class="nav nav-main">
        <BigStarButton href="#" buttonStyle={1} text="Games"/>
        <BigStarButton href="#" buttonStyle={2} text="Art"/>
    </div>
    
    <div class="nav nav-other pointer-events-none">
        <BigStarButton href="#" buttonStyle={3} text="Other"/>
    </div> 
    
    <div class="nav">
        <TextButton 
            text="About" 
            --mainColor="var(--white-main)" 
            --secColor="var(--white-sec)" 
            --shadColor="var(--white-shad)" 
            --textColor="var(--white-shad)"
        />
        <!-- <TextButton 
            text="Download CV" 
            --mainColor="var(--main-dark)" 
            --secColor="var(--main-dark-shad)" 
            --shadColor="var(--main-dark-shad)" 
            --textColor="var(--white-main)"
        /> -->
    </div>
    
    <div class="nav nav-socials">
        <IconButton 
            icon="/src/lib/assets/logos/email-white.svg"
            alt="email"
            href="mailto:leo@yolwoocle.com"
            --mainColor="var(--main-dark)" 
            --secColor="var(--main-dark-shad)" 
            --shadColor="var(--main-dark-shad)" 
        />
        <IconButton 
            icon="/src/lib/assets/logos/bluesky-white.svg"
            alt="bluesky"
            href="https://bsky.app/profile/yolwoocle.com/"
            --mainColor="var(--main-dark)" 
            --secColor="var(--main-dark-shad)" 
            --shadColor="var(--main-dark-shad)" 
        />
        <IconButton 
            icon="/src/lib/assets/logos/twitter-white.svg"
            alt="twitter/x"
            href="https://x.com/yolwoocle_/"
            --mainColor="var(--main-dark)" 
            --secColor="var(--main-dark-shad)" 
            --shadColor="var(--main-dark-shad)" 
        />
        <IconButton 
            icon="/src/lib/assets/logos/itchio-white.svg"
            alt="itchio"
            href="https://yolwoocle.itch.io/"
            --mainColor="var(--main-dark)" 
            --secColor="var(--main-dark-shad)" 
            --shadColor="var(--main-dark-shad)" 
        />
        <IconButton 
            icon="/src/lib/assets/logos/github-white.svg"
            alt="github"
            href="https://github.com/yolwoocle"
            --mainColor="var(--main-dark)" 
            --secColor="var(--main-dark-shad)" 
            --shadColor="var(--main-dark-shad)" 
        />
        
    </div>
</div>

<style>
    .page {
        display: flex;
        flex-direction: column;

        align-items: center;
        justify-content: center;
    }

    .titles {
        text-align: center;
    }

    .nav {
        display: flex;
        justify-content: center;

        flex-direction: row;
        gap: 20px;
    }
    
    .nav-main {
        display: flex;
        gap: 60px;

        margin-top: 40px;
    }

    .nav-other {
        position: relative;
        top: -60px;

        height: 130px;
    }

    .nav-socials {
        margin-top: 20px;
        gap: 10px;
    }


    @keyframes constantMovement {
        0%{
            background-position: 0px 0px;
        }
        100% {
            background-position: 0px 110px;
        }
    }

    .page {
        margin: 0;

        width: 100%;
        height: 100vh;

        background-position: 0px;
        background-image: linear-gradient(135deg, var(--green-main) 25%, var(--green-sec) 25%, var(--green-sec) 50%, var(--green-main) 50%, var(--green-main) 75%, var(--green-sec) 75%, var(--green-sec) 100%);
        background-size: 110px 110px;
        
        animation: constantMovement 7s linear infinite;
    }
</style>