<script setup>
import Greet from "@/components/Greet.vue";

const name = "Laraib";
</script>
<template>
  <section
    id="hero"
    class="w-full px-4 bg-base-100"
    style="background-image: url('./images/circuit-board.svg')"
  >
    <div
      class="grid place-content-center gap-12 max-w-screen-xl h-screen mx-auto"
    >
      <article
        class="text-center p-4 border-2 rounded-md border-base-300 bg-base-100 sm:text-xl sm:p-8"
      >
        <h1
          class="relative text-6xl leading-tight tracking-tight font-black sm:text-8xl"
        >
          <Greet :name="name" class="blur-sm" />
          <Greet :name="name" class="absolute inset-0" />
        </h1>
        <p class="pt-4 leading-snug">
          A
          <span class="relative">
            <span
              class="bg-gradient-to-r from-primary to-secondary bg-clip-text text-transparent"
            >
              Fullstack Developer
            </span>
            <span
              class="absolute inset-0 blur-sm bg-gradient-to-r from-primary to-secondary bg-clip-text text-transparent"
            >
              Fullstack Developer
            </span>
          </span>
          proficient in Laravel, Django and MEVN
        </p>
      </article>

      <div class="flex gap-2 justify-center">
        <a href="#portfolio" class="btn btn-primary">Portfolio</a>
        <a
          href="#contact"
          class="btn btn-outline bg-base-100 border-base-300 border-2 ml-4"
          >Contact</a
        >
      </div>
    </div>
  </section>
</template>
