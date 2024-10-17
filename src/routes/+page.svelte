<script>
  import "$lib/global.css";
  import { fade } from "svelte/transition";
</script>

<svelte:head>
  <title>ZN</title>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</svelte:head>

<div
  class="absolute inset-0 bg-gradient-to-r from-transparent via-blue-400 to-blue-950 bg-[length:1200%_1200%] animate-gradient-animate z-[-1]"
  transition:fade={{ duration: 250 }}
></div>

<div
  class="flex items-center justify-center min-h-screen max-w-screen px-4 py-12 bg-black bg-opacity-50"
  transition:fade={{ duration: 250 }}
>
  <div class="text-center max-w-3xl w-full">
    <h1 class="text-4xl sm:text-5xl font-extrabold text-white mb-0">
      Welcome!
    </h1>

    <p
      class="text-base sm:text-lg text-white mb-8 sm:mb-6 pt-5"
      transition:fade={{ duration: 250 }}
    >
      Check out my work
    </p>
    <div class="flex justify-center gap-2 mb-12">
      <a
        href="/photography"
        class="bg-blue-900 text-white font-semibold py-3 px-6 rounded-lg shadow-md hover:bg-blue-600 transition duration-300 hover:text-blue-800 w-[110px] h-[40px] flex justify-center items-center"
        transition:fade={{ duration: 250 }}
      >
        Photography
      </a>
      <a
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
      </a>
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
    animation: gradientAnimation 15s ease infinite;
  }
</style>
