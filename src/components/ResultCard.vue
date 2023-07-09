<template>
  <div class="absolute -bottom-12 w-full flex justify-center items-center">
    <div class="w-4/5 flex justify-between divide-x bg-white rounded-lg md:p-4 lg:p-6">
      <ResultItem>
        <template #title>IP ADDRESS</template>
        <template #content>
          <span>192.212.174.101</span>
        </template>
      </ResultItem>

      <ResultItem class="ps-4">
        <template #title>LOCATION</template>
        <template #content>
          <span>Broklyn, Ny</span>
          10001
        </template>
      </ResultItem>

      <ResultItem class="ps-4">
        <template #title>TIMEZONE</template>
        <template #content>
          <span>UTC -05:00</span>
        </template>
      </ResultItem>

      <ResultItem class="ps-4">
        <template #title>ISP</template>
        <template #content>
          <span>STARLINK</span>
        </template>
      </ResultItem>
    </div>
  </div>
</template>

<script>
import ResultItem from "./ResultItem.vue";

export default {
  name: "result-card",
  components: {
    ResultItem,
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
