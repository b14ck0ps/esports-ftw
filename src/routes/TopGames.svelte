<script>
    /* random generated data  */
    let t_games = [
        {
            name: "Valorant",
            publisher: "Riot Games",
            platform: "PC",
            pricePool: "$ 234K",
        },
        {
            name: "Overwatch",
            publisher: "Blizzard Entertainment",
            platform: "PC",
            pricePool: "$ 333K",
        },
        {
            name: "Fortnite",
            publisher: "Epic Games",
            platform: "PC",
            pricePool: "$ 69K",
        },
        {
            name: "Apex Legends",
            publisher: "Electronic Arts",
            platform: "PC",
            pricePool: "$ 20K",
        },
    ];
</script>

<main>
    <div class="flex items-center justify-between">
        <div>
            <!--Header-->
            <div class="flex items-center gap-20">
                <div class="flex items-center gap-3">
                    <i
                        class="p-2 bg-gray-900 rounded-lg fa-solid fa-clock-rotate-left"
                    />
                    <p class="font-bold">Top Games</p>
                </div>
                <div
                    class="flex items-center gap-4 px-4 py-2 text-sm transition-all bg-gray-900 rounded-lg cursor-pointer hover:bg-gray-700"
                >
                    <p>More</p>
                    <i class="fa-solid fa-arrow-right" />
                </div>
            </div>
            <div class="mt-2">
                <!--lists, get this list from API-->
                {#each t_games as game}
                    <div
                        class="flex justify-between p-3 mb-2 transition-all bg-gray-900 cursor-pointer rounded-xl hover:scale-x-105"
                    >
                        <div>
                            <div class="flex items-center gap-3">
                                <svg
                                    class="w-12 h-12"
                                    xmlns="http://www.w3.org/2000/svg"
                                    enable-background="new 0 0 128 128"
                                    viewBox="0 0 128 128"
                                    id="pc"
                                    ><path
                                        fill="#505070"
                                        d="M76 77.98H12c-3.309 0-6-2.691-6-6v-36c0-3.309 2.691-6 6-6h64c3.309 0 6 2.691 6 6v36c0 3.309-2.691 6-6 6zm-64-44c-1.103 0-2 .897-2 2v36c0 1.103.897 2 2 2h64c1.103 0 2-.897 2-2v-36c0-1.103-.897-2-2-2H12z"
                                    /><path
                                        fill="#505070"
                                        d="M44 92a2 2 0 0 1-2-2V76a2 2 0 0 1 4 0v14a2 2 0 0 1-2 2z"
                                    /><path
                                        fill="#505070"
                                        d="M56 92H32a2 2 0 0 1 0-4h24a2 2 0 0 1 0 4zM116 92h-16c-3.309 0-6-2.691-6-6V36c0-3.309 2.691-6 6-6h16c3.309 0 6 2.691 6 6v50c0 3.309-2.691 6-6 6zm-16-58c-1.103 0-2 .897-2 2v50c0 1.103.897 2 2 2h16c1.103 0 2-.897 2-2V36c0-1.103-.897-2-2-2h-16z"
                                    /><path
                                        fill="#505070"
                                        d="M120 46H96a2 2 0 0 1 0-4h24a2 2 0 0 1 0 4zM108 80c-2.206 0-4-1.794-4-4s1.794-4 4-4 4 1.794 4 4-1.794 4-4 4z"
                                    /></svg
                                >

                                <div>
                                    <h3 class="text-xs font-semibold">
                                        {game.name}
                                    </h3>
                                    <h6 class="text-xs opacity-70">
                                        {game.publisher} - {game.platform}
                                    </h6>
                                </div>
                            </div>
                        </div>
                        <p class="text-xs">
                            {game.pricePool}
                        </p>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</main>
