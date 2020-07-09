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
export default {
  async asyncData ({ $content, params }) {
    const detailPage = await $content('blog').where({ 'slug': params.title }).fetch()
    const result = detailPage[0]

    return {
      result
    }
  }  
}
</script>
