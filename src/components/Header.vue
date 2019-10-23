<template>
  <div class="font-sans antialiased" id="app">
    <nav class="flex items-center fixed w-full justify-between flex-wrap bg-gray-900 z-10 p-6">
      <div class="flex items-center flex-no-shrink text-3xl text-white mr-6">
        <router-link to="/">
        Eazy HealthCare
        </router-link>
      </div>
      <div class="block sm:hidden">
        <button
          @click="toggle"
          class="flex items-center px-3 py-2 border rounded text-teal-lighter border-teal-light hover:text-white hover:border-white"
        >
          <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <title>Menu</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </button>
      </div>
      <div
        :class="open ? 'block': 'hidden'"
        class="w-full flex-grow sm:flex sm:items-center sm:w-auto"
      >
        <div class="text-sm sm:flex-grow"></div>
        <div>
          <router-link
            to="drugs"
            class="block mt-4 lg:inline-block uppercase text-white font-semibold text-lg md:px-4 md:py-2 lg:mt-0 mr-4"
          >Drugs</router-link>
                    <router-link
            to="addDrug"
            class="block mt-4 lg:inline-block uppercase text-white font-semibold text-lg md:px-4 md:py-2 lg:mt-0 mr-4"
          >Add Drug</router-link>
          <router-link
            to="pricing"
            class="block mt-4 lg:inline-block uppercase text-white font-semibold text-lg md:px-4 md:py-2 lg:mt-0 mr-4"
          >FAQS</router-link>
          <router-link
            to="faq"
            class="block mt-4 lg:inline-block font-semibold text-white text-lg uppercase md:px-4 md:py-2 lg:mt-0 mr-4"
          >Sign In</router-link>
          <button
            class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
          >Get Started</button>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
import { SweetModal, SweetModalTab } from "sweet-modal-vue";
export default {
  components: {
    SweetModal,
    SweetModalTab
  },
  data() {
    return {
      open: false
    };
  },
  methods: {
    toggle() {
      console.log(this.open);
      this.open = !this.open;
      console.log(this.open);
    }
  }
};
</script>

<style scoped>
.my-header {
  color: black;
  z-index: 100;
}

.order-btn {
  background-color: #ffb601;
  color: #fff;
  text-transform: uppercase;
}

.order-btn2 {
  background-color: #efa706;
  color: #fff;
  text-transform: uppercase;
}

button:focus {
  outline: none;
}
</style>