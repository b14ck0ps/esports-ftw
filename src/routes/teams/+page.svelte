<script>
    import Teams from "./teamsLists.svelte";
</script>

<main class="w-3/4 m-auto">
    <section>
        <!-- normal filters -->
        <h1 class="text-3xl font-medium">Esports Events Statistics</h1>
        <div class="flex justify-between items-center">
            <div class="mt-3 mr-5">
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
    <!-- teams list -->
    <Teams />
</main>

<style>
    main {
        color: white;
    }
</style>
