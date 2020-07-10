<template>
  <div class="wrapper">
    <div class="content-home">
      <div class="profile-img">
        <img src="~assets/img/my-profile.png" />
      </div>
      <h1 class="font-bold text-2xl mt-10 mb-3">IRHAM NUR FATHONI</h1>
      <h2 class="mb-12">Web and Mobile Dev</h2>
      <div class="social-group">
        <a class="social-link" href="mailto:noer.fathoni1@gmail.com" target="_blank">
          <i class="la la-envelope"></i>
        </a>
        <a class="social-link" href="https://github.com/noerfathoni/" target="_blank">
          <i class="lab la-github"></i>
        </a>
        <a class="social-link" href="https://www.instagram.com/noerirham/" target="_blank">
          <i class="lab la-instagram"></i>
        </a>
        <a class="social-link" href="https://www.linkedin.com/in/irham-nur-fathoni-207626139" target="_blank">
          <i class="lab la-linkedin"></i>
        </a>
      </div>
      <div class="nav mb-10">
        <nuxt-link to="/" active-class="active" exact class="nav-item active">
          HOME
        </nuxt-link>
        <nuxt-link to="/about" active-class="active" class="nav-item">
          ABOUT
        </nuxt-link>
        <nuxt-link to="/blog" active-class="active" class="nav-item">
          BLOG
        </nuxt-link>
      </div>
    </div>
    <footer class="text-center p-5 justify-center w-full">
      &copy; 2020 Irham Nur Fathoni. Powered By
      <a class="underline" href="https://nuxtjs.org/" target="_blank">NuxtJS</a>
    </footer>
  </div>
</template>

<script>
export default {
  head () {
    return {
      title: 'Irham Nur Fathoni',
    }
  }
}
</script>
