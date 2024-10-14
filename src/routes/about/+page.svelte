<script>
	import "$lib/global.css";
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
	class="bg-cover bg-center"
	style="background-image: url('/images/profilebg.avif');"
>
	<nav
		class="bg-opacity-75 text-white p-4 absolute top-0 w-full flex justify-center items-center"
	>
		<a class="nav-link mr-5" href="/about" style="color: white;">About</a>
		<a class="navbar-brand text-3xl font-semibold" href="/photography">ZN</a>
		<a class="nav-link ml-5" href="/portfolio" style="color: white;"
			>Portfolio</a
		>
	</nav>

	<header
		class="bg-cover bg-center min-h-screen flex flex-col justify-center items-center pt-10 pb-10 pr-5 pl-5"
	>
		<div class="container mx-auto text-center">
			<br />
			<div
				class="bg-stone-900 bg-opacity-90 rounded-lg p-8 shadow-2xl max-w-3xl mx-auto"
			>
				<div class="flex justify-center">
					<img
						src="/images/profile.avif"
						alt="Zach Niederstadt"
						class="w-40 h-40 rounded-full object-cover mx-auto mb-4 shadow-2xl"
					/>
				</div>
				<caption
					class="flex justify-center text-xs text-stone-300 leading-relaxed pb-3"
				>
					Me (right) with the Gran Turismo franchise creator, Kazunori Yamauchi</caption
				>
				<h2 class="text-3xl font-bold text-stone-400 mb-4">
					Hi! I'm Zachary Niederstadt,
				</h2>
				<p class="text-gray-200 text-lg leading-relaxed mb-4"></p>
				<p class="text-stone-200 text-sm leading-relaxed mb-4">
					I'm someone who's loved photogrphy my whole life, and has recently
					started to learn how to use a digital camera and mess with capture
					settings manually as well as how to edit and color grade using Adobe
					Lightroom. I really enjoy the challenge of capturing motorsports at
					high speeds, and the challenge of trying to make a great background
					that's not overpowering the the subject. I also enjoy the challenge
					that arises of trying to make the subject really pop without
					seperating it from the background and making it feel digitally
					created/edited.
				</p>
				<p class="text-gray-200 text-sm leading-relaxed mb-4">
					I also hope to use photography and Psychology together to help remind
					people you can find interesting perspectives in the most mundane
					areas. As being a Psychology graduate, I hope to find as many aspects
					of life I can to help ground people into healthier mindsets and
					persepectives of life. And I think in a chaotic world of hyper
					stimulations, the importance of photography to be something where you
					slow down, and think about about a single moment in time for a bit is
					extremely healthy. Not to mention, if you can take average places in
					the world, and guide your creativity to find the beauty in the dull,
					or the calm in the chaos, it can help prepare you to take on those
					challenges in the mental health of your life too.
				</p>
				<p class="text-gray-200 text-sm leading-relaxed mb-4">
					Besides photography and Psychology, I'm just a huge sports fan in
					general. Especially when you're talking about actually getting out
					there and playing. I'll play almost any sport if you ask. I also
					played a year of college baseball and was a part of a Porsche Esports
					challenge event with Gran Turismo 7 (from the picture above with the
					creator). I also just love nature and expoloring this world we call
					home as well.
				</p>
			</div>
			<br />
		</div>
	</header>
	<p class="text-white text-center py-3" style="margin-top:-3rem">
		&copy; {year} Zach Niederstadt. All rights reserved.
	</p>
</main>
