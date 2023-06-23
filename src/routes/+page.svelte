<script>
    import oracle from "$lib/assets/icons/oracle.png";
    import dotnet from "$lib/assets/icons/dotnetseven.webp";
    import svelte from "$lib/assets/icons/svelte.svg";
    import logo from "$lib/assets/icons/logo.png";
    import RecentTournaments from "./RecentTournaments.svelte";
    import UpcomminTournament from "./upcomminTournament.svelte";
    import TopGames from "./TopGames.svelte";
</script>

<head>
    
</head>
<main>
    <div class="gradient p-10 w-3/4 m-auto rounded-t-lg">
        <div class="flex flex-col justify-center items-center">
            <h1 class="text-3xl font-semibold text-center my-3 mb-8">
                Everything about the esports popularity
            </h1>
            <p class="text-center w-[1000px]">
                Esports FTW is not just another analytical service. We are a
                team of passionate gamers and esports enthusiasts who are
                dedicated to exploring the development of esports. Our service
                is designed to make esports more honest and clear, helping
                sponsors, organizers, and fans alike to better understand the
                industry. With our cutting-edge technology and expert analysis,
                we provide a unique perspective on the world of esports that you
                won't find anywhere else. Whether you're a casual fan or a
                seasoned pro, Esports FTW has something for everyone. Join us
                today and discover the future of esports!
            </p>
            <div class="mt-10 flex gap-3 justify-center items-center">
                <a href="/">
                    <div
                        class="bg-[#091523] py-3 px-6 rounded-full font-semibold flex justify-center items-center gap-2 opacity-90 hover:cursor-pointer hover:scale-105 transition"
                    >
                        <img class="w-5 inline-block" src={logo} alt="log" />
                        Esports FTW
                    </div>
                </a>
                <p class="font-bold text-2xl">=</p>
                <a
                    href="https://github.com/wnameless/docker-oracle-xe-11g"
                    target="_blank"
                >
                    <div
                        class="bg-[#091523] py-3 px-6 rounded-full font-semibold flex items-center justify-normal gap-2 opacity-90 hover:cursor-pointer hover:scale-105 transition"
                    >
                        <img
                            class="inline-block h-6 mr-2"
                            src={oracle}
                            alt=""
                            srcset=""
                        />
                        Oracle 11G
                    </div>
                </a>
                <p class="font-bold text-2xl">+</p>
                <a
                    href="https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-7"
                    target="_blank"
                >
                    <div
                        class="bg-[#091523] py-3 px-8 rounded-full font-semibold opacity-90 flex items-center justify-center hover:cursor-pointer hover:scale-105 transition"
                    >
                        <img
                            class="inline-block h-6 mr-2"
                            src={dotnet}
                            alt=""
                            srcset=""
                        />
                        Dot Net 7.0
                    </div>
                </a>
                <p class="font-bold text-2xl">+</p>
                <a href="https://kit.svelte.dev/" target="_blank">
                    <div
                        class="bg-[#091523] py-3 px-8 rounded-full font-semibold opacity-90 flex items-center justify-center hover:cursor-pointer hover:scale-105 transition"
                    >
                        <img
                            class="inline-block w-8 mr-2"
                            src={svelte}
                            alt=""
                            srcset=""
                        />
                        SvelteKit
                    </div>
                </a>
            </div>
        </div>
    </div>
    <div
        class="bg-gray-900 w-3/4 m-auto rounded-b-lg flex items-center justify-between"
    >
        <div class="flex gap-8 items-center p-5">
            <p>Our Database Incluses:</p>
        </div>
        <div
            class="flex justify-between gap-8 items-center p-5 border-l-2 border-y-0 border-collapse border-gray-700 hover:cursor-pointer hover:bg-gray-700 flex-grow"
        >
            <div>
                <p class="text-xl font-semibold">12 00</p>
                <p>{"Tournaments & events".toUpperCase()}</p>
            </div>
            <i class="fa-solid fa-arrow-right" />
        </div>
        <div
            class="flex justify-between gap-8 items-center p-5 border-l-2 border-y-0 border-collapse border-gray-700 hover:cursor-pointer hover:bg-gray-700 flex-grow"
        >
            <div>
                <p class="text-xl font-semibold">600</p>
                <p>{"games".toUpperCase()}</p>
            </div>
            <i class="fa-solid fa-arrow-right" />
        </div>
        <div
            class="flex justify-between gap-8 items-center p-5 border-l-2 border-y-0 border-collapse border-gray-700 hover:cursor-pointer hover:bg-gray-700 flex-grow"
        >
            <div>
                <p class="text-xl font-semibold">21 000</p>
                <p>{"players".toUpperCase()}</p>
            </div>
            <i class="fa-solid fa-arrow-right" />
        </div>
        <div
            class="flex justify-between gap-8 items-center p-5 border-l-2 border-y-0 border-collapse border-gray-700 hover:cursor-pointer hover:bg-gray-700 flex-grow"
        >
            <div>
                <p class="text-xl font-semibold">769</p>
                <p>{"teams".toUpperCase()}</p>
            </div>
            <i class="fa-solid fa-arrow-right" />
        </div>
    </div>
    <div class="flex justify-between w-3/4 m-auto mt-10">
        <RecentTournaments />
        <UpcomminTournament />
        <TopGames />
    </div>
    <!-- section for recent items -->
</main>

<style>
    main {
        color: white;
        font-family: "Poppins", sans-serif;
    }

    .gradient {
        background-image: linear-gradient(to right, #6a11cb 0%, #2575fc 100%);
    }
</style>
