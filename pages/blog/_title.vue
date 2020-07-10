<template>
  <div class="wrapper">
    <Navbar />
    <div class="content">
      <h1 class="text-4xl font-bold mb-4">{{ result.title }}</h1>
      <p><i class="la la-calendar"></i> {{ $moment(result.createdAt).format('dddd, DD MMMM YYYY') }}</p>
      <br />
      <nuxt-content :document="result" />
    </div>
    <footer class="text-center p-5 justify-center w-full">
      &copy; 2020 Irham Nur Fathoni. Powered By
      <a class="underline" href="https://nuxtjs.org/">NuxtJS</a>
    </footer>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'

export default {
  components: {
    Navbar
  },
  async asyncData ({ $content, params }) {
    const detailPage = await $content('blog').where({ 'slug': params.title }).fetch()
    const result = detailPage[0]

    return {
      result
    }
  }  ,
  head () {
    return {
      title: this.result.title,
    }
  }
}
</script>
