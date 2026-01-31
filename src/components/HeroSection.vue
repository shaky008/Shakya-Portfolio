<template>
  <section id="home" class="hero">
    <div class="hero-content">
      <p class="hero-greeting">Hello, I am</p>
      <h1 class="hero-name">Utsav Shakya</h1>
      <p class="hero-tagline">
        <span class="typing-text">{{ displayedText }}</span>
        <span class="cursor">|</span>
      </p>
      <p class="hero-description">
        Passionate about technology, IT and security, and building solutions
        that make a difference. Currently exploring opportunities in IT,
        cybersecurity and software development.
      </p>
      <div class="hero-cta">
        <a
          href="#projects"
          @click.prevent="scrollTo('projects')"
          class="btn btn-primary"
          >View My Work</a
        >
        <a
          href="#contact"
          @click.prevent="scrollTo('contact')"
          class="btn btn-secondary"
          >Get In Touch</a
        >
      </div>
    </div>
    <div class="hero-visual">
      <div class="code-block">
        <span class="code-line">
          <span class="code-keyword">const</span> developer = {
        </span>
        <span class="code-line">
          &nbsp;&nbsp;name: <span class="code-string">"Utsav Shakya"</span>,
        </span>
        <span class="code-line">
          &nbsp;&nbsp;interests: [<span class="code-string"
            >"Cybersecurity"</span
          >, <span class="code-string">"Development"</span>,
          <span class="code-string">Football</span>,
          <span class="code-string">🐐Lebron James</span>],
        </span>
        <span class="code-line">
          &nbsp;&nbsp;isHireable: <span class="code-boolean">true</span>
        </span>
        <span class="code-line">};</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HeroSection",
  data() {
    return {
      phrases: [
        "Aspiring IT & Cybersecurity Professional",
        "Software Developer",
        "Problem Solver",
        "Security Enthusiast",
      ],
      currentPhraseIndex: 0,
      displayedText: "",
      isDeleting: false,
      typeSpeed: 100,
    };
  },
  mounted() {
    this.typeEffect();
  },
  methods: {
    typeEffect() {
      const currentPhrase = this.phrases[this.currentPhraseIndex];

      if (this.isDeleting) {
        // Remove characters
        this.displayedText = currentPhrase.substring(
          0,
          this.displayedText.length - 1
        );
      } else {
        // Add characters
        this.displayedText = currentPhrase.substring(
          0,
          this.displayedText.length + 1
        );
      }

      // Determine typing speed
      let speed = this.isDeleting ? 50 : this.typeSpeed;

      // If word is complete
      if (!this.isDeleting && this.displayedText === currentPhrase) {
        speed = 2000; // Pause at end
        this.isDeleting = true;
      } else if (this.isDeleting && this.displayedText === "") {
        this.isDeleting = false;
        this.currentPhraseIndex =
          (this.currentPhraseIndex + 1) % this.phrases.length;
        speed = 500; // Pause before typing next
      }

      setTimeout(() => this.typeEffect(), speed);
    },
    scrollTo(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: "smooth" });
      }
    },
  },
};
</script>

<style scoped>
.typing-text {
  display: inline;
}

.cursor {
  display: inline-block;
  color: var(--primary);
  animation: blink 1s infinite;
  font-weight: 300;
}

@keyframes blink {
  0%,
  50% {
    opacity: 1;
  }
  51%,
  100% {
    opacity: 0;
  }
}
</style>
