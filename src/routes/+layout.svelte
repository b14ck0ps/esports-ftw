<script>
    import "../app.css";
</script>

<body class="flex flex-col min-h-screen">
    <header class="bg-gray-900 text-white py-4">
        <!-- Navigation Bar -->
        <nav class="container mx-auto flex justify-normal items-center px-4 gap-4">
            <div class="flex items-center">
                <!-- Logo -->
                <img
                    src="https://escharts.com/img/logos/esc-logo-white.svg"
                    alt="Logo"
                />
            </div>
            <div class="flex items-center gap-10 ml-5 font-semibold">
                <!-- Navigation Links -->
                <a href="/tournament" class="text-gray-300 hover:text-[#48f955]">Tournament</a>
                <a href="/games" class="text-gray-300 hover:text-[#48f955]">Games</a>
                <a href="/teams" class="text-gray-300 hover:text-[#48f955]">Teams</a>
                
            </div>
        </nav>
    </header>

    <main class="flex-grow bg-gray-800 py-8">
        <!-- Main Content -->
        <slot />
    </main>

    <footer class="bg-gray-900 text-white py-4">
        <!-- Footer -->
        <div class="container mx-auto px-4">
            <p class="text-center">
                &copy; 2023 Your Company. All rights reserved.
            </p>
        </div>
    </footer>
</body>
