<template>
  <div class="flex-wrap justify-around p-10 bg-gray-300">
    <div>
    <a href="/"><span class=" font-bold text-indigo-400 lg:text-6xl md:text-5xl sm: text-5xl"
          >Tic Tac Toe</span></a>
    </div>
    <div class="flex  justify-end mt-5">
      <nav class="flex flex-row justify-around md:gap-36 sm: gap-12">
         <NuxtLink class="text-gray-500  hover:text-white md:text-2xl sm:text-xl" to="/"
          >Home</NuxtLink
        >
        <NuxtLink class="text-gray-500 hover:text-white md:text-2xl sm:text-xl" to="/game"
          >Game</NuxtLink
        >
       
        <NuxtLink class="text-gray-500 hover:text-white md:text-2xl sm:text-xl" to="/about"
          >Tips</NuxtLink
        >
      </nav>
    </div>
  </div>
</template>

<script setup></script>
