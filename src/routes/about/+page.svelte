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
		<a
			class="navbar-brand text-2xl font-semibold"
			href="/photography"
			style="color: white;">Zach Niederstadt</a
		>
		<a class="nav-link ml-5" href="/portfolio" style="color: white;"
			>Portfolio</a
		>
	</nav>

	<header
		class="bg-cover bg-center min-h-screen flex flex-col justify-center items-center"
	>
		<div class="container mx-auto text-center">
			<br />
			<div
				class="bg-white bg-opacity-90 rounded-lg p-8 shadow-md max-w-3xl mx-auto"
			>
				<div class="flex justify-center">
					<img
						src="/images/profile.avif"
						alt="Zach Niederstadt"
						class="w-40 h-40 rounded-full object-cover mx-auto mb-4 shadow-lg"
					/>
				</div>
				<h2 class="text-3xl font-bold text-gray-800 mb-4">About Me</h2>
				<p class="text-gray-700 text-lg leading-relaxed mb-4">
					Hello! I'm Zach Niederstadt,
				</p>
				<p class="text-gray-700 text-lg leading-relaxed mb-4">...</p>
				<p class="text-gray-700 text-lg leading-relaxed mb-4">...</p>
				<p class="text-gray-700 text-lg leading-relaxed mb-4">
					Besides photography...
				</p>
				<p class="text-gray-700 text-lg leading-relaxed">
					Thank you for visiting my website :D
				</p>
			</div>
			<br />
		</div>
	</header>
	<p class="text-white text-center py-3" style="margin-top:-3rem">
		&copy; {year} Zach Niederstadt. All rights reserved.
	</p>
</main>
