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
  style="background-image: url('/images/backgrounds.jpg');"
  transition:fade={{ duration: 300 }}
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
    class="bg-cover bg-center flex flex-col justify-center items-center pt-5 pb-12 pr-5 pl-5"
  >
    <div
      class="h-lvh bg-center flex flex-col justify-top justify-between pt-[7%] items-center lg:pt-13"
    >
      <div
        class="container mx-auto text-center pt-12 sm:pt-8 md:pt-5 lg:pt-0 xl:pt-[-2]"
      >
        <h1
          class="text-5xl font-bold font-orbitron text-white tracking-wider"
          in:slide
          out:fade
        >
          Contact Me
        </h1>
        <p
          class="text-lg text-white mt-4 tracking-widest"
          style="color: white"
          out:fade
        >
          Feel free to reach out and ask questions
        </p>
        <br />
        <div class="mt-20">
          <div
            class="text-white font-orbitron text-sm pt-5 tracking-wider pt-10"
          >
            Email
          </div>
          <div class="text-white text-sm font-semibold pt-2">
            NiederstadtZ@gmail.com
          </div>
          <div class="text-white font-orbitron text-sm pt-7 tracking-wider">
            Mobile (text preffered at first)
          </div>
          <div class="text-white text-sm font-semibold pt-2">
            (214)-972-7846
          </div>
        </div>
      </div>
    </div>
  </header>
  <footer class="sticky mb-0">
    <div class="mt--3">
      <p class="text-white text-center py-3 pt-12" style="" in:fade out:fade>
        &copy; {year} Zach Niederstadt. All rights reserved.
      </p>
    </div>
  </footer>
</main>
