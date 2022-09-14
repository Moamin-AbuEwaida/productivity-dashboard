<template>
  <div
    class="relative bg-white shadow-orange-50 shadow-2xl p-7 rounded-xl flex"
  >
    <div
      class="absolute top-0 left-0 w-2 h-full rounded-l-xl"
      :class="`bg-${task.color}`"
    ></div>
    <div class="flex-1">
      <h6 class="font-bold">{{ task.name }}</h6>
      <p>{{ task.desc }}</p>
    </div>
    <button
      class="flex justify-center items-center w-7 h-7 border rounded-full"
      @click="() => (task.active = !task.active)"
    >
      <mdicon
        name="check"
        v-if="task.active"
        class="w-7 text-white bg-black rounded-full"
      />
    </button>
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
