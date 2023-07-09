<template>
  <div class="w-full flex justify-center items-center">
    <div class="w-5/12">
      <div class="font-medium text-2xl text-center py-2 text-white">IP Address Tracker</div>
      <div class="flex">
        <input
          type="text"
          name="ipInput"
          id=""
          class="block w-full rounded-l-md border-0 text-sm text-gray-900 placeholder:text-gray-400 sm:text-sm sm:leading-6 p-2.5"
          placeholder="Search for any IP address or domain"
        />
        <button
          type="button"
          class="flex-shrink-0 p-3.5 rounded-r-md bg-gray-700 text-white"
        >
          <img src="../assets/images/icon-arrow.svg" alt="" />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, computed, onMounted } from "vue";
export default {
  name: "search-box",
  components: {},

  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
