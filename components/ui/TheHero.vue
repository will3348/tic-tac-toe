<template>
  <div
    class="xs:flex flex-col-reverse md:grid md:grid-cols-3 py-10 bg-gray-200"
  >
    <div class="col-span-1 text-center self-center m-6">
      <div class="flex flex-col py-10">
        <h1 class="text-gray-500 mb-6 xl:text-6xl lg:text-5xl md:text-3xl sm:text-3xl ">
          {{ heroTitle }}
        </h1>
        <slot name="hero-description"></slot>
      </div>
      <div class="flex flex-col justify-between gap-10">
        <slot name="links"></slot>
      </div>
    </div>
    <div class="col-span-2 place-self-stretch">
      <slot name="hero-image"></slot>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  heroTitle: {
    type: String,
    default: "Hero Title",
  },
});
</script>
