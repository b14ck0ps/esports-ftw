// BEGIN: ed8c6549bwf9
<script>
    let r_tournaments = [
        {
            name: "Valorant Chapion League 2034",
            game: "Valorant",
            platform: "PC",
            date: new Date().toLocaleDateString().replace(/\//g, "."),
        },
        {
            name: "Overwatch World Cup 2022",
            game: "Overwatch",
            platform: "PC",
            date: new Date().toLocaleDateString().replace(/\//g, "."),
        },
        {
            name: "FIFA World Cup 2022",
            game: "FIFA 22",
            platform: "PlayStation 5",
            date: new Date().toLocaleDateString().replace(/\//g, "."),
        },
        {
            name: "League of Legends World Championship 2022",
            game: "League of Legends",
            platform: "PC",
            date: new Date().toLocaleDateString().replace(/\//g, "."),
        },
        {
            name: "Call of Duty World League 2022",
            game: "Call of Duty",
            platform: "Xbox Series X",
            date: new Date().toLocaleDateString().replace(/\//g, "."),
        }
    ];
</script>

<main>
    <div class="flex justify-between items-center">
        <div>
            <!--Header-->
            <div class="flex gap-20 items-center">
                <div class="flex items-center gap-3">
                    <i
                        class="fa-solid fa-clock-rotate-left bg-gray-900 p-2 rounded-lg"
                    />
                    <p class="font-bold">Recent Tournaments</p>
                </div>
                <div
                    class="flex text-sm items-center gap-4 bg-gray-900 rounded-lg px-4 py-2 cursor-pointer hover:bg-gray-700 transition-all"
                >
                    <p>More</p>
                    <i class="fa-solid fa-arrow-right" />
                </div>
            </div>
            <div>
                <!--Table-->
                {#each r_tournaments as tournament}
                <div
                    class="flex justify-between my-6 bg-gray-900 p-3 rounded-xl cursor-pointer hover:scale-x-105 transition-all"
                >
                    <div>
                        <div class="flex items-center gap-3">
                            <svg
                                class="w-10 fill-current text-red-600"
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 32 32"
                                id="valorant"
                                ><path
                                    d="M4.772 7.364A1 1 0 0 0 3 8v8c0 .245.09.481.252.665l8 9c.19.213.462.335.748.335h6a.999.999 0 0 0 .772-1.636l-14-17zM12.449 24 5 15.62v-4.833L15.881 24h-3.432zM28.336 7.058a.998.998 0 0 0-1.11.309l-9 11A1.001 1.001 0 0 0 19 20h6c.265 0 .52-.105.707-.293l3-3A.997.997 0 0 0 29 16V8a1 1 0 0 0-.664-.942zM27 15.586 24.586 18H21.11L27 10.801v4.785z"
                                /></svg
                            >
                            <div>
                                <h3 class="text-xs font-semibold">{tournament.name}</h3>
                                <h6 class="text-xs opacity-70">{tournament.game} : {tournament.platform}</h6>
                            </div>
                        </div>
                    </div>
                    <p class="text-xs">{tournament.date}</p>
                </div>
                {/each}
            </div>
        </div>
    </div>
</main>
// END: ed8c6549bwf9