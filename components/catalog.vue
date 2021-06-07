<template>
  <div id="products" class="w-full bg-light py-20">
    <div class="container mx-auto px-4">
      <h4 class="text-h5 font-bold mb-8 text-gray">Каталог</h4>
      <div
        data-aos="fade-down"
        data-aos-duration="2000"
        class="flex flex-wrap -mx-4 overflow-hidden"
      >
        <div
          v-for="product in products"
          :key="product.id"
          class="my-4 px-4 w-full md:w-1/2 lg:w-1/3 relative"
        >
          <div class="product w-full overflow-hidden">
            <img class="w-full" :src="product.img" />
            <div
              class="block w-full h-full absolute bg-clip-content bg-orange-800 px-4 inset-0 hidden product-hover"
            >
              <nuxt-link
                :to="product.link"
                class="w-full h-full flex justify-center items-center"
              >
                <div
                  class="px-4 py-3 border-2 border-white text-white text-body font-semibold font-sans"
                >
                  {{ product.title }}
                </div>
              </nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          img: "http://epika.com.tr//resim/upload/7128a.jpg",
          title: "Диванные комплекты",
          link: "/products/sofa-sets",
        },
        {
          img: "http://epika.com.tr/resim/upload/7164a.jpg",
          title: "Угловые комплекты",
          link: "/products/corner-sets",
        },
        {
          img: "http://epika.com.tr/resim/upload/7179a.jpg",
          title: "Диваны",
          link: "/products/sofas",
        },
        {
          img: "http://epika.com.tr/images/intearch/services/services4.jpg",
          title: "Кресла",
          link: "/products/bergers",
        },
        {
          img: "http://epika.com.tr/images/intearch/services/services5.jpg",
          title: "Кровати",
          link: "/products/beds",
        },
        {
          img: "http://epika.com.tr/images/intearch/services/services6.jpg",
          title: "Журнальные столики",
          link: "/products/coffee-tables",
        },
      ],
    };
  },
};
</script>

<style scoped>
.product:hover .product-hover {
  display: block;
}
</style>