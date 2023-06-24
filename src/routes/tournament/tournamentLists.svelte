<script lang="ts">
    import {
        Paginator,
        Table,
        type PaginationSettings,
    } from "@skeletonlabs/skeleton";
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
    const table_header = [
        "Name",
        "Game",
        "Prize Pool",
        "Platform",
        "Event Date",
    ];
    // PaginatorSettings
    let page = {
        offset: 0,
        limit: 5,
        size: tournaments.length,
        amounts: [1, 2, 3, 5, tournaments.length],
    } as PaginationSettings;
    $: sourceBodySliced = tournaments.slice(
        page.offset * page.limit,
        page.offset * page.limit + page.limit
    );
</script>

<main class="p-2 mt-3 rounded-xl table-container">
    <div class="w-full mt-3">
        <Table
            class="w-full mb-5"
            source={{
                head: table_header,
                body: sourceBodySliced.map((team) => [
                    team.name,
                    team.game,
                    team.prizePool,
                    team.platform,
                    team.eventDate.toString(),
                ]),
            }}
            interactive
            striped
            hover
        />
        <Paginator bind:settings={page} />
    </div>
</main>
