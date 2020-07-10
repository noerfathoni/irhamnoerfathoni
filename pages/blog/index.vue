<template>
  <div class="wrapper">
    <Navbar />
    <div class="content">
      <h1 class="text-4xl font-bold mb-4">BLOG</h1>
      <div v-for="blog in blogs" :key="blog.title" class="blog-item">
        <h4><nuxt-link :to="urlToDetail(blog.slug)">{{ blog.title }}</nuxt-link></h4>
        <p class="description">{{ blog.description }}</p>
        <p class="created-at">
          <i class="la la-calendar"></i>
          {{ $moment(blog.createdAt).format('dddd, DD MMMM YYYY') }}
        </p>
      </div>
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
  async asyncData ({ $content }) {
    const blogs = await $content('blog').sortBy('createdAt', 'desc').fetch()
    
    return {
      blogs
    }
  },
  methods: {
    urlToDetail (name) {
      return `/blog/${name}`
    }
  },
  head () {
    return {
      title: 'Blog | Irham Nur Fathoni',
    }
  }
}
</script>
