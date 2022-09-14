<template>
  <div
    class="rounded-xl text-white p-4 flex justify-between flex-col gap-7"
    :class="`bg-${project.color}`"
  >
    <div class="flex justify-between items-center">
      <div class="flex -space-x-2">
        <img
          v-for="(image, index) in images"
          :src="image"
          :key="index"
          alt="person"
          class="inline-block w-8 h-8 rounded-full ring-2"
          :class="`ring-${project.color}`"
        />
        <button
          class="bg-black flex justify-center items-center rounded-full w-8 h-8"
        >
          <span class="text-sm">+ {{ project.people }}</span>
        </button>
      </div>
      <button>
        <mdicon name="dots-vertical" />
      </button>
    </div>
    <h3 class="font-bold text-3xl">{{ project.name }}</h3>
    <div class="space-y-2">
      <p>
        <span>{{ project.tasks }} tasks</span> |
        <span>{{ project.percentage }} tasks%</span>
      </p>
      <div class="relative h-2 bg-black bg-opacity-20 rounded-xl">
        <span
          class="absolute bg-gray-200 h-2 top-0 left-0 rounded-xl"
          :style="`width:${project.percentage}%`"
          >{{}}</span
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      images: [
        "https://images.unsplash.com/photo-1528892952291-009c663ce843?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=344&q=80",
        "https://images.unsplash.com/photo-1441622915984-05d13dfb3d8c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80",
      ],
    };
  },
};
</script>
