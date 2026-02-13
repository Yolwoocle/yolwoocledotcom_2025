<script lang="ts">
	import Socials from "../../Socials.svelte";
	import TextButton from "../../TextButton.svelte";

  const birthDate = new Date('2004-12-07');
  const today = new Date();
  
  // Calculate age: subtract years, then adjust if birthday hasn't hit yet
  const age = today.getFullYear() - birthDate.getFullYear() - 
    (today < new Date(today.getFullYear(), birthDate.getMonth(), birthDate.getDate()) ? 1 : 0);
</script>

<div class="w-full flex flex-col items-center">
    <!-- <div class="max-w-215 px-5 text-center text-(--main-very-dark)">
        <h1 class="font-black text-4xl pt-6 pb-4">Art</h1>
        <p class="text-xl">
            You can find here a curated collection of my art. <br>
            Drawings I am particularily proud of have a star next to them. 
        </p>
    </div> -->
    <div class="max-w-215 px-5 py-10 flex flex-col items-center text-center text-(--main-very-dark)">
        <div class="py-15">
            <img src="src/lib/assets/images/hileo.gif" alt="drawing of leo" class="h-90"/>
        </div>
        <h1 class="font-black text-8xl pt-6 pb-4">Hi!</h1>
        <p class="text-2xl/10">
            I’m <strong>Léo Bernard</strong>, also known as <strong>Yolwoocle</strong>.<br>
            I’m <span>{age}</span> years old, I'm from France, and my pronouns are ‘he/him’. <br>
            I’ve loved making things ever since I was a child. <br>
            I believe that creating things is deeply human. <br>
            It’s something that brings me joy in my life, <br>    
            And I hope to share this joy to others through my creations. :)
        </p>

        <h1 class="font-black text-6xl pt-10 pb-4">Contact</h1>
        <p class="text-2xl/10">
            Here you can find various ways to contact me. <br>
            I read every message, but I might not always answer. <br>
            Please prioritize email for business-related enquiries.  
        </p>
        <Socials />
        <p class="text-2xl/10 pt-10">
            <strong>Discord:</strong> yo&#108woocl&#101<br>
            <strong>Email:</strong> &#108eo&#64yo&#108woocl&#101&#46com<br>
            (email responses may come from a dfferent address)<br>
        </p>

        <h1 class="font-black text-6xl pt-10 pb-4">Resume</h1>
        <p class="text-2xl/10">
            TODO
        </p>
        <TextButton 
            --mainColor="var(--main-dark)"
            --secColor="var(--main-dark-shad)"
            --shadColor="var(--main-dark-shad)"
            --textColor="#fff"
            text="TODO"
        />
    </div>
</div>

<style>
    strong {
        font-weight: 800;
    }
</style>