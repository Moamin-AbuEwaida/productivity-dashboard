<template>
  <div class="relative grid grid-cols-12 border-r-2 h-full">
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
      <button class="bg-stone-300 p-2 rounded-lg">
        <mdicon name="menu" />
      </button>
    </div>
    <div class="col-span-12 lg:block">
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
    <div class="col-span-12 p-10">
      <NavBarMenu />
    </div>
    <div class="absolute bottom-0 left-0">
      <svg width="200" height="100" viewBox="-100 -100 200 200">
        <polygon points="0,0 80,120 -80,120" fill="#234236" />
        <polygon points="0,-40 60,60 -60,60" fill="#0C5C4C" />
        <polygon points="0,-80 40,0 -40,0" fill="#38755B" />
        <rect x="-20" y="120" width="40" height="30" fill="brown" />
      </svg>
    </div>
  </div>
</template>

<script>
import NavBarMenu from "./NavBarMenu.vue";
export default {
  name: "NavBar",
  components: { NavBarMenu },
};
</script>

<style></style>
