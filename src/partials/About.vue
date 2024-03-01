<script setup>
import Github from "../components/icons/Github.vue";
import Linkedin from "../components/icons/Linkedin.vue";
import Leetcode from "../components/icons/Leetcode.vue";
</script>

<template>
  <section id="about" class="w-full px-4 py-16 bg-base-200">
    <div class="flex flex-col mx-auto max-w-screen-xl lg:flex-row lg:w-[90vw]">
      <div class="max-h-[400px] rounded-lg overflow-hidden lg:w-1/2">
        <img src="/images/my_image.webp" alt="Laraib's image" />
      </div>
      <div class="pt-8 lg:pl-8 lg:w-1/2">
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
          <!-- Leetcode -->
          <a
            href="https://leetcode.com/laraib07/"
            target="_blank"
            class="opacity-90 hover:opacity-100"
          >
            <Leetcode />
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
