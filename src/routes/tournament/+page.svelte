<main class="w-3/4 m-auto">
    <section>
        <!-- normal filters -->
        <h1 class="text-3xl font-medium">Esports Events Statistics</h1>
        <div class="flex justify-between items-center">
            <div class="my-5 mr-5">
                <p class="ml-2 mb-1">Game</p>
                <select
                    name="games"
                    id="game"
                    class="w-[300px] rounded-md px-2 py-1 bg-gray-900 opacity-80"
                >
                    <option value="all">All Games</option>
                    <option value="dota2">Valorant</option>
                    <option value="csgo">CS:GO</option>
                    <option value="lol">League of legends</option>
                </select>
            </div>
            <div class="my-5 mr-5">
                <p class="ml-2 mb-1">Game publisher</p>
                <select
                    name="games-publisher"
                    id="game-publisher"
                    class="w-[300px] rounded-md px-2 py-1 bg-gray-900 opacity-80"
                >
                    <option value="all">All publisher</option>
                    <option value="riot">Riot Games</option>
                    <option value="blizzard">Blizzard Entertainment</option>
                    <option value="epic">Epic Games</option>
                    <option value="ea">Electronic Arts</option>
                </select>
            </div>
            <div class="my-5 mr-5">
                <p class="ml-2 mb-1">Year</p>
                <select
                    name="year"
                    id="year"
                    class="w-[300px] rounded-md px-2 py-1 bg-gray-900 opacity-80"
                >
                    <option value="all">All time period</option>
                    <option value="2021">2021</option>
                    <option value="2020">2020</option>
                </select>
            </div>
            <div class="my-5 mr-5">
                <p class="ml-2 mb-1">Teams</p>
                <select
                    name="teams"
                    id="teams"
                    class="w-[300px] rounded-md px-2 py-1 bg-gray-900 opacity-80"
                >
                    <option value="all">All teams</option>
                    <option value="team1">Team 1</option>
                    <option value="team2">Team 2</option>
                    <option value="team3">Team 3</option>
                </select>
            </div>
        </div>
    </section>

    <section class="flex gap-3">
        <!-- addition filters -->
        <div class="flex items-center gap-2 text-gray-400">
            <i class="fa-solid fa-filter" />
            <h1>Additional filters:</h1>
        </div>
        <div class="flex justify-between items-center gap-5">
            <div>
                <div
                    class=" border text-blue-500 border-blue-500 inline-block px-5 py-1 rounded-full font-bold"
                >
                    <i class="fa-solid fa-arrow-trend-up mr-2" />
                    Upcommming
                </div>
            </div>
            <div>
                <div
                    class=" border text-blue-500 border-blue-500 inline-block px-5 py-1 rounded-full font-bold opacity-70"
                >
                    <i class="fa-solid fa-clock-rotate-left" />
                    Recent
                </div>
            </div>
            <div>
                <div
                    class=" border text-blue-500 border-blue-500 inline-block px-5 py-1 rounded-full font-bold opacity-70"
                >
                    <i class="fa-solid fa-dollar-sign" />
                    Price Pool
                </div>
            </div>
        </div>
    </section>

    <!-- search -->

    <div class="relative">
        <input
            class="mt-10 w-full rounded-xl bg-gray-900 px-5 py-1 focus:outline-none pl-10 placeholder:text-gray-500"
            placeholder="Search tournament by name"
            type="text"
        />
        <i
            class="fa-solid fa-magnifying-glass absolute top-12 left-3 text-gray-400"
        />
    </div>
</main>

<style>
    main {
        color: white;
    }
</style>
