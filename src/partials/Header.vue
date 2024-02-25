<script setup>
import { ref, onMounted } from "vue";
import BrandLogo from "../components/BrandLogo.vue";

const top = ref(true);
const drawerOpen = ref(false);

defineProps({
  resumeLink: {
    type: String,
    required: true,
  },
});

onMounted(() => {
  window.addEventListener("scroll", () => {
    if (top.value && window.scrollY > 10) {
      top.value = false;
    } else if (!top.value && window.scrollY <= 10) {
      top.value = true;
    }
  });
});
</script>

<template>
  <header
    :class="{ 'shadow-md': !top }"
    class="fixed top-0 right-0 left-0 px-4 py-2 backdrop-blur bg-base-100/30 z-50"
  >
    <div
      class="flex flex-col max-w-screen-xl mx-auto lg:items-center lg:flex-row"
    >
      <div class="flex flex-row flex-1 justify-between items-center">
        <BrandLogo />
        <div>
          <a
            :href="resumeLink"
            target="_blank"
            class="btn btn-primary border-2 mr-2 lg:hidden"
          >
            Resume
          </a>
          <button
            id="drawer"
            class="lg:hidden"
            @click="drawerOpen = !drawerOpen"
          >
            <svg
              height="64"
              width="64"
              fill="currentColor"
              viewBox="0 0 16 16"
              class="w-6 h-6"
            >
              <path
                v-show="!drawerOpen"
                fill-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                clip-rule="evenodd"
              ></path>
              <path
                v-show="drawerOpen"
                fill-rule="evenodd"
                d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                clip-rule="evenodd"
              ></path>
            </svg>
          </button>
        </div>
      </div>
      <nav
        :class="{ hidden: !drawerOpen, flex: drawerOpen }"
        class="flex flex-col lg:flex lg:flex-row lg:items-center"
        @click="drawerOpen = !drawerOpen"
      >
        <a href="#about" class="btn btn-ghost">About</a>
        <a href="#experience" class="btn btn-ghost">Experience</a>
        <a href="#portfolio" class="btn btn-ghost">Portfolio</a>
        <a href="#skills" class="btn btn-ghost">Skills</a>
        <a href="#contact" class="btn btn-ghost">Contact</a>
      </nav>

      <a
        :href="resumeLink"
        target="_blank"
        class="hidden btn btn-primary border-2 ml-2 lg:flex"
      >
        Resume
      </a>
    </div>
  </header>
</template>
