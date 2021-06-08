<template>
  <header class="w-full h-20 flex items-center bg-gray flex fixed top-0 z-20">
    <div class="container mx-auto px-4 overflow-hidden">
      <div class="flex flex-wrap items-center overflow-hidden lg:-mx-3">
        <div
          class="
            w-full
            overflow-hidden
            flex
            justify-between
            items-center
            lg:my-3
            lg:px-3
            lg:w-1/5
          "
        >
          <nuxt-link to="/"
            ><img src="../static/logo.png" alt="logo"
          /></nuxt-link>
          <svg
            @click="mobileMenuOpened = true"
            class="lg:hidden cursor-pointer"
            width="32"
            height="21"
            viewBox="0 0 32 21"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M0 21H32V17.5H0V21ZM0 12.25H32V8.75H0V12.25ZM0 0V3.5H32V0H0Z"
              fill="#FDFDFD"
            />
          </svg>
        </div>

        <div
          v-show="mobileMenuOpened"
          class="mobile-menu absolute top-0 bg-gray inset-x-0 lg:hidden"
        >
          <div
            @click="mobileMenuOpened = false"
            class="
              flex
              h-20
              items-center
              container
              mx-auto
              px-2
              justify-end
              cursor-pointer
            "
          >
            <svg
              class="h-10 w-10 text-white"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </div>
          <div class="container px-2 mx-auto pt-3 pb-6">
            <nav>
              <div
                class="
                  text-white text-3xl
                  font-semibold font-sans
                  text-gray-800
                "
              >
                <div class="hover:text-white py-6">
                  <a href="/#about">О нас</a>
                </div>
                <div
                  class="dropdown flex cursor-pointer py-6"
                  aria-expanded="false"
                >
                  <span>Каталог</span>
                  <svg
                    class="text-gray-800 ml-1 h-5 w-5"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                      clip-rule="evenodd"
                    />
                  </svg>
                  <div
                    class="
                      dropdown-menu
                      absolute
                      hidden
                      z-10
                      pt-4
                      -ml-3
                      mt-10
                      bg-gray
                    "
                  >
                    <ol>
                      <li
                        v-for="product in products"
                        :key="product.id"
                        class="px-8 py-3 hover:text-white"
                      >
                        <nuxt-link :to="product.link">{{
                          product.title
                        }}</nuxt-link>
                      </li>
                    </ol>
                  </div>
                </div>

                <div class="hover:text-white py-6">
                  <a href="/#contact">Контакты</a>
                </div>
              </div>
            </nav>
          </div>
          <div class="pb-4 flex justify-center">
            <a
              href="/#contact"
              class="
                px-4
                py-3
                border-2 border-orange
                text-orange text-body
                font-semibold font-sans
                hover:text-orange-800
                hover:border-orange-800
              "
              >Связаться</a
            >
          </div>
        </div>

        <div class="hidden lg:block overflow-hidden lg:my-3 lg:px-3 lg:w-2/5">
          <nav>
            <div
              class="
                text-white text-lead2
                font-semibold font-sans
                text-gray-800
              "
            >
              <div class="inline hover:text-white">
                <a href="/#about">О нас</a>
              </div>
              <div
                class="dropdown inline-flex mx-8 cursor-pointer"
                aria-expanded="false"
              >
                <span>Каталог</span>
                <svg
                  class="text-gray-800 ml-1 h-5 w-5"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                  aria-hidden="true"
                >
                  <path
                    fill-rule="evenodd"
                    d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                    clip-rule="evenodd"
                  />
                </svg>
                <div
                  class="
                    dropdown-menu
                    absolute
                    hidden
                    z-10
                    pt-4
                    -ml-3
                    mt-5
                    bg-gray
                  "
                >
                  <ol>
                    <li
                      v-for="product in products"
                      :key="product.id"
                      class="px-8 py-3 hover:text-white"
                    >
                      <nuxt-link :to="product.link">{{
                        product.title
                      }}</nuxt-link>
                    </li>
                  </ol>
                </div>
              </div>

              <div class="inline hover:text-white">
                <a href="/#contact">Контакты</a>
              </div>
            </div>
          </nav>
        </div>

        <div
          class="
            hidden
            lg:flex
            lg:justify-end
            overflow-hidden
            lg:my-3
            lg:px-3
            lg:w-2/5
          "
        >
          <a
            href="/#contact"
            class="
              px-4
              py-3
              border-2 border-orange
              text-orange text-body
              font-semibold font-sans
              hover:text-orange-800
              hover:border-orange-800
            "
            >Связаться</a
          >
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      mobileMenuOpened: false,
      products: [
        {
          img: "7128a.jpg",
          title: "Диванные комплекты",
          link: "/products/sofa-sets",
        },
        {
          img: "7164a.jpg",
          title: "Угловые комплекты",
          link: "/products/corner-sets",
        },
        {
          img: "7179a.jpg",
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
.dropdown:hover .dropdown-menu {
  display: block;
}
.dropdown:hover svg {
  color: white;
}
.dropdown:hover span {
  color: white;
}
</style>