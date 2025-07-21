<template>
    <div class="bg-white text-white min-h-screen">
        <header class="relative p-8 md:px-12">
            <img 
            src="~/assets/images/splatter.svg" 
            alt="Efek kuas cat"
            class="absolute top-0 left-0 w-full h-full object-cover z-0">
            <nav class="relative z-10 container mx-auto flex justify-between items-center">
                <ul class="flex items-center gap-6">
                    <li><a href="#home" class="text-white font-bold hover:text-gray-300">Home</a></li>
                    <li><a href="#about" class="text-gray-400 hover:text-white">About</a></li>
                    <li><a href="#skills" class="text-gray-400 hover:text-white">Skills</a></li>
                    <li><a href="#works" class="text-gray-400 hover:text-white">Works</a></li>
                    <li><a href="#contact" class="text-gray-400 hover:text-white">Contact</a></li>
                </ul>
            </nav>
        </header>
        <main>
            <slot />
        </main>
        <footer class="p-4 mt-12">
            <div class="container mx-auto text-center text-gray-400">
                <p>&copy; 2025. Dibuat dengan ❤️ oleh RS</p>
            </div>
        </footer>
    </div>
</template>