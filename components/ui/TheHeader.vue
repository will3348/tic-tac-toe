<template>
  <div class="flex justify-around p-10 bg-gray-300">
    <div>
    <a href="/"><span class="text-6xl font-bold text-indigo-400"
          >Tic Tac Toe</span></a>
    </div>
    <div class="sm:flex sm:flex-col">
      <nav class="flex sm:flex-col md:flex-row justify-around md:gap-36">
         <NuxtLink class="text-gray-500 text-2xl hover:text-white" to="/"
          >Home</NuxtLink
        >
        <NuxtLink class="text-gray-500 text-2xl hover:text-white" to="/game"
          >Game</NuxtLink
        >
       
        <NuxtLink class="text-gray-500 text-2xl hover:text-white" to="/about"
          >Tips</NuxtLink
        >
      </nav>
    </div>
  </div>
</template>

<script setup></script>
