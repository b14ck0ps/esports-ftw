<script>
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
    $: console.log($page.route.id);
</script>

<body class="flex flex-col min-h-screen">
    <header class="bg-gray-900 text-white py-4">
        <!-- Navigation Bar -->
        <nav
            class="container mx-auto flex justify-normal items-center px-4 gap-4"
        >
            <div class="flex items-center">
                <!-- Logo -->
                <a href="/"><img class="w-44" src={logo} alt="Logo" /> </a>
            </div>
            <div class="flex items-center gap-10 ml-5 font-semibold">
                <!-- Navigation Links -->
                <a href="/tournament" class="text-gray-300 hover:text-[#48f955]"
                    >Tournament</a
                >
                <a href="/games" class="text-gray-300 hover:text-[#48f955]"
                    >Games</a
                >
                <a href="/teams" class="text-gray-300 hover:text-[#48f955]"
                    >Teams</a
                >
            </div>
        </nav>
    </header>

    {#if isEnoughScreenAvailable}
        <main class="flex-grow bg-gray-800 py-8">
            <!-- Main Content -->
            <slot />
        </main>
    {:else}
        <div class="flex-grow bg-gray-800 py-8">
            <p class="text-center text-white mt-[25vh]">
                Don't have enough time to make this responsive. <br /> Please
                use desktop or get a bigger screen to view this website.
                <span class="block mt-3"> - Dev Team 🫡 </span>
            </p>
        </div>
    {/if}

    <footer class="bg-gray-900 text-white py-4">
        <!-- Footer -->
        <div class="container mx-auto px-4">
            <p class="text-center">
                &copy; 2023 E-SPORTS FTW. All rights reserved.
            </p>
        </div>
    </footer>
</body>
