<script lang="ts" setup>

</script>

<template>
    <div class="bg-white text-white min-h-screen">
        <header class="p-8 md:px-12 sticky top-0 w-full z-30 bg-[#000C24]/80 border-gray-500/50 h-[75px] flex items-center backdrop-blur-lg">
        <img 
        src="~/assets/images/splatterNav.svg" 
        alt="Efek kuas cat navbar"
        class="absolute animate-pulse left-[18px] top-[-2px] object-cover w-[120px]">
            <nav class="relative z-10 container mx-auto flex justify-between items-center">
                <ul class="flex items-center gap-12">
                    <li><a href="#home" class="text-lg hover:font-bold text-gray-400 hover:text-[#F44336]">Home</a></li>
                    <li><a href="#about" class="mx-1 text-lg hover:font-bold text-gray-400 hover:text-[#F44336]">About</a></li>
                    <li><a href="#skills" class="mx-1 text-lg hover:font-bold text-gray-400 hover:text-[#F44336]">Skills</a></li>
                    <li><a href="#works" class="mx-1 text-lg hover:font-bold text-gray-400 hover:text-[#F44336]">Works</a></li>
                    <li><a href="#contact" class="mx-1 text-lg hover:font-bold text-gray-400 hover:text-[#F44336]">Contact</a></li>
                </ul>
            </nav>
        </header>
        <main>
            <slot />
        </main>
        <footer>
            <div class="relative w-full h-[215px] mx-auto flex flex-col justify-center text-center text-gray-400 bg-[#000C24]">
                <img
                src="~/assets/images/splatterBgFoo.svg"
                alt="splatter bg skills"
                class="absolute w-[313px] right-[50px] object-cover"
                >
                <p class="font-semibold text-[#FFFFFF]">mochammadrs_</p>
                <div class="flex justify-center gap-4 m-3">
                <a 
                href="https://github.com/mochammadrs" 
                target="_blank" 
                rel="noopener noreferrer"
                class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                aria-label="GitHub">
                <Icon name="mdi:github" class="text-3xl" />
                </a>
                <a 
                href="https://linkedin.com/in/mochammadrs" 
                target="_blank" 
                rel="noopener noreferrer"
                class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                aria-label="LinkedIn">
                <Icon name="mdi:linkedin" class="text-3xl" />
                </a>
                <a 
                href="https://instagram.com/mochammadrs_" 
                target="_blank" rel="noopener noreferrer"
                class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                aria-label="Instagram">
                <Icon name="mdi:instagram" class="text-3xl" />
                </a>
                <a 
                href="https://facebook.com/rebellious0209" 
                target="_blank" 
                rel="noopener noreferrer"
                class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                aria-label="Facebook">
                <Icon name="mdi:facebook" class="text-3xl" />
                </a>
                <a 
                href="https://x.com/mochammadrs_" 
                target="_blank" 
                rel="noopener noreferrer"
                class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                aria-label="Twitter">
                <Icon name="fa6-brands:x-twitter" class="text-3xl" />
                </a>
            </div>
                <p>All Right Reserved &copy; 2025. Dibuat dengan ❤️ oleh RS</p>
            </div>
        </footer>
    </div>
</template>