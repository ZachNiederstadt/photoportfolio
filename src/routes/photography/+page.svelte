<script>
  import "$lib/global.css";
  import { fade, slide } from "svelte/transition";
  import { inject } from "@vercel/analytics";

  const year = new Date().getFullYear();
</script>

<svelte:head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Zach Niederstadt - Photographer</title>
  <meta property="og:title" content="Zach Niederstadt - Photographer" />
  <meta
    property="og:description"
    content="Hey! I'm Leo, a photographer with experience in Events, Landscape and Street!"
  />
  <meta property="og:image" content="" />
  <link rel="preload" href="/images/test.avif" as="image" />
</svelte:head>

<main
  class="bg-cover bg-center content-center"
  style="background-image: url('/images/test.avif');"
  transition:fade={{ duration: 300 }}
>
  <nav
    class="bg-opacity-75 text-white p-4 absolute top-0 w-full flex justify-center items-center"
  >
    <a class="nav-link mr-5 other" href="/about" style="color: white;">About</a>
    <a
      class="navbar-brand text-4xl font-semibold font-orbitron text tracking-wider"
      href="/">ZN</a
    >
    <a class="nav-link ml-5 other" href="/portfolio" style="color: white;"
      >Portfolio</a
    >
  </nav>
  <header
    class="bg-cover bg-center min-h-screen flex flex-col justify-center items-center pt-7 pb-12 pr-5 pl-5"
  >
    <div
      class="bg-cover bg-center min-h-screen flex flex-col justify-top justify-between pt-[2%] items-center"
    >
      <div
        class="container mx-auto text-center pt-8 sm:pt-6 md:pt-8 lg:pt-5 xl:pt-5"
      >
        <h1
          class="text-3xl font-bold font-orbitron text-white tracking-wider"
          in:slide
          out:fade
        >
          Zach Niederstadt
        </h1>
        <p
          class="text-md font-semibold text-white mt-4 tracking-widest"
          style="color: white"
          out:fade
        >
          Capturing life as it flies by.
        </p>
        <p
          class="text-xs font-semibold text-white mt-1 tracking-widest"
          style="color: white"
          out:fade
        >
          Shot on Canon T1i
        </p>
        <br />
        <div class="pt-5 md:pt-0" out:slide>
          <a
            class="btn btn-primary btn-lg mt-4 px-8 py-2 text-white font-orbitron text-sm tracking-widest font-semibold rounded-full bg-stone-700 hover:bg-gray-800 transition duration-300 ease-in-out"
            style="color: white"
            href="/portfolio"
          >
            Explore Portfolio
          </a>
        </div>
      </div>
      <footer class="sticky mb-0">
        <div class="mt--3">
          <p
            class="text-white text-center py-3 pt-12"
            style=""
            in:fade
            out:fade
          >
            &copy; {year} Zach Niederstadt. All rights reserved.
          </p>
        </div>
      </footer>
    </div>
  </header>
</main>
