<main>
    <div class=" w-[500px] m-auto mt-[15vh]">
        <form
            action="/"
            method="GET"
            class="shadow-md rounded px-8 pt-6 pb-8 mb-4 bg-gray-900"
        >
            <div class="mb-4">
                <label class="block text-gray-700 font-bold mb-2" for="email">
                    Email
                </label>
                <input
                    class="shadow appearance-none border rounded w-full py-2 px-3 text-white leading-tight focus:outline-none focus:shadow-outline bg-gray-700 border-none"
                    id="email"
                    type="email"
                    placeholder="yourname@email.com"
                />
            </div>
            <div class="mb-6">
                <label
                    class="block text-gray-700 font-bold mb-2"
                    for="password"
                >
                    Password
                </label>
                <input
                    class="shadow appearance-none border rounded w-full py-2 px-3 text-white leading-tight focus:outline-none focus:shadow-outline bg-gray-700 border-none"
                    id="password"
                    type="password"
                    placeholder="********"
                />
            </div>
            <div class="flex items-center justify-between">
                <button
                    class="border border-green-ftw hover:text-green-ftw text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
                    type="submit"
                >
                    Sign In
                </button>
                <a
                    class="inline-block align-baseline font-bold text-sm text-white hover:text-green-ftw"
                    href="/"
                >
                    Forgot Password?
                </a>
            </div>
        </form>
    </div>
</main>
