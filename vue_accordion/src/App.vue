<script setup lang="ts">
import AccordionBtn from './components/AccordionBtn.vue';
import DarkModeToggleBtn from './components/DarkModeToggleBtn.vue';
</script>

<template>
  <div class=" w-screen min-h-screen bg-white dark:bg-slate-700">
    <div class="w-full flex justify-around items-center mb-10">

      <h1 class="text-black dark:text-white text-xl font-bold ml-5 mt-5 mr-1">Accordion Menu Button Demo</h1>
      <DarkModeToggleBtn class="mr-5 mt-5 ml-1" />


    </div>



    <div class="m-5">
      <AccordionBtn />
    </div>

  </div>
</template>

<style scoped>
@media (prefers-reduced-motion: reduce) {

  * {
    transition: none !important;
  }
}
</style>
