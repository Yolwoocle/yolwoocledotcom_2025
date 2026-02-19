<script lang="ts">
	import CardGrid from '../../CardGrid.svelte';

	let projects = [
		[
			{
				cardType : "large",
				starred : true,
				
				label : "Bugscraper",
				description : "Rise to the top of a bug-filled skyscraper",
				longDescription : `Welcome to the Bugscraper.<br>
				Bugscraper is a solo or co-op roguelike shooter. As you climb toward your tyrannical boss's office, you'll battle floor after floor of enemies. Using a wide arsenal of weapons and upgrades, mow them down and aim for the top!<br>
				`,
				img : "src/lib/assets/images/games/bugscraper/thumbnail.png",
				preview : "./img/games/bugscraper/gameplay.gif",
				trailer : null,
				links: {
					"Official website": "https://bugscraper.net/",
					"Steam": "https://store.steampowered.com/app/2957130/Bugscraper/",
					"itch.io": "https://yolwoocle.itch.io/bugscraper/",
				}
			}, 
			{
				cardType : "large",
				starred : true,

				label : "Globs",
				description : "Meet the size-changing Globs in this colorful puzzle game",
				longDescription : ` Meet the size-changing Globs in this colorful puzzle game. Use the curious properties of their bodies at your advantage to solve a variety of puzzles, all in a expressive pixel art aesthetic and upbeat soundtrack.
				<br>
				The puzzles are designed to be approachable, but provide additional optional challenges for players wishing to put their puzzle-solving skills to the test.  
				Discover 40 levels across 4 different worlds.<br><br>
				
				This game was originally made in 96 hours for the <a href="https://itch.io/jam/gmtk-2024">GMTK Game Jam 2024</a> based on the theme "Built to Scale", but we continued working on it afterwards. 
				`,
				img : "src/lib/assets/images/games/globs/thumbnail.png",
				preview : "./img/games/globs/screenshot.png",
				trailer : "https://www.youtube.com/embed/yNs8oIw1vEM?si=EH5uMefULzqRiaOH",
				links: {
					"Android": "https://play.google.com/store/apps/details?id=com.yolwoocle.globs",
					"iOS": "https://apps.apple.com/us/app/globs-a-colorful-puzzle-game/id6738417089",
					"Steam": "https://s.team/a/3219110",
					"itch.io": "https://ninesliced.itch.io/globs/",
					"Github": "https://github.com/ARKANYOTA/gmtk2024/",
				}
			}, 
		],
		[
			{
				cardType : "normal",
				
				starred : true,

				label : "Birds With Guns",
				description : "Mess with the Flock, you get the Glock",
				longDescription : `Are you ready to have a quacking time? Toucan play this egg-citing game right now! Made by an im-peck-able team of quail-ified developers, you're gonna have no egrets. <b>Birds With Guns</b> is a game I made with a friend over the course of a vacation.`,
				img : "src/lib/assets/images/games/bwg/bwg_square.png",
				preview : null, //"./img/games/bwg/gif/bwg_1.gif",
				trailer : "https://www.youtube.com/embed/jb6uOKTxTlc",
				links : {
					"PICO-8 Forums": "https://www.lexaloffle.com/bbs/?tid=45334",
					"itch.io": "https://yolwoocle.itch.io/birds-with-guns",
				},
			}, 
			{
				cardType : "normal",
				
				label : "Minesweeper Royale",
				description : "Minesweeper, but it's a battle royale.",
				longDescription : `<b>Minesweeper Royale</b> is what minesweeper would be like if it were
				a battle royale game. Multiple players compete to be the fastest to complete the
				same minesweeper board, or to be the last one alive. This game is complete with a chat
				system and a display showing all the player boards. This was my first ever attempt 
				at networking, using the L&Ouml;VE framework and luasocket. It was a project I made 
				for school, hence it's not available on itch.io and I didn't advertize it. <br>The 
				source code is available on GitHub, but the little documentation I have provided
				is in French. During my attempts to make it work, I have rarely managed to make it
				work across multiple computers, but it does work locally. I encourage you to take 
				a look at the source code.`,
				img : "src/lib/assets/images/games/minesweeper_royale/thumbnail.png",
				preview : "./img/games/minesweeper_royale/gameplay.png",
				trailer : null, //"https://www.youtube.com/embed/jb6uOKTxTlc",
				links : {
					"GitHub": "https://github.com/Yolwoocle/Minesweeper_Royale",
				},
			}, 
			{
				cardType : "normal",
				
				label : "Derailed!",
				description : "A co-op game about building tracks",
				longDescription : `<b>Derailed!</b> is yet another PICO-8 game I made to challenge myself. It's a co-op game where you need to communicate with a friend to bring a train to its station. It's a fan-made demake of Unrailed!. After I made some concept art for a PICO-8 demake of this game, I thought it would be fun to actually turn it into a real thing. I hope that you'll have fun playing it, and maybe you can grab a friend to try it out.<br><br><i>(The game is unfinished, but it's playable nonetherless. I don't plan to finish it.)</i>`,
				img : "src/lib/assets/images/games/derailed/pico-8_unrailed_concept_thumbnail.png",
				preview : "./img/games/derailed/pico-8_unrailed_concept_thumbnail_wide.png",
				trailer: null,
				links: {
					"PICO-8 Forums": "https://www.lexaloffle.com/bbs/?pid=derailed",
					"itch.io": "https://yolwoocle.itch.io/derailed",
				}
			},
			{
				starred: true,

				label : "Pico Dino",
				description : "Reimagining Google Chrome's secret game",
				longDescription : `<b>Pico Dino</b> is what came out as I tried to make something simple, but as polished as possible. I really like complexity 
				that rises from simple things, like icons and puzzles (and even math), so I found it very fun trying to come up with a complex moveset 
				from a very simple 2-button control scheme. I originally wanted to add different worlds, power-ups, more enemies, but at some point I had 
				to make something I could actually finish. Nonetherless, I'm quite pleased with how it turned out.<br>
				I sent my game by email to Edward Jung, one of the two creators of the original game, and he seemed to love it, which made me very happy.
				`,
				img : "src/lib/assets/images/games/picodino/thumbnail.png",
				preview : "./img/games/picodino/dinogifusethis.gif",
				trailer: null, //"https://www.youtube.com/embed/XF79HG9XOaA",
				links: {
					"PICO-8 Forums": "https://www.lexaloffle.com/bbs/?tid=40759",
					"itch.io": "https://yolwoocle.itch.io/pico-dino",
				}
			}, 
		],
		
		[
			{
				cardType : "title",

				text : "Game jam games",
			},		
		],

		[

			{
				cardType : "normal",
				
				label : "Oracle's Inn",
				description : "Practice Malpractice",
				longDescription : `Welcome to my potion shoppe! I'm glad to have you here. However, I can sense dark waters in your future. I know just the ingredients...
				In <b>Oracle's Inn</b>, you take the role of alchemist/doctor/oracle/bundle of joy and happen to be just the person your customers need. Catch glimpses into the futures of your customers, and prepare for them live-saving potions in advance!
				This game was made in 3 days with Louie Chapman for the Mini Jam 112, following the theme "Chrono" and limitation "Only three buttons".`,
				img : "src/lib/assets/images/games/oraclesInn/OraclesInnThumnail.png",
				preview : "./img/games/oraclesInn/gameplay.gif",
				trailer : null,
				links: {
					"itch.io": "https://louiechapm.itch.io/oracles-inn",
				}
			}, 

			{
				cardType : "normal",
				
				label : "Octoboom",
				description : "Ping, Pong, Boom. Made for a game jam.",
				longDescription : `<b>Octoboom</b> is a game I made with friends for 
				<a href="https://ldjam.com/events/ludum-dare/49">Ludum Dare 49</a> 
				in the span of 3 days. <br>An accident has occurred in the mine and 
				toxic gas is escaping! Flee! Your bomb is your weapon. Throw it on 
				enemies, and catch it before it explodes. The longer you let it 
				fly, the more points it’ll give you, but this is at your own risk.`,
				img : "src/lib/assets/images/games/octoboom/thumbnail.png",
				preview : "./img/games/octoboom/screenshot2.png",
				trailer : null, //"https://www.youtube.com/embed/jb6uOKTxTlc",
				links : {
					"itch.io": "https://yolwoocle.itch.io/octoboom",
					"Ludum Dare 49 Submission": "https://ldjam.com/events/ludum-dare/49/octoboom",
				},
			}, 
			{
				cardType : "normal",
				
				label : "Chaser Of Dawn",
				description : "A game about looping around a planet. Made for a game jam.",
				longDescription : `<b>Chaser Of Dawn</b> is a game that was made for the Ludum Dare 47 game jam.
				We had 3 days to make a game based on the theme "Stuck in a loop", and we used the Pico-8 engine. The game was inspired by exoplanets that don't rotate and have a very big difference in temperature between their two sides.
				It was a lot of fun and we hope to do more games like this in the future!`,
				img : "src/lib/assets/images/games/chaserofdawn/chaserofdawn_miniature.png",
				preview : null,//"./img/games/chaserofdawn/chaserofdawn_1.png",
				trailer: "https://www.youtube.com/embed/XF79HG9XOaA",
				links: {
					"Ludum Dare 47 Submission": "https://ldjam.com/events/ludum-dare/47/chaser-of-dawn",
					"PICO-8 Forums": "https://www.lexaloffle.com/bbs/?tid=40733",
					"itch.io": "https://yolwoocle.itch.io/chaser-of-dawn",
				}
			}, 
		],
	];
</script>

<div class="w-full flex flex-col items-center">
	<div class="max-w-215 px-5 text-center text-(--main-very-dark)">
		<h1 class="font-black text-4xl pt-6 pb-4">Games</h1>
		<p class="text-xl">
			Here is a collection of some of my games. <br />
			Projects I am particularily proud of have a
			<span>
				<img
					src="src/lib/assets/icons/star_outlined.png"
					alt="star"
					class="star w-8 relative"
				/>
            </span> next to them.<br>
			You can find all projects on my <a class="card-link" href="https://yolwoocle.itch.io/">itch.io</a>.
		</p>
		<CardGrid cards={projects} cardWidth="240px" cardHeight="320px" />
	</div>
</div>

<style>
	.star {
		animation: constantRotation 8s linear infinite;
        display: inline-block;
	}

	@keyframes constantRotation {
		0% {
			transform: rotate(0);
		}
		100% {
			transform: rotate(360deg);
		}
	}
</style>
