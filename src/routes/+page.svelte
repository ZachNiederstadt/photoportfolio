<script>
  import "$lib/global.css";
  import { fade, slide } from "svelte/transition";

  // Create a reactive statement to handle screen orientation
  let isPortrait = false;

  if (typeof window !== "undefined") {
    // Initial check
    isPortrait =
      window.matchMedia("(orientation: portrait)").matches ||
      window.matchMedia("(max-width: 768px)").matches;

    // Listen for changes
    window
      .matchMedia("(orientation: portrait)")
      .addEventListener("change", (e) => {
        isPortrait = e.matches;
      });

    window.matchMedia("(max-width: 768px)").addEventListener("change", (e) => {
      isPortrait = e.matches;
    });
  }
</script>

<svelte:head>
  <title>ZN</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</svelte:head>

<!-- whole page background -->
<div
  class="bg-cover bg-center"
  style="background-image: url({isPortrait
    ? '/images/welcome-portrait.avif'
    : '/images/welcome.avif'});"
>
  <div
    class="flex items-center justify-center inset-0 z-[-1] h-dvh"
    transition:fade={{ duration: 250 }}
  >
    <div
      class="m-auto flex px-4 py-12 bg-opacity-100"
      transition:fade={{ duration: 250 }}
    >
      <div class="text-center max-w-3xl w-full">
        <h1
          class="text-4xl sm:text-5xl font-extrabold text-white mb-0 font-orbitron"
        >
          Welcome!
        </h1>
        <p
          class="text-base sm:text-lg text-white mb-8 sm:mb-7 pt-5 pb-20"
          transition:fade={{ duration: 250 }}
        >
          Check out my work
        </p>
        <div class="pt-20" out:slide>
          <a
            class="btn mt-5 px-7 py-3 text-white font-orbitron text-sm tracking-widest font-semibold rounded-full bg-blue-950 hover:bg-blue-400 transition duration-300 ease-in-out"
            href="photography"
            target="_blank"
          >
            Photography
          </a>
        </div>
        <div class="pt-8" out:slide>
          <a
            class="btn mt-5 px-8 py-3 text-white font-orbitron text-sm tracking-widest font-semibold rounded-full bg-blue-950 hover:bg-blue-400 transition duration-300 ease-in-out"
            style="color: white"
            href="/socials"
            target="_blank"
          >
            Socials
          </a>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  @keyframes gradientAnimation {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }
  .animate-gradient-animate {
    animation: gradientAnimation 20s ease infinite;
  }
</style>
