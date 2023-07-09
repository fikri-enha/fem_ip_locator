<template>
  <div>
    <div class="text-xs font-medium text-gray-500">
      <slot name="title"> </slot>
    </div>
    <div class="text-xl font-medium text-gray-800 mt-2">
      <slot name="content"> </slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "result-item",
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
