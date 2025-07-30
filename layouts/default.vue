<script lang="ts" setup>
import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

const activeLinkIndex = ref(0)

const homeEl = ref<HTMLLIElement | null>(null)
const aboutEl = ref<HTMLLIElement | null>(null)
const skillsEl = ref<HTMLLIElement | null>(null)
const worksEl = ref<HTMLLIElement | null>(null)
const contactEl = ref<HTMLLIElement | null>(null)

const linkElements = [homeEl, aboutEl, skillsEl, worksEl, contactEl]

const splatterStyle = computed(() => {
    const activeElement = linkElements[activeLinkIndex.value]?.value

    if (activeElement) {
        const offsetLeft = activeElement.offsetLeft
        return {
            left: `${offsetLeft + 19}px`,
            opacity: 1,
        };
    }
    return { opacity: 0 }
});

function setActiveLink(index: number) {
    activeLinkIndex.value = index
    if (observer) {
        observer.disconnect();
    }

    if (scrollTimeout) clearTimeout(scrollTimeout);
    scrollTimeout = setTimeout(() => {
        sectionsToObserve.forEach(section => observer?.observe(section))
    }, 1000)
}

const navLinks = [
    { id: 'home' },
    { id: 'about' },
    { id: 'skills' },
    { id: 'works' },
    { id: 'contact' }
]

let scrollTimeout: NodeJS.Timeout | null = null

let observer: IntersectionObserver | null = null
const sectionsToObserve: Element[] = [];

onMounted(() => {
    const observerOptions = {
        root: null,
        rootMargin: '0px',
        threshold: 0.8
    }

    observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
            if (entry.isIntersecting) {
                const id = entry.target.id;
                const newIndex = navLinks.findIndex(link => link.id === id)
                if (newIndex !== -1) {
                    activeLinkIndex.value = newIndex
                }
            }
        });
    }, observerOptions);

    const sections = document.querySelectorAll('section[id]');
    sections.forEach(section => {
        sectionsToObserve.push(section);
        observer?.observe(section)
    });
});

onBeforeUnmount(() => {
    if (observer) observer.disconnect();
    if (scrollTimeout) clearTimeout(scrollTimeout);
});
</script>

<template>
    <div class="bg-white text-white min-h-screen">
        <header
            class="p-4 md:p-8 md:px-12 sticky top-0 w-full z-30 bg-[#000C24]/80 border-gray-500/50 h-[75px] flex items-center backdrop-blur-lg hidden md:flex">
            <img 
            src="~/assets/images/splatterNav.svg" alt="Efek kuas cat navbar"
                class="absolute animate-pulse left-[10px] w-[100px] md:left-[18px] top-[-2px] object-cover md:w-[120px] transition-all duration-300 ease-in-out hidden md:block"
                :style="splatterStyle">
            <nav class="relative z-10 container mx-auto flex justify-between items-center w-full">
                <ul class="flex items-center justify-between md:justify-start w-full gap-4 md:gap-12 hidden md:flex">
                    <li ref="homeEl">
                        <a 
                        href="#home" :class="activeLinkIndex === 0 ? 'font-bold text-[#F44336]' : 'text-gray-400'"
                            class="text-lg hover:font-bold hover:text-[#F44336]" @click="setActiveLink(0)">Home
                        </a>
                    </li>
                    <li ref="aboutEl">
                        <a 
                        href="#about" :class="activeLinkIndex === 1 ? 'font-bold text-[#F44336]' : 'text-gray-400'"
                            class="mx-1 text-lg hover:font-bold hover:text-[#F44336]" @click="setActiveLink(1)">About
                        </a>
                    </li>
                    <li ref="skillsEl">
                        <a 
                        href="#skills" :class="activeLinkIndex === 2 ? 'font-bold text-[#F44336]' : 'text-gray-400'"
                            class="mx-1 text-lg hover:font-bold hover:text-[#F44336]" @click="setActiveLink(2)">Skills
                        </a>
                    </li>
                    <li ref="worksEl">
                        <a 
                        href="#works" :class="activeLinkIndex === 3 ? 'font-bold text-[#F44336]' : 'text-gray-400'"
                            class="mx-1 text-lg hover:font-bold hover:text-[#F44336]" @click="setActiveLink(3)">Works
                        </a>
                    </li>
                    <li ref="contactEl">
                        <a 
                        href="#contact" :class="activeLinkIndex === 4 ? 'font-bold text-[#F44336]' : 'text-gray-400'"
                            class="mx-1 text-lg hover:font-bold hover:text-[#F44336]" @click="setActiveLink(4)">Contact
                        </a>
                    </li>
                </ul>
            </nav>
        </header>
        <main>
            <slot />
        </main>
        <footer>
            <div
                class="relative w-full h-[215px] mx-auto flex flex-col justify-center text-center text-gray-400 bg-[#000C24]">
                <img 
                src="~/assets/images/splatterBgFoo.svg" alt="splatter bg foo"
                    class="absolute w-[313px] right-[50px] object-cover hidden md:block">
                <p class="font-semibold text-[#FFFFFF]">mochammadrs_</p>
                <div class="flex justify-center gap-4 m-3">
                    <a 
                    href="https://github.com/mochammadrs" target="_blank" rel="noopener noreferrer"
                        class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                        aria-label="GitHub">
                        <Icon name="mdi:github" class="text-3xl" />
                    </a>
                    <a 
                    href="https://linkedin.com/in/mochammadrs" target="_blank" rel="noopener noreferrer"
                        class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                        aria-label="LinkedIn">
                        <Icon name="mdi:linkedin" class="text-3xl" />
                    </a>
                    <a 
                    href="https://instagram.com/mochammadrs_" target="_blank" rel="noopener noreferrer"
                        class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                        aria-label="Instagram">
                        <Icon name="mdi:instagram" class="text-3xl" />
                    </a>
                    <a 
                    href="https://facebook.com/rebellious0209" target="_blank" rel="noopener noreferrer"
                        class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                        aria-label="Facebook">
                        <Icon name="mdi:facebook" class="text-3xl" />
                    </a>
                    <a 
                    href="https://x.com/mochammadrs_" target="_blank" rel="noopener noreferrer"
                        class="text-gray-400 hover:text-white transition-transform duration-300 hover:scale-125"
                        aria-label="Twitter">
                        <Icon name="fa6-brands:x-twitter" class="text-3xl" />
                    </a>
                </div>
                <p class="text-xs md:text-base">All Right Reserved &copy; 2025. Dibuat dengan ❤️ oleh RS</p>
            </div>
        </footer>
    </div>
</template>