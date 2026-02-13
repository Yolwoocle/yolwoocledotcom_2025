<script lang="ts">
	import CardGrid from "../../CardGrid.svelte";

	let projects = [
        {
            img : "src/lib/assets/images/art/love.png",
            label : "I'll be there for you",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/humanditto.png",
            label : "Human Ditto",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/kirbystar.gif",
            label : "Kirby Star",
            description : "Inspired by Kiana Mosser",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/comm_alexis_pfp.png",
            label : "Alexis",
            description : "Commission",
        },
        {
            img : "src/lib/assets/images/art/n7_pull_twitter.png",
            label : "N7 Hoodie Contest Submission",
            description : "Unfortunately did not win :(",
        },
        {
            img : "src/lib/assets/images/art/cat_and_girl.png",
            label : "Cat and Girl",
            description : "Commission",
        },
        {
            img : "src/lib/assets/images/art/carboard_city.png",
            label : "Miniature Kaiju",
            description : "<a class='card-link' href=\"https://bsky.app/profile/yolwoocle.com/post/3lwvbf3huv22r\">Behind the pixels</a>",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/sunnyside_cruise.png",
            label : "Sunnyside Cruise",
            description : "<a class='card-link' href='https://bsky.app/profile/yolwoocle.com/post/3lqlfgz77uc2d'>Behind the pixels</a>",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/leo_starter_pack_noai_small.png",
            label : "Yolwoocle Starter Pack",
            description : "",
        },
        {
            img : "src/lib/assets/images/drawings/dino_remake.png",
            label : "Chrome Dino Remake (2025)",
            description : "Concept art",
        },
        {
            img : "src/lib/assets/images/drawings/mario_redraw_scene.png",
            label : "Super Mario Bros. Redrawn",
            description : "Concept art",
        },
        {
            img : "src/lib/assets/images/drawings/assembleenationale2.png",
            label : "Ennemicycle",
            description : "Mockup for a french politics fighting joke game",
        },
        {
            img : "src/lib/assets/images/art/catcliff.png",
            label : "Serenity",
            description : "",
            starred: true,
        },
        {
            img : "src/lib/assets/images/drawings/switchblade.png",
            label : "Switchblade",
            description : "Commissioned artwork for a game",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/BoxOfMushies.png",
            label : "Box of Mushies",
            description : "Made using Blender",
        },
        {
            img : "src/lib/assets/images/art/hxi2_hoodie.png",
            label : "HXi² hoodie",
            description : "Artwork made for a school hoodie",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/sweat_taupins_v1.png",
            label : "Taupins",
            description : "Artwork for a school hoodie",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/TreesThings.png",
            label : "Hidden Kingdom",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/antPoster.png",
            label : "Soldier Ant",
            description : "Artwork that inspired Bugscraper",
        },
        {
            img : "src/lib/assets/images/art/minecraft_desert-pico8.png",
            label : "PICO-8 Minecraft: Desert",
            description : "Concept Art Mockup",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/minecraft-pico8.png",
            label : "PICO-8 Minecraft: Overworld",
            description : "Concept Art Mockup",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/pico-8_unrailed_concept.png",
            label : "PICO-8 Unrailed Demake Mockup",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/LCD Console Concept.png",
            label : "LCD Console Mockup",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/BJG_coffee_recycle_shop_thing_FINAL.png",
            label : "Cofee Shop",
            description : "Inspired by Brandon James Greer",
        },
        {
            img : "src/lib/assets/images/art/aquarium.gif",
            label : "Aquarium",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/microchipCity_watermark.png",
            label : "Microchip City",
            description : "Made to accompany the following track: <a class='card-link' href=\"https://www.youtube.com/watch?v=JCoXo-hwczs\">YouTube</a>",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/MicrochipCitySketch.jpg",
            label : "Microchip City Sketch",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/clayGoombud.jpg",
            label : "Clay Goombud",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/atelier_info.png",
            label : "Poster for a programming club",
            description : "",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/girlwateringplant4.png",
            label : "Girl Watering Plants",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/dino_sleeping17.gif",
            label : "Dino's adventure begins",
            description : "",
            starred: true,
        },
        {
            img : "src/lib/assets/images/art/dinogbwatermark_bigger.gif",
            label : "Gameboy Chrome Dino",
            description : "Concept Art",
            starred: true,
        }, 
        {
            img : "src/lib/assets/images/art/diamond5.png",
            label : "Diamonds",
            description : "",
            starred: true,
        }, 
        {
            img : "src/lib/assets/images/art/heartImprovedWaterMark.png",
            label : "Hearts",
            description : "",
        }, 
        {
            img : "src/lib/assets/images/art/trefleImprovedWatermark.png",
            label : "Clubs",
            description : "",
        }, 
        {
            img : "src/lib/assets/images/art/spaceChess.jpg",
            label : "Space Chess",
            description : "Made using Blender",
        }, 
        {
            img : "src/lib/assets/images/art/NESvoxelArt.jpg",
            label : "NES Voxel Art",
            description : "A tribute",
        }, 
        {
            img : "src/lib/assets/images/art/RobertoZucco.png",
            label : "Roberto Zucco",
            description : "Made for my French class",
            starred: true,
        }, 
        {
            img : "src/lib/assets/images/art/GoombaGoombette3.png",
            label : "Goomba Love",
            description : "",
        }, 
        {
            img : "src/lib/assets/images/art/pigeons_NOT_WATERMARKED_23-oct_V3.png",
            label : "Pigeon chase",
            description : "",
        },
        {
            img : "src/lib/assets/images/art/DoodleArtVertical.png",
            label : "Doodle Art",
            description : "",
        }, 
        {
            img : "src/lib/assets/images/art/voxelArtCactus.jpg",
            label : "Voxel Cacti",
            description : "Made using Magicavoxel",
        },
        {
            img : "src/lib/assets/images/art/marioMakerFanArt.png",
            label : "Super Mario Maker 2 Fanart",
            description : "Around 2018",
        },
    ];

</script>

<div class="w-full flex flex-col items-center">
    <div class="max-w-215 px-5 text-center text-(--main-very-dark)">
        <h1 class="font-black text-4xl pt-6 pb-4">Art</h1>
        <p class="text-xl">
            You can find here a curated collection of my art. <br>
            Drawings I am particularily proud of have a star next to them. 
        </p>
        <CardGrid cards={projects} />
    </div>
</div>

<style>
</style>
