<script>
    import "../app.css";
</script>

<body class="flex flex-col min-h-screen">
    <header class="bg-gray-900 text-white py-4">
        <!-- Navigation Bar -->
        <nav class="container mx-auto flex justify-between items-center px-4">
            <div class="flex items-center">
                <!-- Logo -->
                <img
                    src="https://escharts.com/img/logos/esc-logo-white.svg"
                    alt="Logo"
                />
            </div>
            <div class="flex items-center">
                <!-- Navigation Links -->
                <a href="/" class="text-gray-300 hover:text-white px-3">Home</a>
                <a href="/about" class="text-gray-300 hover:text-white px-3"
                    >About</a
                >
                <a href="_" class="text-gray-300 hover:text-white px-3"
                    >Services</a
                >
                <a href="/Contact" class="text-gray-300 hover:text-white px-3"
                    >contact</a
                >
            </div>
        </nav>
    </header>

    <main class="flex-grow bg-gray-100 py-8">
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
