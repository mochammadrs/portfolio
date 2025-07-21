<template>
    <section class="relative min-h-screen flex items-center overflow-hidden p-8">
        <img 
        src="~/assets/images/splatter.svg" 
        alt="Efek kuas cat"
        class="absolute top-0 left-0 w-full h-full object-cover">
        <div class="relative z-10 px-4">
            <h1 class="text-6xl stroke-text-light text-transparent">
                Mochammad RS
            </h1>
            <p class="text-lg md:text-xl text-[#ffffff] mt-2">
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
            <div class="">
                <TheScroll />
            </div>
        </div>
    </section>
</template>
