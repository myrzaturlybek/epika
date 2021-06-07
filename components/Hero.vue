<template>
  <div class="hero relative w-full bg-light mt-20">
    <div class="container mx-auto px-4 z-10">
      <div class="flex flex-wrap overflow-hidden">
        <div
          data-aos="zoom-in"
          data-aos-duration="3000"
          class="w-full flex flex-col items-center overflow-hidden lg:w-1/2 py-48 px-8"
        >
          <h1 class="text-gray font-bold text-h2 md:text-h1 text-center mb-6">
            Отражайте Свою Душу И Стиль
          </h1>
          <p class="text-lead1 text-center text-gray mb-10">
            Бренд, в котором сталь и эстетика встречаются
          </p>
          <div>
            <a
              href="#products"
              class="block px-8 py-4 text-white text-lead2 font-semibold font-sans bg-orange hover:bg-orange-800"
              >Каталог</a
            >
          </div>
        </div>

        <div class="w-full overflow-hidden lg:w-1/2">
          <!-- Column Content -->
        </div>
      </div>
    </div>
    <div
      class="absolute hidden lg:block top-0 right-0 w-1/2 z-0 h-full overflow-hidden"
    >
      <div class="flex flex-wrap justify-end w-full h-full overflow-hidden">
        <div
          data-aos="fade-left"
          data-aos-duration="2000"
          class="hero-img w-full h-full overflow-hidden"
        >
          <!-- Column Content -->
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-img {
  background: url("../static/Hero.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
/* @media (max-width: 1023px) {
  .hero {
    background-size: cover;
  }
} */
</style>