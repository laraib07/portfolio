<script setup></script>

<template>
  <section
    id="hero"
    class="w-full px-4 bg-base-100"
    style="background-image: url('/images/circuit-board.svg')"
  >
    <div
      class="relative grid place-content-center max-w-screen-xl h-[100vh] mx-auto"
    >
      <div class="flex flex-col items-center text-center w-full">
        <h1 class="text-6xl font-extrabold sm:text-8xl">Hi, I am Laraib</h1>
        <p
          class="text-lg mt-6 p-4 border-2 rounded-md border-base-300 bg-base-100 sm:text-xl"
        >
          A
          <span
            class="bg-gradient-to-r from-primary to-secondary bg-clip-text text-transparent"
          >
            Fullstack Developer
          </span>
          proficient in Laravel, Django and MEVN
        </p>

        <div class="flex gap-2 pt-6">
          <a href="#portfolio" class="btn btn-primary">Portfolio</a>
          <a href="#contact" class="btn border-2 ml-4">Contact</a>
        </div>

        <div
          class="absolute bottom-8 text-6xl animate-bounce bg-gradient-to-b from-primary to-secondary bg-clip-text text-transparent"
        >
          &darr;
        </div>
      </div>
    </div>
  </section>
</template>
