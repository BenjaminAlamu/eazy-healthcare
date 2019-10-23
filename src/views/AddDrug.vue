<template>
  <div class="pt-32">
    <p class="text-center title-text m-2">Add New Drug</p>
    <form class="w-full mt-8 max-w-lg mx-auto">
      <div class="flex flex-wrap -mx-3 mb-6">
        <div class="w-full px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >Drug Name</label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
        </div>
        <div class="w-full px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >Drug Price</label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="number"
            placeholder="Doe"
          />
        </div>
        <div class="w-full px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >Drug Image</label>
          <input
            class="appearance-none block w-full text-gray-700 py-3 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="file"
            placeholder="Doe"
          />
        </div>
        <div class="w-full px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >Drug Description</label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Description"
          />
        </div>
      </div>
<vue-element-loading v-if="loading" :active="loading" :is-full-screen="true"/>
      <button
        @click.prevent="showAlert"
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
      >Submit</button>
    </form>
  </div>
</template>

<script>
import DrugCard from "@/components/DrugCard.vue";
export default {
  components: {
    DrugCard
  },
  data(){
      return{
          loading:false
      }
  },
  methods: {
    showAlert() {
        this.loading = true;
        const that = this;
      setTimeout(function() {
          that.loading = false
        that.$swal("Success!", "New Drug added!", "success");
      }, 1000);
    }
  }
};
</script>

<style scoped>
.title-text {
  font-size: 36px;
  line-height: 59px;
  text-align: center;
}
</style>