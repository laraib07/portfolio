<template>
  <section id="hero" class="w-full min-h-screen px-4 bg-base-100">
    <div class="flex flex-row items-center max-w-screen-xl h-screen mx-auto">
      <div class="md:w-1/2">
        <h2 class="text-xl">Fullstack Developer</h2>
        <h1 class="text-6xl font-bold">Hi, I am Laraib.</h1>
        <div id="hero_cta" class="pt-4">
          <button name="portfolio" class="btn btn-primary">Portfolio</button>
          <button name="contact" class="btn btn-outline border-2 ml-4">
            Contact
          </button>
        </div>
      </div>
      <div class="hidden items-center pt-16 md:block">
        <img
          src="/images/hero.webp"
          alt="hero image"
          loading="lazy"
          class="object-contain h-screen py-20 mx-auto"
        />
      </div>
    </div>
  </section>
</template>
