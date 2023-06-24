<script>
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
</script>

<main class="bg-gray-900 p-2 rounded-xl mt-3">
    <table class="w-full table-fixed mt-3">
        <thead>
            <tr>
                <th class="w-1/4 px-4 py-2 text-left text-gray-100">Name</th>
                <th class="w-1/4 px-4 py-2 text-left text-gray-100"
                    >Total Prize won</th
                >
                <th class="w-1/4 px-4 py-2 text-left text-gray-100"
                    >Total Games Played</th
                >
            </tr>
        </thead>
        <tbody>
            {#each teams as team, i}
                <tr class={i % 2 === 0 ? "bg-[#0d131f]" : "bg-[#111827]"}>
                    <td
                        class="px-4 py-2 text-gray-100 flex items-center justify-between"
                        ><div>
                            <p>{team.name}</p>
                            <p class="text-xs">
                                {team.game} , {team.location}
                            </p>
                        </div>
                    </td>
                    <td class="px-4 py-2 text-gray-100">{team.prizePool}</td>
                    <td class="px-4 py-2 text-gray-100">{team.totalGame}</td>
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
                    d="M10.707,5.293a1,1,0,0,1,0,1.414L7.414,10l3.293,3.293a1,1,0,1,1-1.414,1.414l-4-4a1,1,0,0,1,0-1.414l4-4a1,1,0,0,1,1.414,0Z"
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
