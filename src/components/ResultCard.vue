<template>
  <div class="absolute -bottom-40 md:-bottom-20 w-full flex justify-center items-center">
    <div class="w-4/5 flex flex-col md:flex-row items-center justify-between md:divide-x bg-white rounded-2xl md:rounded-xl py-6 px-2 md:p-4 lg:p-6">
      <ResultItem class="self-start md:w-1/4">
        <template #title>IP ADDRESS</template>
        <template #content>
          {{dataToShow.ipAddress}}
        </template>
      </ResultItem>

      <ResultItem class="self-start md:w-1/4 md:ps-4 mt-4 md:mt-0">
        <template #title>LOCATION</template>
        <template #content>
          {{dataToShow.location}}
        </template>
      </ResultItem>
      
      <ResultItem class="self-start md:w-1/4 md:ps-4 mt-4 md:mt-0">
        <template #title>TIMEZONE</template>
        <template #content>
          UTC {{dataToShow.timezone}}
        </template>
      </ResultItem>
      
      <ResultItem class="self-start md:w-1/4 md:ps-4 mt-4 md:mt-0">
        <template #title>ISP</template>
        <template #content>
          {{dataToShow.isp}}
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
  props: {
    dataToShow: {
      type: Object,
      required: true
    }
  },
  setup(props, {emit}) {

    return {

    };
  },
};
</script>

<style lang="scss" scoped></style>
