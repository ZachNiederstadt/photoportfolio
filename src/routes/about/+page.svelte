<script>
	import "$lib/global.css";
	import { fade, slide, fly } from "svelte/transition";
	const year = new Date().getFullYear();
</script>

<svelte:head>
	<title>About Me - Zach Niederstadt</title>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<meta property="og:title" content="Zach Niederstadt - About Me" />
	<meta
		property="og:description"
		content="Learn more about Zach Niederstadt, a passionate photographer specializing in Events, Weddings, and Portraiture."
	/>
	<meta property="og:image" content="/images/_DSC2618.avif" />
</svelte:head>

<main
	class="bg-cover bg-center content-center background"
	style="background-image: url('/images/profilebg.avif');"
>
	<nav
		class="bg-opacity-75 text-white p-4 absolute top-0 w-full flex justify-center items-center"
	>
		<a class="nav-link mr-5 other" href="/about" style="color: white;">About</a>
		<a
			class="navbar-brand text-4xl font-semibold font-orbitron text tracking-wider"
			href="/photography">ZN</a
		>
		<a class="nav-link ml-5 other" href="/portfolio" style="color: white;"
			>Portfolio</a
		>
	</nav>

	<header
		class="bg-cover bg-center min-h-screen flex flex-col justify-center items-center pt-10 pb-10 pr-5 pl-5"
	>
		<div
			class="container mx-auto text-center tracking-tight"
			transition:fly={{ x: -20, duration: 700 }}
		>
			<br />
			<div
				class="bg-stone-900 bg-opacity-70 rounded-lg p-8 shadow-2xl max-w-3xl mx-auto
				"
				transition:fade={{ duration: 700 }}
			>
				<div class="flex justify-center pb-5">
					<figure>
						<img
							src="/images/profile.avif"
							alt="Zach Niederstadt"
							class="w-40 h-40 rounded-full object-cover mx-auto mb-4 shadow-2xl"
						/>
					</figure>
				</div>
				<h2
					class="text-3xl font-bold font-orbitron text-white mb-10 tracking-wide"
				>
					Hi! I'm Zachary Niederstadt
				</h2>
				<p class="text-gray-200 text-lg leading-relaxed mb-4"></p>
				<p class="text-stone-200 text-sm leading-loose mb-4 tracking-wide">
					I'm someone who's loved photogrphy my whole life, and has recently
					started to learn how to use a camera with manual settings as well as
					fine tuning my editing and color grading skills using Adobe Lightroom.
					I also really enjoy the challenge of capturing motorsports at high
					speeds, and the challenge of trying to make a great background that's
					satisfying but not overpowering the subject, and creating a great
					subject that doesn't sit too seperately from the background.
				</p>
				<p class="text-stone-200 text-sm leading-loose mb-4 tracking-wide">
					---
				</p>
				<p
					class="text-stone-100 text-sm leading-loose mb-4 font-semibold tracking-wide"
				>
					Along with developing my skills, I hope to use photography and
					Psychology together to help remind people that you can find
					interesting perspectives that make life feel more exciting and
					stunning. As being a Psychology graduate, I hope to find as many
					aspects of life that I can to help ground people into healthier
					mindsets and persepectives of life. And I think in a chaotic world of
					hyper stimulations, the impact of photography to be something where
					you slow down, and think about about a single moment in time in a
					single spot for a bit is extremely healthy. Not to mention, if you can
					guide your creativity to find the calm in the chaos, or the beauty in
					the dull, it can help prepare you to take on those challenges in the
					mental health of your life too.
				</p>
				<p class="text-stone-200 text-sm leading-loose mb-4 tracking-wide">
					---
				</p>
				<p class="text-stone-200 text-sm leading-loose mb-4 tracking-wide">
					Besides photography and Psychology, I'm also a huge sports fan.
					Especially when you're talking about actually getting out there and
					playing, I'll play almost any sport if you ask. And that's one thing
					photography helps with as I enjoy watching sports, but the camera
					keeps my mind distracted from being bummed that I'm not participating.
					And with my experience, it's usually hard to keep me distracted as I
					played a year of college baseball and have participated in a Porsche
					Esports challenge event with Gran Turismo 7 (from the picture above
					with the creator), just to show my competitive nature. With the
					mention of Gran Turismo as well, I definitely love video games too. I
					really enjoy how they both constantly force me to push myself to learn
					and improve more, while also being a healthy space for my competitive
					side. And the biggest thing is that they're amazing for spending time
					with friends and staying connected. To quickly wrap things up, I love
					nature and expoloring this world we call home as well. I haven't been
					able to as much in the last few years though, but I used to find
					nature as one of the most healing places to be. I also used to love
					using nature as a photography playground with my phone at times.
				</p>
				<p
					class="flex justify-center text-[10px] text-white leading-relaxed pb- pt-2 tracking-widest"
				>
					[Profile Img.]From when I got to meet the Gran Turismo franchise
					creator
				</p>
				<a
					class="text-blue-500 text-sm"
					href="https://en.wikipedia.org/wiki/Kazunori_Yamauchi"
					>Kazunori Yamauchi</a
				>
			</div>
			<!-- <div class="flex justify-center gap-4 pt-5 mb-0" style="">
				<a
					href="https://www.instagram.com/niederdrifts/"
					class="bg-blue-900 text-white font-semibold py-3 w-[95px] flex justify-center
           rounded-lg shadow-md hover:bg-blue-600 hover:text-blue-800 h-[40px] flex justify-center items-center"
					style=""
				>
					Instagram
				</a>
				<a
					href="https://www.youtube.com/niederdrifts/"
					class="bg-blue-900 text-white font-semibold py-3 px-6 rounded-lg shadow-md hover:bg-blue-600 hover:text-blue-800 w-[95px] h-[40px] flex justify-center items-center"
					style=""
				>
					YouTube
				</a> -->
			<!-- </div> -->
			<br />
		</div>
	</header>
	<p class="text-white text-center py-3" style="margin-top:-3rem">
		&copy; {year} Zach Niederstadt. All rights reserved.
	</p>
</main>

<style>
	.text {
		text-shadow: 3px 3px 9px silver;
	}
	.other {
		text-shadow: 1.8px 1.8px 5px silver;
	}
</style>
