<script setup>
import { ref } from "vue";
import Alert from "../components/Alert.vue";

const scriptURL = import.meta.env.VITE_GOOGLE_SCRIPT_URL;
const alertTimeout = 5000;

const loading = ref(false);
const alert = ref({
  message: null,
  success: false,
});

function validateForm(form) {
  const inputs = form.querySelectorAll("input, textarea");

  for (let input of inputs) {
    if (input.value == "") {
      setAlert(input.getAttribute("name") + " not filled!", false);
      return false;
    }
  }
  return true;
}

function setAlert(message, success) {
  alert.value.message = message;
  alert.value.success = success;

  setTimeout(function () {
    alert.value.message = null;
    alert.value.success = false;
  }, alertTimeout);
}

function submitForm(event) {
  const form = event.target;

  if (!validateForm(form)) {
    return;
  }

  const controller = new AbortController();
  const signal = controller.signal;

  setTimeout(() => {
    controller.abort();
  }, 15000);

  loading.value = true;

  fetch(scriptURL, { method: "POST", body: new FormData(form), signal })
    .then((response) => {
      if (!response.ok) {
        throw Error("Failed to send message!");
      }
      setAlert("Message sent successfully!", true);
      form.reset();
    })
    .catch((err) => {
      setAlert(err.message, false);
    })
    .finally(() => {
      loading.value = false;
    });
}
</script>

<template>
  <section id="contact" class="w-full px-4 py-16 bg-base-200">
    <div class="mx-auto max-w-screen-lg">
      <h1 class="text-4xl font-semibold sm:text-6xl">Contact</h1>
      <div class="grid pt-6 gap-8 md:grid-cols-2">
        <p>
          Feel free to drop me a message! Whether you have a project in mind or
          just want to say hello, I'm all ears. I look forward to connecting
          with you and exploring how we can collaborate on something amazing!
        </p>
        <form
          name="submit-to-google-sheet"
          class="flex flex-col space-y-4 p-8 bg-base-100 rounded-md"
          @submit.prevent="submitForm"
        >
          <input
            type="text"
            placeholder="Full Name"
            name="Name"
            class="input input-bordered w-full"
          />
          <input
            type="email"
            placeholder="Email"
            name="Email"
            class="input input-bordered w-full"
          />
          <textarea
            placeholder="Write you message..."
            rows="4"
            name="Message"
            class="textarea textarea-bordered text-base"
          ></textarea>
          <button
            :disabled="loading"
            type="submit"
            class="btn btn-primary w-full"
          >
            <span :class="{ 'animate-spin': loading }">{{
              loading ? "&#8635;" : "Submit"
            }}</span>
          </button>
        </form>
        <Alert :alert="alert" />
      </div>
    </div>
  </section>
</template>
