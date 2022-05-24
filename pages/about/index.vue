<template>
  <div class="bg-gray-200">
    <div class="page-content" v-if="data">
      <div class="title text-center w-full">
        <h1 class="font-mono  text-yellow-500 pt-20 lg:text-7xl md:text-6xl sm:text-5xl xs:text-4xl">
          {{ data.title }}
        </h1>
        <h2 class="text-gray-700 p-10 lg:text-5xl md:text-4xl sm:text-3xl">{{ data.subtitle }}</h2>
        <div
          class="
            w-full
            grid grid-cols-1
            lg:grid-cols-1
            xl:grid-cols-2
            gap-10
            w-4/5
            mx-auto
            my-10
          "
        >
          <div class="wrapper">
            <img class="rounded-2xl w-full" :src="data.image.filename" alt="" />
          </div>

          <div
            class="
              paragraph
              w-full
              my-auto
              mx-auto
              shadow-xl
              rounded-xl
              bg-red-300
              border-solid border-neutral-100 border-2
            "
          >
            <p class="font-mono leading-normal text-white xl:text-2xl p-10 lg:text-3xl p-5 md:text-2xl sm:text-2xl">
              {{ data.description }}
            </p>
          </div>
        </div>
      </div>
      <!-- card-section -->
      <div
        class="
         w-full
          card-section
          text-center
          text-slate-500
          lg:text-3xl
          md:text-2xl
          sm:text-xl
        "
      >
        <div
          class="

            w-3/5
            card1
            rounded
            overflow-hidden
            shadow-lg
            bg-red-200
            border-solid border-neutral-100 border-2
            mx-auto
            mt-10
            p-5
          "
        >
          <h2 class="tip1 ">{{ data.tip1 }}</h2>
        </div>
        <div
          class="
            w-3/5
            card2
            rounded
            overflow-hidden
            shadow-lg
            bg-red-200
            border-solid border-neutral-100 border-2
             mx-auto
            mt-10
            p-5
          "
        >
          <h2 class="tip2">{{ data.tip2 }}</h2>
        </div>
        <div
          class="
            w-3/5
            card3
            rounded
            overflow-hidden
            shadow-lg
            bg-red-200
            border-solid border-neutral-100 border-2
             mx-auto
            mt-10
            p-5
          "
        >
          <h2 class="tip3">{{ data.tip3 }}</h2>
        </div>
        <div
          class="
            w-3/5
            card3
            rounded
            overflow-hidden
            shadow-lg
            bg-red-200
            border-solid border-neutral-100 border-2
             mx-auto
            mt-10
            p-5
          "
        >
          <h2 class="tip4">{{ data.tip4 }}</h2>
        </div>
        <div
          class="
            w-3/5
            card3
            rounded
            overflow-hidden
            shadow-lg
            bg-red-200
            border-solid border-neutral-100 border-2
             mx-auto
            mt-10
            p-5
          "
        >
          <h2 class="tip5">{{ data.tip5 }}</h2>
        </div>
      </div>
       <div
          class="
            w-full
            grid grid-cols-1
            lg:grid-cols-1
            xl:grid-cols-2
            gap-10
            w-4/5
            mx-auto
            mt-10
            px-5
            pb-10
          "
        >
          <div class="wrapper">
            <img class="rounded-2xl w-full" :src="data.image2.filename" alt="" />
          </div>

          <div
            class="
              paragraph
              w-full
              my-auto
              mx-auto
              shadow-xl
              rounded-xl
              bg-red-300
              border-solid border-neutral-100 border-2
            "
          >
            <p class="font-mono  leading-normal text-white p-10 xl:text-2xl lg:text-3xl md:text-2xl sm:text-xl">
              {{ data.info }}
            </p>
          </div>
        </div>
    </div>
  </div>
</template>
<script setup>
import { ref, onMounted } from "vue";
// fetch data from storyblok
const data = ref(null);
onMounted(async () => {
  data.value = await fetch(
    "https://api.storyblok.com/v2/cdn/stories/tips-content?version=draft&token=HHShNjDzKdOnykCsj3lFUQtt&"
  )
    .then((response) => response.json())
    .then(({ story }) => story.content);
});
</script>
