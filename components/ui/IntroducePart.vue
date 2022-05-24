<template>
  <section class="grid md:grid-cols-1 lg:grid-cols-3 bg-gray-200 sm:gap-10 pb-20">
    <div class="flex flex-col col-span-1">
      <slot name="about-image"></slot>
    </div>
    <div class="grid grid-cols-1 sm:col-span-1 md:col-span-2 items-center">
      <h2 class="sm:text-3xl md:text-4xl lg:text-3xl xl:text-4xl text-gray-500 sm:px-10 sm:py-2 md:p-5">
        {{ introduceTitle }}
      </h2>
      <p class="sm:text-2xl md:text-3xl lg:text-xl xl:text-3xl text-gray-700 sm:px-10 sm:py-6 md:p-5">
        {{ introduceDescription }}
      </p>
      <slot name="links"></slot>
    </div>
  </section>
</template>

<script setup>
const props = defineProps({
  introduceTitle: {
    type: String,
    default: "Title",
  },
  introduceDescription: {
    type: String,
    default: "Description",
  },
});
</script>
