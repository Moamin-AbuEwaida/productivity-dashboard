<template>
  <div
    class="relative lg:space-y-10 lg:block p-2 grid grid-cols-12 border-r-2 h-full"
  >
    <div class="pl-10 col-span-6 flex justify-center items-center gap-4">
      <div
        class="bg-gradient-to-tl from-color_3 to-pink-500 rounded-xl p-2 text-white"
      >
        <mdicon
          name="checkbox-marked-circle-plus-outline"
          class="text-current"
        />
      </div>
      <strong>Producteevy</strong>
    </div>
    <div class="lg:hidden col-span-6 flex justify-end items-center">
      <button class="bg-stone-300 p-2 rounded-lg" @click="toggleMenu">
        <mdicon name="menu" />
      </button>
    </div>
    <div class="col-span-12 hidden lg:block">
      <div class="relative w-full h-24 flex flex-col items-center gap-4">
        <img
          src="https://images.unsplash.com/photo-1508214751196-bcfd4ca60f91?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80"
          alt="sara"
          class="w-24 h-24 rounded-full"
        />
        <p
          class="absolute bg-white -bottom-2 left-1/2 transform -translate-x-1/2 px-2 text-xs text-orange-500 flex items-center gap-1 rounded-full"
        >
          <mdicon name="clock" width="15px" />
          <span class="font-bold">10h</span>
        </p>
      </div>
      <div class="text-center mt-7">
        <h1 class="font-bold text-black-900">Sarah Connor</h1>
        <a href="#" class="text-grey-500">Sara@test.com</a>
      </div>
    </div>
    <div
      class="col-span-12 p-10 flex items-center justify-center"
      v-if="menuIsActive"
    >
      <NavBarMenu />
    </div>
    <div class="hidden lg:block absolute bottom-0 left-0 px-[25%]">
      <svg width="100" height="100" viewBox="-100 -100 200 200">
        <defs>
          <path
            id="branch"
            d="
        M 0 0 L 0 -90
        M 0 -20 L 20 -34
        M 0 -20 L -20 -34
        M 0 -40 L 20 -54
        M 0 -40 L -20 -54
        M 0 -60 L 20 -74
        M 0 -60 L -20 -74"
            stroke="#E5C39C"
            stroke-width="5"
          />
        </defs>

        <use href="#branch" />
        <use href="#branch" transform="rotate(60)" />
        <use href="#branch" transform="rotate(120)" />
        <use href="#branch" transform="rotate(180)" />
        <use href="#branch" transform="rotate(240)" />
        <use href="#branch" transform="rotate(300)" />
      </svg>
    </div>
  </div>
</template>

<script setup>
import NavBarMenu from "./NavBarMenu.vue";
import { ref } from "vue";

const MODILE_BREAKPOINT = 1024;
const width = ref(document.body.offsetWidth);
const menuIsActive = ref(width.value > MODILE_BREAKPOINT);

const toggleMenu = () => (menuIsActive.value = !menuIsActive.value);
window.addEventListener("resize", () => {
  width.value = document.body.offsetWidth;
  menuIsActive.value = width.value > MODILE_BREAKPOINT;
});
</script>

<style></style>
~~
