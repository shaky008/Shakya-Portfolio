<template>
  <section id="projects" class="projects">
    <div class="section-container">
      <h2 class="section-title">Projects</h2>
      <p class="section-subtitle">
        Here are some of the projects I've worked on
      </p>
      <div class="projects-grid">
        <ProjectCard
          v-for="project in projects"
          :key="project.title"
          :project="project"
        />
      </div>
    </div>
  </section>
</template>

<script>
import ProjectCard from "./ProjectCard.vue";

export default {
  name: "ProjectsSection",
  components: {
    ProjectCard,
  },
  props: {
    projects: {
      type: Array,
      required: true,
    },
  },
};
</script>
