<script>
    import GameLists from "./gameLists.svelte";
</script>

<main class="w-3/4 m-auto">
    <section>
        <!-- normal filters -->
        <h1 class="text-3xl font-medium">
            Top esports games in 2023 by prize money
        </h1>
    </section>

    <div class="flex justify-between items-baseline gap-10">
        <!-- search -->
        <div class="flex-grow">
            <div class="relative">
                <input
                    class="mt-10 w-full rounded-xl bg-gray-900 px-5 py-1 focus:outline-none pl-10 placeholder:text-gray-500"
                    placeholder="Search game by name"
                    type="text"
                />
                <i
                    class="fa-solid fa-magnifying-glass absolute top-12 left-3 text-gray-400"
                />
            </div>
        </div>
        <!-- sort -->
        <div class="flex">
            <div class="flex">
                <div>Period by:</div>
                <div>
                    <select
                        class="w-[100px] bg-gray-900 mx-4 px-2 py-1 bg-opacity-80 rounded"
                        name="year"
                        id="year"
                    >
                        <option value="2021">2023</option>
                        <option value="2022">2022</option>
                    </select>
                </div>
            </div>
            <div class="flex">
                <div>Sort by:</div>
                <div>
                    <select
                        class="w-[100px] bg-gray-900 mx-4 px-2 py-1 bg-opacity-80 rounded"
                        name="sort"
                        id="sort"
                    >
                        <option value="prize">Prize</option>
                        <option value="date">Date</option>
                    </select>
                </div>
            </div>
        </div>
    </div>
    <!-- games list -->
    <GameLists />
</main>

<style>
    main {
        color: white;
    }
</style>
