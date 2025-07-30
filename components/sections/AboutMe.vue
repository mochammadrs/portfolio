<template>
  <section id="about" class="relative min-h-screen flex flex-col justify-start pt-6 md:pt-28">
    <div class="relative container mx-auto px-4 z-10">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
        <img
            src="~/assets/images/bgPoto.svg"
            alt="Foto profil"
            class="absolute top-[-35px] left-[138px] z-[-1] object-cover hidden md:block"
          >
        <div class="w-full max-w-sm mx-auto">
          <img
            src="~/assets/images/profil.jpg"
            alt="Foto profil"
            class="shadow-2xl w-full h-auto object-cover md:[clip-path:polygon(0%_0%,100%_0%,100%_90%,0%_100%)]"
          >
        </div>
        <div>
          <h2 class="text-4xl md:text-5xl font-bold mb-4 text-[#F44336]">About Me</h2>
          <p class="text-lg md:text-2xl text-normal text-[#000C24] leading-relaxed mb-6">
            Saya adalah seorang Junior Frontend Developer dengan passion untuk menciptakan antarmuka web yang bersih, modern, dan intuitif. Saya selalu bersemangat untuk mempelajari teknologi baru dan berkolaborasi dalam tim untuk menghasilkan produk digital yang luar biasa.
          </p>
          <a
            href="https://drive.google.com/file/d/1WBYXpYxFNjIyRhUxxuDv_Z_-s1Gozibm/view?usp=sharing"
            target="_blank"
            class="inline-block bg-[#000C24] hover:bg-[#022D81] text-white font-bold py-3 px-6 rounded-md transition-colors duration-300"
          >
            Download CV
          </a>
        </div>
      </div>
    </div>
    <div class="absolute bottom-[-70px] left-1/2 -translate-x-1/2 md:bottom-10 md:left-12 md:translate-x-3">
        <TheScroll2/>
      </div>
  </section>
</template>