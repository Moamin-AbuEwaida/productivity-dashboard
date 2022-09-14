<template>
  <div class="space-y-7">
    <h3 class="text-3xl font-bold">Statistics</h3>
    <div class="flex flex-col md:flex-row gap-4">
      <div
        class="bg-stone-200 rounded-xl p-4 flex-1 space-y-10"
        v-for="({ title, value }, index) in stats"
        :key="index"
      >
        <p class="inline-block text-5xl">{{ value }}</p>
        <h6 class="text-lg">{{ title }}</h6>
      </div>
      <button
        class="hover:bg-white transform transition hover:-translate-y-1 border-2 border-dashed rounded-xl p-4 flex flex-col justify-between items-center"
      >
        <mdicon name="plus" class="border-2 rounded-full w-7" />
        <span class="text-lg">New Widget</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      stats: [
        {
          title: "Tracked time",
          value: "24h",
        },
        {
          title: "Finished tasks",
          value: "18",
        },
      ],
    };
  },
};
</script>

<style></style>
