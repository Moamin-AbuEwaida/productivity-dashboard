<template>
  <div class="space-y-7 w-full">
    <h3 class="text-3xl font-bold">Tasks For Today</h3>
    <div class="flex flex-col space-y-4">
      <Task v-for="(task, index) in tasks" :key="index" :task="task" />
    </div>
  </div>
</template>

<script>
import Task from "./Task.vue";
export default {
  components: { Task },
  data() {
    return {
      tasks: [
        {
          name: "Mobile App",
          desc: "Preparing Figma file",
          color: "color_1",
          active: true,
        },
        {
          name: "UX Wireframe",
          desc: "Design UX Wireframe",
          color: "color_2",
          active: false,
        },
        {
          name: "Mobile App",
          desc: "Research",
          color: "color_3",
          active: false,
        },
      ],
    };
  },
};
</script>

<style></style>
