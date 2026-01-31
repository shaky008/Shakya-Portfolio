<template>
  <nav class="navbar">
    <div class="nav-brand">US</div>
    <ul class="nav-links">
      <li><a href="#home" @click.prevent="scrollTo('home')">Home</a></li>
      <li>
        <a href="#background" @click.prevent="scrollTo('background')"
          >Background</a
        >
      </li>
      <li>
        <a href="#projects" @click.prevent="scrollTo('projects')">Projects</a>
      </li>
      <li>
        <a href="#contact" @click.prevent="scrollTo('contact')">Contact</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  methods: {
    scrollTo(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: "smooth" });
      }
    },
  },
};
</script>
