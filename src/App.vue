<template>
  <div class="app">
    <Navbar />
    <HeroSection />
    <BackgroundSection :skills="skills" />
    <ProjectsSection :projects="projects" />
    <ContactSection />
    <FooterSection />
  </div>
</template>

<script>
// Imports
import Navbar from "./components/Navbar.vue";
import HeroSection from "./components/HeroSection.vue";
import BackgroundSection from "./components/BackgroundSection.vue";
import ProjectsSection from "./components/ProjectsSection.vue";
import ContactSection from "./components/ContactSection.vue";
import FooterSection from "./components/FooterSection.vue";

export default {
  name: "App",

  components: {
    Navbar,
    HeroSection,
    BackgroundSection,
    ProjectsSection,
    ContactSection,
    FooterSection,
  },

  // Data that gets passed down to child components via props
  data() {
    return {
      skills: [
        "🔐 Network and Network Security",
        "💀 Metasploit",
        "🦈 Wireshark",
        "🔓 Burp Suite",
        "📡 Nmap",
        "🐧 Linux [Ubuntu, Fedora, Kali]",
        "⚽ Football",
        "🏂 Snowboarding",
        "🌐 Cisco",
        "🤝 Customer Service",
        "🤖 AI models",
        "⚡ JavaScript",
        "💚 Vue.js",
        "🟢 Node.js",
        "🚂 Express JS",
        "⚛️ React",
        "🐍 Python",
        "🚀 FastAPI",
        "🎨 HTML/CSS",
        "🪟 Windows",
        "🍎 MacOS",
        "📱 Android",
        "📲 IOS",
        "☁️ AWS [EC2, Lambda, s3, DynamoDB]",
        "💧 DigitalOcean",
        "📦 Git",
        "🗄️ SQL",
        "🕵️ Penetration Testing",
        "🐳 Docker",
        "☕ Java",
      ],
      projects: [
        {
          title: "Ethical Hacking Framework",
          description:
            "A deliberately vulnerable task management system designed for ethical hacking and penetration testing practice with intentional security flaws.",
          icon: "🔓",
          tags: ["Node.js", "React", "Security", "Kali", "PostgreSQL"],
          link: "https://github.com/shaky008/EHF",
        },
        {
          title: "MLP vs AdaBoost Classification",
          description:
            "Machine learning project comparing Neural Networks and Ensemble methods to predict student dropout and academic success.",
          icon: "🤖",
          tags: ["Python", "Machine Learning", "PCA", "Jupyter"],
          link: "https://github.com/shaky008/MLP-vs-AdaBoost-for-classification",
        },
        {
          title: "MovieHub",
          description:
            "A movie discovery app built with React and TypeScript that displays movies using TMDB API with filtering options.",
          icon: "🎬",
          tags: ["React", "TypeScript", "Vite", "API"],
          link: "https://github.com/shaky008/MovieHub",
        },
        {
          title: "Football Blog",
          description:
            "A web blog application for football content with user authentication, CRUD operations, voting system, and search functionality.",
          icon: "⚽",
          tags: ["PHP", "MySQL", "Bootstrap", "jQuery"],
          link: "https://github.com/shaky008/Football_Blog",
        },
        {
          title: "Ticket Booking System",
          description:
            "A console-based ticket booking system allowing customers to book transportation tickets with admin functions for system management.",
          icon: "🎫",
          tags: ["C++", "SQLite", "OOP", "Make"],
          link: "https://github.com/nelsonmuthiga/comp3140",
        },
        {
          title: "AI Emergency Scenario Generator",
          description:
            "AI-powered emergency management tool using Llama3 LLM to create tabletop exercise scenarios for organizations. Built for Innomergence Solutions.",
          icon: "🚨",
          tags: ["React", "FastAPI", "Firebase", "Ollama"],
          link: null,
        },
      ],
    };
  },
};
</script>
