<template>
    <section id="home" class="bg-[#000C24] lg:bg-transparent relative min-h-screen flex items-center p-4 md:p-8">
        <div class="relative z-10 w-full text-center md:text-left md:px-8">
            <h1 class="text-4xl md:text-6xl stroke-text-light text-transparent font-extrabold">
                Mochammad RS
            </h1>
            <p class="text-lg md:text-2xl text-[#ffffff] mt-2 font-semibold">
                Engineer + Junior Front-end Developer
            </p>
            <div class="flex gap-4 mt-6 justify-center md:justify-start">
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
            <div class="absolute left-1/2 -translate-x-1/2 bottom-[-230px] md:translate-x-0 md:left-auto md:bottom-[-260px]">
                <TheScroll />
            </div>
        </div>
    </section>
</template>
