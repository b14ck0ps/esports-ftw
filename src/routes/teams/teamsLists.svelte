<script lang="ts">
    import { Table, tableMapperValues } from "@skeletonlabs/skeleton";
    import type { TableSource } from "@skeletonlabs/skeleton";
    const teams = [
        {
            name: "Team 1",
            game: "Valorant",
            prizePool: "$1000",
            totalGame: "10",
            location: "NYC",
        },
        {
            name: "Team 2",
            game: "Overwatch",
            prizePool: "$2000",
            totalGame: "10",
            location: "VBT",
        },
        {
            name: "Team 3",
            game: "League of Legends",
            prizePool: "$3000",
            totalGame: "10",
            location: "LA",
        },
        {
            name: "Team 4",
            game: "Dota 2",
            prizePool: "$4000",
            totalGame: "10",
            location: "NYC",
        },
        {
            name: "Team 5",
            game: "Counter-Strike: Global Offensive",
            prizePool: "$5000",
            totalGame: "10",
            location: "NYC",
        },
        {
            name: "Team 6",
            game: "Rainbow Six Siege",
            prizePool: "$6000",
            totalGame: "10",
            location: "NYC",
        },
        {
            name: "Team 7",
            game: "Fortnite",
            prizePool: "$7000",
            totalGame: "10",
            location: "NYC",
        },
        {
            name: "Team 8",
            game: "Apex Legends",
            prizePool: "$8000",
            totalGame: "10",
            location: "NYC",
        },
        {
            name: "Team 9",
            game: "Rocket League",
            prizePool: "$9000",
            totalGame: "10",
            location: "NYC",
        },
        {
            name: "Team 10",
            game: "Hearthstone",
            prizePool: "$10000",
            totalGame: "10",
            location: "NYC",
        },
    ];
    const teams_table: TableSource = {
        // A list of heading labels.
        head: ["Name", "Game", "Prize Pool", "Total Game", "Location"],
        // The data visibly shown in your table body UI.
        body: tableMapperValues(teams, [
            "name",
            "game",
            "prizePool",
            "totalGame",
            "location",
        ]),
    };
</script>

<main class="p-2 mt-3">
    <Table
        class="w-full mt-3 table-fixed"
        source={teams_table}
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
