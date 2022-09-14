<template>
  <div class="relative bg-white shadow-orange-50 shadow-2xl p-7 rounded-xl">
    <div
      class="absolute top-0 left-0 w-2 h-full rounded-l-xl"
      :class="`bg-${task.color}`"
    ></div>
  </div>
</template>

<script>
export default {
  props: {
    task: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style></style>
