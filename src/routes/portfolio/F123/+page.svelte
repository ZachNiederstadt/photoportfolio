<script>
    import "$lib/global.css";
    import { onMount } from "svelte";

    let collections = [
        {
            name: "F1 2023",
            images: [
                "/images/F1/image-1.avif",
                "/images/F1/image-4.avif",
                "/images/F1/image-2.avif",
                "/images/F1/image-3.avif",
                "/images/F1/image-6.avif",
                "/images/F1/image-9.avif",
                "/images/F1/image-8.avif",
                "/images/F1/image-5.avif",
                "/images/F1/image-7.avif",
                "/images/F1/image-10.avif",
                "/images/F1/image-15.avif",
                "/images/F1/image-11.avif",
            ],
        },
    ];
    let backgroundImage = "";
    let fullscreen = false;
    let imgElement;

    onMount(() => {
        const randomIndex = Math.floor(
            Math.random() * collections[0].images.length,
        );
        backgroundImage = `url('${collections[0].images[randomIndex]}')`;

        document.body.style.backgroundImage = backgroundImage;
        document.body.style.backgroundSize = "cover";
        document.body.style.backgroundRepeat = "no-repeat";
    });
    const year = new Date().getFullYear();
    function toggleFullScreen(imageUrl) {
        if (!fullscreen) {
            imgElement = document.createElement("img");
            imgElement.src = imageUrl;
            imgElement.style.position = "fixed";
            imgElement.style.top = "0";
            imgElement.style.left = "0";
            imgElement.style.width = "100%";
            imgElement.style.height = "100%";
            imgElement.style.zIndex = "9999";
            imgElement.style.cursor = "zoom-out";
            imgElement.addEventListener("click", exitFullScreen);

            document.body.appendChild(imgElement);

            if (imgElement.requestFullscreen) {
                imgElement.requestFullscreen();
            } else if (imgElement.webkitRequestFullscreen) {
                imgElement.webkitRequestFullscreen();
            } else if (imgElement.msRequestFullscreen) {
                imgElement.msRequestFullscreen();
            }

            fullscreen = true;
        } else {
            exitFullScreen();
        }
    }

    function exitFullScreen() {
        if (document.exitFullscreen) {
            document.exitFullscreen();
        } else if (document.webkitExitFullscreen) {
            document.webkitExitFullscreen();
        } else if (document.msExitFullscreen) {
            document.msExitFullscreen();
        }

        imgElement.parentNode.removeChild(imgElement);
        fullscreen = false;
    }
</script>

<svelte:head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Twilight Toboganning - Zach Niederstadt</title>
    <meta
        property="og:title"
        content="Twilight Toboganning - Zach Niederstadt"
    />
    <meta
        property="og:description"
        content="Shoot for Mendip Activity Centers Twilight Toboganning"
    />
    <meta property="og:image" content="/images/_DSC2618.avif" />
</svelte:head>

<div>
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

    <section id="portfolio" class="py-5">
        <div class="container mx-auto mt-20 text-center">
            <h1 class="text-5xl font-bold text-white mb-4">F1 2023 COTA</h1>
            <p class="text-lg font-bold text-white mb-8">
                My view from the Legendary Cota S section
            </p>
            <div
                class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4"
            >
                {#each collections[0].images as image, index}
                    <div class="content-center">
                        <img
                            src={image}
                            alt={`Image ${index + 1}`}
                            class="w-full h-auto cursor-pointer shadow-sm rounded-lg"
                            on:click={() => toggleFullScreen(image)}
                        />
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <footer class="text-white text-center py-3">
        &copy; {year} Zach Niederstadt. All rights reserved.
    </footer>
</div>
