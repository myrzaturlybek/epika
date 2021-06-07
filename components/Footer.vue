<template>
  <footer class="w-full bg-gray pt-20 font-serif text-light">
    <div class="container mx-auto px-4">
      <div class="flex flex-wrap -mx-4 overflow-hidden">
        <div class="my-2 px-4 w-full overflow-hidden md:w-1/2 lg:w-1/4">
          <img src="../static/logo.png" class="mb-8" />
          <p class="text-lead2">
            Компания известна своими запатентованными полностью стальными
            каркасами, впервые изготовленными в Турции и на Земле. Наша
            компания, которая продолжает свою деятельность с 2000 года по
            сегодняшний день с брендом EPIKA, экспортирует значительную часть
            продукции за пределы Турций.
          </p>
        </div>

        <div class="my-2 px-4 w-full overflow-hidden md:w-1/2 lg:w-1/4">
          <h6 class="text-h6 text-gray-800 mb-8">Ссылки</h6>
          <ul>
            <li class="mb-4"><a href="/#about">О нас</a></li>
            <li class="mb-4"><a href="/#contact">Контакты</a></li>
          </ul>
        </div>

        <div class="my-2 px-4 w-full overflow-hidden md:w-1/2 lg:w-1/4">
          <h6 class="text-h6 text-gray-800 mb-8">Каталог</h6>
          <ul>
            <li v-for="product in products" :key="product.id" class="mb-4">
              <nuxt-link :to="product.link">{{ product.title }}</nuxt-link>
            </li>
          </ul>
        </div>

        <div class="my-2 px-4 w-full overflow-hidden md:w-1/2 lg:w-1/4">
          <h6 class="text-h6 text-gray-800 mb-8">Свяжитесь с нами</h6>
          <ul>
            <li class="mb-4 flex items-center">
              <svg
                width="20"
                height="16"
                viewBox="0 0 20 16"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M18 0H2C0.9 0 0.00999999 0.9 0.00999999 2L0 14C0 15.1 0.9 16 2 16H18C19.1 16 20 15.1 20 14V2C20 0.9 19.1 0 18 0ZM18 4L10 9L2 4V2L10 7L18 2V4Z"
                  fill="#FE9A22"
                />
              </svg>
              <p class="ml-2">info@epika.com.kz</p>
            </li>
            <li class="mb-4 flex items-center">
              <svg
                width="20"
                height="22"
                viewBox="0 0 13 22"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M10.5 0H2.5C1.12 0 0 1.12 0 2.5V19.5C0 20.88 1.12 22 2.5 22H10.5C11.88 22 13 20.88 13 19.5V2.5C13 1.12 11.88 0 10.5 0ZM6.5 21C5.67 21 5 20.33 5 19.5C5 18.67 5.67 18 6.5 18C7.33 18 8 18.67 8 19.5C8 20.33 7.33 21 6.5 21ZM11 17H2V3H11V17Z"
                  fill="#FE9A22"
                />
              </svg>
              <p class="ml-2">+7 771 157 55 11</p>
            </li>
            <li class="mb-4 flex items-center">
              <svg
                width="20"
                height="20"
                viewBox="0 0 14 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7 0C3.13 0 0 3.13 0 7C0 12.25 7 20 7 20C7 20 14 12.25 14 7C14 3.13 10.87 0 7 0ZM7 9.5C5.62 9.5 4.5 8.38 4.5 7C4.5 5.62 5.62 4.5 7 4.5C8.38 4.5 9.5 5.62 9.5 7C9.5 8.38 8.38 9.5 7 9.5Z"
                  fill="#FE9A22"
                />
              </svg>
              <p class="ml-2">проспект Аль-Фараби, 17/1 к5Б</p>
            </li>
          </ul>
        </div>
      </div>
      <div class="w-full flex justify-center mt-20 pb-4">
        <span>© 2021 epika</span>
      </div>
    </div>
  </footer>
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