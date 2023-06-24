<script lang="ts">
    import { Table, tableMapperValues } from "@skeletonlabs/skeleton";
    import type { TableSource } from "@skeletonlabs/skeleton";
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
    const game_table: TableSource = {
        // A list of heading labels.
        head: ["name", "Type", "prize Pool", "Platform", "Total Tournament"],
        // The data visibly shown in your table body UI.
        body: tableMapperValues(games, [
            "name",
            "Type",
            "prizePool",
            "platform",
            "totalTournament",
        ]),
    };
</script>

<main class="p-2 mt-3">
    <Table
        class="w-full mt-3 table-fixed"
        source={game_table}
        interactive
        striped
        bordered
        hover
        small
    />
    <!-- pagination -->
    <div class="flex items-center justify-center mt-3">
        <button
            class="px-3 py-1 text-gray-100 bg-gray-800 rounded-l hover:bg-gray-700"
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                class="inline-block w-5 h-5"
                viewBox="0 0 20 20"
                fill="currentColor"
            >
                <path
                    fill-rule="evenodd"
                    d="M10.707,5.293a1,1,0,0,1,0,1.414L7.414,10l3.293,3.293a1,1,0,1,1-1.414,1.414l-4-4a1,1,0,0,1,0-1.414l4-4a1,1,0,0,1,1.414,0Z"
                    clip-rule="evenodd"
                />
            </svg>
        </button>
        <button class="px-3 py-1 text-gray-100 bg-gray-800 hover:bg-gray-700">
            1
        </button>
        <button class="px-3 py-1 text-gray-100 bg-gray-800 hover:bg-gray-700">
            2
        </button>
        <button class="px-3 py-1 text-gray-100 bg-gray-800 hover:bg-gray-700">
            3
        </button>
        <button class="px-3 py-1 text-gray-100 bg-gray-800 hover:bg-gray-700">
            4
        </button>
        <button
            class="px-3 py-1 text-gray-100 bg-gray-800 rounded-r hover:bg-gray-700"
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                class="inline-block w-5 h-5"
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
