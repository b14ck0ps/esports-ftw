<script lang="ts">
    import { Table, tableMapperValues } from "@skeletonlabs/skeleton";
    import type { TableSource } from "@skeletonlabs/skeleton";
    const tournaments = [
        {
            name: "Tournament 1",
            game: "Valorant",
            prizePool: "$1000",
            platform: "PC",
            eventDate: "2022-01-01",
            isOngoing: true,
        },
        {
            name: "Tournament 2",
            game: "League of Legends",
            prizePool: "$500",
            platform: "PC",
            eventDate: "2022-02-14",
            isOngoing: true,
        },
        {
            name: "Tournament 3",
            game: "Dota 2",
            prizePool: "$2000",
            platform: "PC",
            eventDate: "2022-03-17",
            isOngoing: true,
        },
        {
            name: "Tournament 4",
            game: "Overwatch",
            prizePool: "$750",
            platform: "PC",
            eventDate: "2022-04-20",
            isOngoing: false,
        },
        {
            name: "Tournament 5",
            game: "Fortnite",
            prizePool: "$1500",
            platform: "PC",
            eventDate: "2022-05-23",
            isOngoing: false,
        },
        {
            name: "Tournament 6",
            game: "Apex Legends",
            prizePool: "$1000",
            platform: "PC",
            eventDate: "2022-06-26",
            isOngoing: false,
        },
        {
            name: "Tournament 7",
            game: "Rainbow Six Siege",
            prizePool: "$500",
            platform: "PC",
            eventDate: "2022-07-29",
            isOngoing: true,
        },
        {
            name: "Tournament 8",
            game: "Counter-Strike: Global Offensive",
            prizePool: "$2000",
            platform: "PC",
            eventDate: "2022-08-31",
            isOngoing: false,
        },
        {
            name: "Tournament 9",
            game: "Rocket League",
            prizePool: "$750",
            platform: "PC",
            eventDate: "2022-09-30",
            isOngoing: false,
        },
        {
            name: "Tournament 10",
            game: "Call of Duty: Warzone",
            prizePool: "$1500",
            platform: "PC",
            eventDate: "2022-10-31",
            isOngoing: false,
        },
    ];
    const tournament_table: TableSource = {
        // A list of heading labels.
        head: ["Name", "Prize Pool", "Platform", "Event Date"],
        // The data visibly shown in your table body UI.
        body: tableMapperValues(tournaments, [
            "name",
            "prizePool",
            "platform",
            "eventDate",
        ]),
    };
</script>

<main class="p-2 mt-3 rounded-xl table-container">
    <Table
        class="w-full mt-3 table-fixed"
        source={tournament_table}
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
