<template>
  <div class="flex flex-col md:flex-row items-center md:items-stretch gap-8">
    <Project
      v-for="(project, index) in projects"
      :key="index"
      class="w-full md:w-1/3"
      :project="project"
    />
  </div>
</template>

<script>
import Project from "./Project.vue";

export default {
  data() {
    return {
      projects: [
        {
          name: "Web Development",
          tasks: 10,
          percentage: 96,
          people: 3,
          color: "color_1",
        },
        {
          name: "Mobile App Design",
          tasks: 12,
          percentage: 26,
          people: 9,
          color: "color_2",
        },
        {
          name: "Facebook Brand UI Kit",
          tasks: 22,
          percentage: 73,
          people: 5,
          color: "color_3",
        },
      ],
    };
  },
  components: { Project },
};
</script>
