<script>
    import "@skeletonlabs/skeleton/themes/theme-skeleton.css";
    import "@skeletonlabs/skeleton/styles/skeleton.css";
    import "../app.css";

    import logo from "$lib/assets/logo-with-text.png";
    import { onMount } from "svelte";
    import { page } from "$app/stores";

    let isEnoughScreenAvailable = true;

    onMount(() => {
        // Function to check screen resolution
        function checkScreenResolution() {
            isEnoughScreenAvailable =
                window.innerWidth >= 1440 && window.innerHeight >= 300;
        }

        // Initial check on component mount
        checkScreenResolution();

        // Listen for window resize and re-check the screen resolution
        window.addEventListener("resize", checkScreenResolution);

        return () => {
            // Cleanup: remove event listener on component unmount
            window.removeEventListener("resize", checkScreenResolution);
        };
    });
    $: routeId = $page.route.id;
</script>

<body class="flex flex-col min-h-screen">
    <header
        class="flex items-center justify-between py-4 text-white bg-gray-900"
    >
        <!-- Navigation Bar -->
        <nav
            class="container flex items-center gap-4 px-4 mx-auto justify-normal"
        >
            <div class="flex items-center">
                <!-- Logo -->
                <a href="/"><img class="w-44" src={logo} alt="Logo" /> </a>
            </div>
            <div class="flex items-center gap-10 ml-5 font-semibold">
                <!-- Navigation Links -->
                <a
                    href="/tournament"
                    class="{routeId === '/tournament'
                        ? 'text-green-ftw'
                        : 'text-gray-300'}  hover:text-green-ftw">Tournament</a
                >
                <a
                    href="/games"
                    class="{routeId === '/games'
                        ? 'text-green-ftw'
                        : 'text-gray-300'}  hover:text-green-ftw">Games</a
                >
                <a
                    href="/teams"
                    class="{routeId === '/teams'
                        ? 'text-green-ftw'
                        : 'text-gray-300'}  hover:text-green-ftw">Teams</a
                >
            </div>
        </nav>
        <a
            href="/login"
            class="hover:text-green-ftw px-4 py-2 rounded-md mr-5 border hover:border-green-ftw font-semibold {routeId ===
            '/login'
                ? 'text-green-ftw  border-green-ftw'
                : ' border-transparent'} ">Login</a
        >
    </header>

    {#if isEnoughScreenAvailable}
        <main class="flex-grow py-8 bg-gray-800">
            <!-- Main Content -->
            <slot />
        </main>
    {:else}
        <div class="flex-grow py-8 bg-gray-800">
            <p class="text-center text-white mt-[25vh]">
                Don't have enough time to make this responsive. <br /> Please
                use desktop or get a bigger screen to view this website.
                <span class="block mt-3"> - Dev Team 🫡 </span>
            </p>
        </div>
    {/if}

    <footer class="py-4 text-white bg-gray-900">
        <!-- Footer -->
        <div class="container px-4 mx-auto">
            <p class="text-center">
                &copy; 2023 E-SPORTS FTW. All rights reserved.
            </p>
        </div>
    </footer>
</body>
