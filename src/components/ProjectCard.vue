<template>
  <component
    :is="project.link ? 'a' : 'div'"
    :href="project.link || undefined"
    :target="project.link ? '_blank' : undefined"
    :rel="project.link ? 'noopener noreferrer' : undefined"
    class="project-card"
    :class="{ 'no-link': !project.link }"
  >
    <div class="project-icon">{{ project.icon }}</div>
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
    <div class="project-tags">
      <span class="tag" v-for="tag in project.tags" :key="tag">
        {{ tag }}
      </span>
    </div>
    <div class="project-link-hint">
      <span v-if="project.link">View on GitHub →</span>
      <span v-else class="private-badge">🔒 Private Repository</span>
    </div>
  </component>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.project-card {
  text-decoration: none;
  color: inherit;
  display: block;
  cursor: pointer;
}

.project-card.no-link {
  cursor: default;
}

.project-link-hint {
  margin-top: 1rem;
  font-size: 0.9rem;
  color: var(--primary);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-card:hover .project-link-hint {
  opacity: 1;
}

.private-badge {
  color: var(--text-muted);
}
</style>
