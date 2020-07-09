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
      <h1 class="text-4xl font-bold mb-4">PROJECTS</h1>
      <p class="text-2xl leading-loose">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nisi a enim
        sed quae dolorum veniam libero delectus sunt, mollitia rerum harum
        inventore illo quidem officia ut. Adipisci active-class="active" exact
        laudantium cum voluptates. Lorem ipsum dolor sit amet consectetur,
        adipisicing elit. Nisi a enim sed quae dolorum veniam libero delectus
        sunt, mollitia rerum harum inventore illo quidem officia ut. Adipisci
        laudantium cum voluptates.
      </p>
    </div>
    <footer class="text-center p-5 justify-center w-full">
      &copy; 2020 Irham Nur Fathoni. Powered By
      <a class="underline" href="https://nuxtjs.org/">NuxtJS</a>
    </footer>
  </div>
</template>
