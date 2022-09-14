<template>
  <div class="flex flex-col gap-10 p-7">
    <HelloBar />
    <CurrentProjects />
    <TasksForToday class="row-span-2 col-span-12 md:col-span-6" />
    <div class="grid grid-cols-12 grid-rows-2 gap-10">
      <div class="row-span-1 col-span-12 md:col-span-6 bg-debug">stats</div>
      <div class="row-span-1 col-span-12 md:col-span-6 bg-debug">ProPlan</div>
    </div>
  </div>
</template>

<script setup>
import HelloBar from "./HelloBar.vue";
import CurrentProjects from "./CurrentProjects.vue";
import TasksForToday from "./TasksForToday.vue";
</script>

<style></style>
