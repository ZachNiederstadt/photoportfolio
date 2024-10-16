<script>
  import "$lib/global.css";

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
>
  <nav
    class="bg-opacity-75 text-white p-4 absolute top-0 w-full flex justify-center items-center"
  >
    <a class="nav-link mr-5" href="/about" style="color: white;">About</a>
    <a
      class="navbar-brand text-4xl font-semibold font-orbitron"
      href="/photography"
      style=" color: white;">ZN</a
    >
    <a class="nav-link ml-5" href="/portfolio" style="color: white;"
      >Portfolio</a
    >
  </nav>

  <div
    class="bg-cover bg-center min-h-screen flex flex-col justify-top justify-between pt-[7%] items-center lg:pt-13"
  >
    <div class="container mx-auto text-center pt-12 md:pt-5 lg:pt-2 xl:pt-0">
      <h1 class="text-3xl font-bold font-orbitron text-white tracking-wider">
        Zach Niederstadt
      </h1>
      <p
        class="text-md font-semibold text-white mt-4 tracking-widest"
        style="color: white"
      >
        Capturing life as it flies by.
      </p>
      <br />
      <div class="pt-5 md:pt-0">
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
      <div class="flex justify-center gap-10 pb- mb-5" style="">
        <a
          href="https://www.instagram.com/niederdrifts/"
          class="bg-blue-900 text-white font-semibold py-3 px-6 rounded-lg shadow-md hover:bg-blue-600 hover:text-blue-800"
          style=""
        >
          Instagram
        </a>
        <a
          href="https://www.youtube.com/niederdrifts/"
          class="bg-blue-900 text-white font-semibold py-3 px-6 rounded-lg shadow-md hover:bg-blue-600 hover:text-blue-800"
          style=""
        >
          YouTube
        </a>
      </div>
      <div class="mt--3">
        <p class="text-white text-center py-3 pt-12" style="">
          &copy; {year} Zach Niederstadt. All rights reserved.
        </p>
      </div>
    </footer>
  </div>
</main>

<style>
  .bg-cover {
    transition: background-image 1.5s ease-in-out;
  }
</style>
