<script lang="ts">
    import type { PaginationSettings } from "@skeletonlabs/skeleton";
    import { Paginator, Table } from "@skeletonlabs/skeleton";
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
    const table_header = [
        "name",
        "Type",
        "prize Pool",
        "Platform",
        "Total Tournament",
    ];
    // PaginatorSettings
    let page = {
        offset: 0,
        limit: 5,
        size: games.length,
        amounts: [1, 2, 3, 5, games.length],
    } as PaginationSettings;

    $: sourceBodySliced = games.slice(
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
                body: sourceBodySliced.map((game) => [
                    game.name,
                    game.Type,
                    game.prizePool,
                    game.platform,
                    game.totalTournament.toString(),
                ]),
            }}
            interactive
            striped
            hover
        />
        <Paginator bind:settings={page} />
    </div>
</main>
