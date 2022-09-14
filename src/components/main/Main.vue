<template>
  <div class="flex flex-col gap-10 p-7">
    <HelloBar />
    <CurrentProjects />
    <div class="grid grid-cols-12 grid-rows-2 gap-10">
      <TasksForToday class="row-span-2 col-span-12 md:col-span-6" />
      <Stats class="row-span-1 col-span-12 md:col-span-6" />
      <Proplan class="row-span-1 col-span-12 md:col-span-6" />
    </div>
  </div>
</template>

<script setup>
import HelloBar from "./HelloBar.vue";
import CurrentProjects from "./CurrentProjects.vue";
import TasksForToday from "./TasksForToday.vue";
import Stats from "./Stats.vue";
import Proplan from "./Proplan.vue";
</script>

<style></style>
