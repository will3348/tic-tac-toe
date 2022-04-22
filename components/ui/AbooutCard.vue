<template>
  <section class="grid sm:grid-cols-1 md:grid-cols-3 bg-gray-200 sm:gap-10">
    <div class="flex flex-col col-span-1">
      <slot name="about-image"></slot>
    </div>
    <div class="grid grid-cols-1 sm:col-span-1 md:col-span-2 items-center">
      <h2 class="sm:text-3xl md:text-6xl text-white sm:px-10 sm:py-2 md:p-10">
        {{ aboutTitle }}
      </h2>
      <p class="sm:text-2xl md:text-4xl text-gray-700 sm:px-10 sm:py-6 md:p-10">
        {{ aboutDescription }}
      </p>
      <slot name="links"></slot>
    </div>
  </section>
</template>

<script setup>
const props = defineProps({
  aboutTitle: {
    type: String,
    default: "About Card Title",
  },
  aboutDescription: {
    type: String,
    default: "About Card Description",
  },
});
</script>
