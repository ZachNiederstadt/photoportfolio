<script>
  import "$lib/global.css";
  import { fade } from "svelte/transition";
</script>

<svelte:head>
  <title>ZN</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</svelte:head>

<!-- whole page background -->
<div
  class="bg-cover bg-center"
  style="background-image: url('/images/welcome.avif');"
>
  <div
    class="flex items-center justify-center inset-0 z-[-1] h-dvh"
    transition:fade={{ duration: 250 }}
  >
    <!--bg-gradient-to-r from-transparent via-blue-950 bg-[length:20000%_50%] animate-gradient-animate -->
    <!-- contents welcome etc...does not need a height -->
    <div
      class="m-auto flex px-4 py-12 bg-opacity-100"
      transition:fade={{ duration: 250 }}
    >
      <div class="text-center max-w-3xl w-full">
        <h1 class="text-4xl sm:text-5xl font-extrabold text-white mb-0">
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
            style=""
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
        <!-- <a
          href="https://github.com/ZachNiederstadt"
          target="_blank"
          class="bg-blue-600 text-white font-semibold py-3 px-6 rounded-lg shadow-md hover:bg-blue-400 transition duration-300 hover:text-blue-500 w-[110px] h-[40px] flex justify-center items-center"
          transition:fade={{ duration: 250 }}
        >
          Github
        </a>
        <a
          href="https://docs.google.com/document/d/1rVgljEEaeOdQa3Y7yF_dapNw2Kt7qeqOZVkeqAEnwkA/edit?usp=sharing"
          target="_blank"
          class=" bg-blue-300 text-white font-semibold py-3 px-6 rounded-lg shadow-md hover:bg-blue-100 hover:text-blue-400 transition duration-300 w-[110px] h-[40px] flex justify-center items-center"
          transition:fade={{ duration: 250 }}
        >
          Resume
        </a> -->
      </div>
    </div>
  </div>
</div>

<!-- Tailwind CSS Custom Animation -->
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
