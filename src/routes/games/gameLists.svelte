<script>
    const games = [
        {
            name: "Valorant",
            Type: "FPS",
            platform: "PC",
            prizePool: "$1000",
            totalTournament: 10,
            isOngoing: true,
        },
        {
            name: "League of Legends",
            Type: "MOBA",
            platform: "PC",
            prizePool: "$5000",
            totalTournament: 20,
            isOngoing: true,
        },
        {
            name: "Fortnite",
            Type: "Battle Royale",
            platform: "PC",
            prizePool: "$2000",
            totalTournament: 15,
            isOngoing: true,
        },
        {
            name: "Overwatch",
            Type: "FPS",
            platform: "PC",
            prizePool: "$3000",
            totalTournament: 12,
            isOngoing: false,
        },
        {
            name: "Dota 2",
            Type: "MOBA",
            platform: "PC",
            prizePool: "$8000",
            totalTournament: 25,
            isOngoing: true,
        },
        {
            name: "Apex Legends",
            Type: "Battle Royale",
            platform: "PC",
            prizePool: "$1500",
            totalTournament: 8,
            isOngoing: false,
        },
        {
            name: "Counter-Strike: Global Offensive",
            Type: "FPS",
            platform: "PC",
            prizePool: "$6000",
            totalTournament: 18,
            isOngoing: false,
        },
        {
            name: "Rainbow Six Siege",
            Type: "FPS",
            platform: "PC",
            prizePool: "$4000",
            totalTournament: 14,
            isOngoing: false,
        },
        {
            name: "Rocket League",
            Type: "Sports",
            platform: "PC",
            prizePool: "$2500",
            totalTournament: 10,
            isOngoing: false,
        },
        {
            name: "FIFA 22",
            Type: "Sports",
            platform: "PC",
            prizePool: "$3500",
            totalTournament: 16,
            isOngoing: false,
        },
    ];
</script>

<main class="bg-gray-900 p-2 rounded-xl mt-3">
    <table class="w-full table-fixed mt-3">
        <thead>
            <tr>
                <th class="w-6"><i class="fa-solid fa-list" /></th>
                <th class="w-1/4 px-4 py-2 text-left text-gray-100">Name</th>
                <th class="w-1/4 px-4 py-2 text-left text-gray-100">Type</th>
                <th class="w-1/4 px-4 py-2 text-left text-gray-100"
                    >Prize Pool</th
                >
                <th class="w-1/4 px-4 py-2 text-left text-gray-100">Platform</th
                >
                <th class="w-1/6 px-4 py-2 text-gray-100 text-right"
                    >Total Tournament</th
                >
            </tr>
        </thead>
        <tbody>
            {#each games as game, i}
                <tr class={i % 2 === 0 ? "bg-[#0d131f]" : "bg-[#111827]"}>
                    <td>
                        {i + 1}
                    </td>
                    <td
                        class="px-4 py-2 text-gray-100 flex items-center justify-between"
                        ><div>
                            <p>{game.name}</p>
                        </div>
                    </td><td class="px-4 py-2 text-gray-100">{game.Type}</td>
                    <td class="px-4 py-2 text-gray-100">{game.prizePool}</td>
                    <td class="px-4 py-2 text-gray-100">{game.platform}</td>
                    <td class="px-4 py-2 text-gray-100 text-right">
                        {#if game.isOngoing}<span
                                class="text-white rounded font-semibold bg-green-400 px-2 py-[1px] text-[.6em] bg-opacity-40"
                                >On Going: 1</span
                            > /{/if}
                        {game.totalTournament}</td
                    >
                </tr>
            {/each}
        </tbody>
    </table>
    <!-- pagination -->
    <div class="flex items-center justify-center mt-3">
        <button
            class="bg-gray-800 text-gray-100 px-3 py-1 rounded-l hover:bg-gray-700"
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 inline-block"
                viewBox="0 0 20 20"
                fill="currentColor"
            >
                <path
                    fill-rule="evenodd"
                    d="M10.707,5.293a1,1,0,0,1,1.414,0l4,4a1,1,0,0,1,0,1.414l-4,4a1,1,0,0,1-1.414-1.414L12.586,10,10.707,7.121A1,1,0,0,1,10.707,5.293Z"
                    clip-rule="evenodd"
                />
            </svg>
        </button>
        <button class="bg-gray-800 text-gray-100 px-3 py-1 hover:bg-gray-700">
            1
        </button>
        <button class="bg-gray-800 text-gray-100 px-3 py-1 hover:bg-gray-700">
            2
        </button>
        <button class="bg-gray-800 text-gray-100 px-3 py-1 hover:bg-gray-700">
            3
        </button>
        <button class="bg-gray-800 text-gray-100 px-3 py-1 hover:bg-gray-700">
            4
        </button>
        <button
            class="bg-gray-800 text-gray-100 px-3 py-1 rounded-r hover:bg-gray-700"
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 inline-block"
                viewBox="0 0 20 20"
                fill="currentColor"
            >
                <path
                    fill-rule="evenodd"
                    d="M9.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 11-1.414-1.414L12.586 10 9.293 6.707a1 1 0 010-1.414z"
                    clip-rule="evenodd"
                />
            </svg>
        </button>
    </div>
</main>
