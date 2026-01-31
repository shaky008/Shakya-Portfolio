<template>
  <section id="contact" class="contact">
    <div class="section-container">
      <h2 class="section-title">Let's Connect</h2>
      <p class="contact-text">
        I'm currently open to opportunities in IT, cybersecurity and software
        development. If you'd like to discuss a potential role or just want to
        chat about technology, feel free to reach out!
      </p>
      <div class="contact-links">
        <a
          href="mailto:sshakya.uutsav@gmail.com"
          @click.prevent="copyEmail"
          class="contact-btn"
        >
          <span>📧</span> {{ isEmailCopied ? "Email Copied!" : "Email Me" }}
        </a>
        <a
          href="https://www.linkedin.com/in/utsav-shakya-491b28226/"
          target="_blank"
          class="contact-btn"
        >
          <span>💼</span> LinkedIn
        </a>
        <a
          href="https://github.com/shaky008"
          target="_blank"
          class="contact-btn"
        >
          <span>🐙</span> GitHub
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactSection",
  data() {
    return {
      isEmailCopied: false,
    };
  },
  methods: {
    //copies email to clipboard
    copyEmail() {
      navigator.clipboard.writeText("sshakya.uutsav@gmail.com");
      this.isEmailCopied = true;
      setTimeout(() => {
        this.isEmailCopied = false;
      }, 5000);
    },
  },
};
</script>
