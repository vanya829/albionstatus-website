<template>
  <section class="flex flex-col items-center mt-6">
    <h1 class="my-2">
      Nothing to see here!
    </h1>
    <p class="leading-loose mt-4">
      Looks like you took a wrong path!
    </p>
    <nuxt-link
      to="/"
      class="gray-900 my-4"
    >
      Back
    </nuxt-link>
    <img src="https://thecatapi.com/api/images/get?format=src&type=gif">
  </section>
</template>

<script>
export default {
  props: {
    error: {
      type: Object,
      required: true
    }
  },
  head () {
    return {
      title: `${this.error.statusCode} - No server status here!`
    }
  }
}
</script>
