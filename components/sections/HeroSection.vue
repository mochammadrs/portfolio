<template>
    <section id="home" class="relative min-h-screen flex items-center overflow-hidden p-8">
        <div class="relative z-10 px-8 bottom-[80px]">
            <h1 class="text-6xl stroke-text-light text-transparent font-extrabold">
                Mochammad RS
            </h1>
            <p class="text-2xl text-[#ffffff] mt-2 font-semibold">
                Engineer + Junior Front-end Developer
            </p>
            <div class="flex gap-4 mt-6">
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
            <div class="absolute bottom-[-260px]">
                <TheScroll />
            </div>
        </div>
    </section>
</template>
