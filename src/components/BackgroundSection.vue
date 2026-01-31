<template>
  <section id="background" class="background">
    <div class="section-container">
      <h2 class="section-title">Background</h2>
      <div class="background-content">
        <div class="about-card">
          <div class="about-icon">🙋‍♂️</div>
          <h3>About Me</h3>
          <p>
            I am a HUGE <strong>Football</strong> fan
            (<strong>LIVERPOOL!</strong>). I have a beautiful Japanese spitz;
            <strong>Zuko</strong>. I recently got into snowboarding and have
            been practicing a lot.
          </p>
        </div>
        <div class="about-card">
          <div class="about-icon">🎯</div>
          <h3>Career Goals</h3>
          <p>
            My primary goal is to establish a career in
            <strong>cybersecurity</strong>, protecting systems and data from
            emerging threats. I'm fascinated by ethical hacking, penetration
            testing, and security analysis.
          </p>
        </div>
        <div class="about-card">
          <div class="about-icon">💻</div>
          <h3>Technical Skills</h3>
          <p>
            While pursuing my cybersecurity aspirations, I've developed solid
            skills in
            <strong>software development</strong>. I enjoy building web
            applications, learning new technologies, and solving complex
            problems through code.
          </p>
        </div>
        <div class="about-card">
          <div class="about-icon">🚀</div>
          <h3>What I Bring</h3>
          <p>
            I'm a quick learner with a strong work ethic. Whether it's writing
            secure code, analyzing vulnerabilities, or developing applications,
            I bring dedication and enthusiasm to every project. But most
            importantly, I am easy to talk to.
          </p>
        </div>
      </div>
      <div class="skills-section">
        <h3>Technologies & Skills</h3>
        <div class="skills-grid">
          <span class="skill-tag" v-for="skill in skills" :key="skill">
            {{ skill }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BackgroundSection",
  props: {
    skills: {
      type: Array,
      required: true,
    },
  },
};
</script>
