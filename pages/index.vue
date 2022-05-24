<template>
  <div class="h-full">
    <TheHero :hero-title="'Make The World A Better Place With Game'">
      <template #hero-image>
        <div class="flex justify-center">
          <img class="sm:w-screen md:w-3/4" src="public\image2.png" alt="Hero Image"
          />
        </div>
      </template>
      <template #links>
        <NuxtLink
          class="bg-white hover:bg-slate-300 text-gray-700 rounded-full text-base text-center lg:text-3xl md:text-2xl sm:text-xl"
          to="/game"
          >Play Now
        </NuxtLink>

        <NuxtLink
          class="bg-gray-500 hover:bg-gray-600 text-white focus:border-blue-400 rounded-full text-base text-center lg:text-3xl md:text-2xl sm:text-xl"
          to="/about"
          >Read some tips
        </NuxtLink>
      </template>
    </TheHero>
    <IntroducePart
      :introduceTitle= "`What is Tic Tac Toe?`"
      :introduceDescription= "`Tic-tac-toe  is a paper-and-pencil game for two players who take turns marking the spaces in a three-by-three grid with X or O. The player who succeeds in placing three of their marks in a horizontal, vertical, or diagonal row is the winner. It is a solved game, with a forced draw assuming best play from both players.`"
    >
      <template #about-image>
        <img
          class="w-10/12 self-center rounded-xl"
          src="public\image1.jpg"
          alt="image"
        />
      </template>
      <template #links>
        <NuxtLink
          class="px-10 sm:pt-10 hover:text-black text-gray-500 md:text-3xl sm:text-xl"
          to="/about"
          >Learn more Tips --></NuxtLink
        >
      </template>
    </IntroducePart>
  </div>
</template>
