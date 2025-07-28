<template>
  <section id="about" class="relative min-h-screen flex flex-col justify-start pt-24">
    <div class="relative container mx-auto px-4 z-10">
      <div class="grid grid-cols-1 md:grid-cols-2 items-center">
        <img
            src="~/assets/images/bgPoto.svg"
            alt="Foto profil"
            class="absolute top-[-100px] left-[104px] z-[-1] object-cover"
          >
        <div class="w-full max-w-sm mx-auto">
          <img
            src="~/assets/images/profil.jpg"
            alt="Foto profil"
            class="rounded-lg shadow-2xl w-full h-auto object-cover"
          >
        </div>
        <div>
          <h2 class="text-5xl font-bold mb-4 text-[#F44336]">About Me</h2>
          <p class="text-2xl text-normal text-[#000C24] leading-relaxed mb-6">
            Saya adalah seorang Junior Frontend Developer dengan passion untuk menciptakan antarmuka web yang bersih, modern, dan intuitif. Saya selalu bersemangat untuk mempelajari teknologi baru dan berkolaborasi dalam tim untuk menghasilkan produk digital yang luar biasa.
          </p>
          <a
            href="/cv-anda.pdf"
            target="_blank"
            class="inline-block bg-[#000C24] hover:bg-[#022D81] text-white font-bold py-3 px-6 rounded-md transition-colors duration-300"
          >
            Download CV
          </a>
        </div>
      </div>
    </div>
    <div class="absolute px-12 left-3 bottom-[60px]">
        <TheScroll2/>
      </div>
  </section>
</template>