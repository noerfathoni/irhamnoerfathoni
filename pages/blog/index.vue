<template>
  <div class="wrapper">
    <nav class="nav-menu">
      <ul>
        <li>
          <nuxt-link to="/" active-class="active" exact>
            HOME
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/projects" active-class="active">
            PROJECTS
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about" active-class="active">
            ABOUT
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/blog" active-class="active">
            BLOG
          </nuxt-link>
        </li>
      </ul>
    </nav>
    <div class="content">
      <h1 class="text-4xl font-bold mb-4">BLOG</h1>
      <div v-for="blog in blogs" :key="blog.title" class="mb-8">
        <h4 class="font-bold text-2xl">{{ blog.title }}</h4>
        <p>{{ blog.description }}</p>
      </div>
    </div>
    <footer class="text-center p-5 justify-center w-full">
      &copy; 2020 Irham Nur Fathoni. Powered By
      <a class="underline" href="https://nuxtjs.org/">NuxtJS</a>
    </footer>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const blogs = await $content('blog').fetch()
    
    return {
      blogs
    }
  }
}
</script>
