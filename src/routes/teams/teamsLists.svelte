<script lang="ts">
    import { Paginator, Table } from "@skeletonlabs/skeleton";
    import type { PaginationSettings } from "@skeletonlabs/skeleton";

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
    const table_header = [
        "Name",
        "Game",
        "Prize Pool",
        "Total Game",
        "Location",
    ];

    // PaginatorSettings
    let page = {
        offset: 0,
        limit: 5,
        size: teams.length,
        amounts: [1, 2, 3, 5, teams.length],
    } as PaginationSettings;
    $: sourceBodySliced = teams.slice(
        page.offset * page.limit,
        page.offset * page.limit + page.limit
    );
</script>

<main class="p-2 mt-3">
    <div class="w-full mt-3">
        <Table
            class="w-full mb-5"
            source={{
                head: table_header,
                body: sourceBodySliced.map((team) => [
                    team.name,
                    team.game,
                    team.prizePool,
                    team.totalGame,
                    team.location,
                ]),
            }}
            interactive
            striped
            hover
        />
        <Paginator bind:settings={page} />
    </div>
</main>
