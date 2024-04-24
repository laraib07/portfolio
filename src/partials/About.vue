<script setup>
import Github from "../components/icons/Github.vue";
import Linkedin from "../components/icons/Linkedin.vue";
import Leetcode from "../components/icons/Leetcode.vue";
import Medium from "../components/icons/Medium.vue";
</script>

<template>
  <section id="about" class="w-full px-4 py-16 bg-base-200">
    <div
      class="grid gap-8 mx-auto max-w-screen-lg place-items-center md:grid-cols-2"
    >
      <div
        class="relative rounded-lg overflow-hidden w-full max-h-[400px] flex justify-center"
      >
        <img
          src="/images/my_image.webp"
          alt="Laraib's image"
          class="object-cover w-full blur-sm"
        />
        <img
          src="/images/my_image.webp"
          alt="Laraib's image"
          class="absolute object-contain h-full"
        />
      </div>
      <article>
        <h1 class="text-4xl font-semibold sm:text-6xl">About Me</h1>
        <p class="pt-6">
          Web developer specializing in full-stack development using Laravel,
          Django, MERN, MEVN, HTML, CSS, and JavaScript. Committed to crafting
          seamless and user-centric web experiences. Let's transform ideas into
          code and build something extraordinary together!
        </p>
        <div class="flex gap-4 items-center pt-6">
          <!-- Github  -->
          <a
            href="https://github.com/laraib07"
            target="_blank"
            class="opacity-90 hover:opacity-100"
          >
            <Github />
          </a>
          <!-- Linkedin -->
          <a
            href="https://www.linkedin.com/in/laraib07/"
            target="_blank"
            class="opacity-90 hover:opacity-100"
          >
            <Linkedin />
          </a>
          <!-- Medium -->
          <a
            href="https://medium.com/@work.laraib"
            target="_blank"
            class="opacity-90 hover:opacity-100"
          >
            <Medium />
          </a>
          <!-- Leetcode -->
          <a
            href="https://leetcode.com/laraib07/"
            target="_blank"
            class="opacity-90 hover:opacity-100"
          >
            <Leetcode />
          </a>
        </div>
      </article>
    </div>
  </section>
</template>
