<template>
  <div class="wrapper">
    <Navbar />
    <div class="content">
      <h1 class="text-4xl font-bold mb-4">ABOUT</h1>
      <img src="~assets/img/leaf.jpg" class="shadow-xl mb-8 rounded-lg object-cover" style="filter: grayscale(100%); height: 24rem;" />
      <p class="about-text">
        The icy  fingers of Pneumonia also touched Johnsy. She was very ill, lying in her bed and not moving at all. 
        A doctor visited her every day but Johnsy was not getting better. One morning, the doctor spoke to 
        Sueoutside Johnsy's room, <br /> 
        “I can' t help her,” the doctor said. “She is very sad and has no desire to live. <br />
        Someone must make her happy again. What is she interested in?” <br />
        “She is an artist,” Sue replied. “She wants to paint a picture of bay of Naples.” <br />
        “Painting!” said the doctor. “That won't help her!” <br />
        <span class="text-2xl leading-loose italic text-center">
        ~ "The Last Leaf"
        </span>
      </p>
      <h2 class="text-3xl font-bold mb-4">Topic Interests : </h2>
      <ol class="interest-list">
        <li>Flutter</li>
        <li>REST API</li>
        <li>PHP | NodeJS</li>
        <li>Vanilla | Vue | NuxtJS</li>
        <li>MySQL</li>
      </ol>
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
  head () {
    return {
      title: 'About | Irham Nur Fathoni',
    }
  }
}
</script>