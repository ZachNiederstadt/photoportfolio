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
          class="text-3xl font-bold font-orbitron text-white tracking-wider"
          in:slide
          out:fade
        >
          My personal social media accounts
        </h1>
        <p
          class="text-sm text-white mt-4 tracking-widest"
          style="color: white"
          out:fade
        >
          Sorry as these are not the most proffesionaly clean accounts (or with
          my Youtube the looks are just all over), but they're more to have fun
          and play with improving my creativity and editing skills from color
          grading to playing with mask tracking and transitions in videos, as
          well as trying to use my psychology degree to try and bring more
          inspiration to followers and other creators and influencers around me.
          At times too, it was just a way to help me through some huge struggles
          in life by using it as something I could consider productive that also
          helped me get through hard head spaces. Also they are in general more
          targeted for adult audiences.
        </p>
        <br />
        <div class="pt-7" out:slide>
          <a
            class="btn btn-primary btn-lg mt-4 px-8 py-2 text-white font-orbitron text-sm tracking-widest font-semibold rounded-full bg-stone-700 hover:bg-gray-800 transition duration-300 ease-in-out"
            style="color: white"
            href="https://www.instagram.com/niederdrifts/"
          >
            Instagram
          </a>
        </div>
        <div class="pt-7" out:slide>
          <a
            class="btn btn-primary btn-lg mt-4 px-8 py-2 text-white font-orbitron text-sm tracking-widest font-semibold rounded-full bg-stone-700 hover:bg-gray-800 transition duration-300 ease-in-out"
            style="color: white"
            href="https://www.youtube.com/channel/UC7L0yEcXbPlPuy2spcKUEGg"
          >
            YouTube
          </a>
        </div>
        <div class="pt-7" out:slide>
          <a
            class="btn btn-primary btn-lg mt-4 px-8 py-2 text-white font-orbitron text-sm tracking-widest font-semibold rounded-full bg-stone-700 hover:bg-gray-800 transition duration-300 ease-in-out"
            style="color: white"
            href="https://www.tiktok.com/@niederdrifts?lang=en"
          >
            Tik Tok
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
