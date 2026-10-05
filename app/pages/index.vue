<script setup lang="ts">
useSeoMeta({
  title: "Home",
  description: "Portfolio of Your Name, a web developer.",
});

// Edit the text below to make it yours.
const name = "Your Name";
const tagline = "Web developer";
const intro =
  "I build simple, useful things for the web. Replace this with a sentence or two about who you are and what you like to work on.";

const heroLinks = ref([
  {
    label: "See my projects",
    to: "#projects",
    icon: "i-lucide-folder-open",
  },
  {
    label: "Contact me",
    to: "#contact",
    variant: "subtle" as const,
    trailingIcon: "i-lucide-arrow-right",
  },
]);

// Add, remove, or reorder projects here. Each one becomes a card.
const projects = ref([
  {
    title: "Project One",
    description: "What it does and what you built. Tech: Vue, Nuxt, Tailwind.",
    icon: "i-lucide-code",
    to: "https://github.com/your-username/project-one",
    target: "_blank",
  },
  {
    title: "Project Two",
    description: "Another thing you made. Tech: JavaScript, HTML, CSS.",
    icon: "i-lucide-palette",
    to: "https://github.com/your-username/project-two",
    target: "_blank",
  },
  {
    title: "Project Three",
    description: "A third project, or delete this one.",
    icon: "i-lucide-rocket",
    to: "https://github.com/your-username/project-three",
    target: "_blank",
  },
]);

const skills = ["HTML", "CSS", "JavaScript", "Vue", "Nuxt", "Tailwind CSS"];

const contactLinks = ref([
  {
    label: "Email",
    to: "mailto:you@example.com",
    icon: "i-lucide-mail",
  },
  {
    label: "GitHub",
    to: "https://github.com/your-username",
    target: "_blank",
    icon: "i-simple-icons-github",
    variant: "subtle" as const,
  },
  {
    label: "LinkedIn",
    to: "https://www.linkedin.com/in/your-username",
    target: "_blank",
    icon: "i-simple-icons-linkedin",
    variant: "subtle" as const,
  },
]);
</script>

<template>
  <div>
    <UPageHero
      :title="`Hi, I'm ${name}`"
      :description="intro"
      :headline="tagline"
      :links="heroLinks"
    />

    <UContainer id="projects" class="my-16">
      <h2 class="mb-6 text-2xl font-semibold">Projects</h2>
      <UPageGrid>
        <UPageCard
          v-for="project in projects"
          :key="project.title"
          v-bind="project"
        />
      </UPageGrid>
    </UContainer>

    <UContainer id="about" class="my-16">
      <h2 class="mb-6 text-2xl font-semibold">Skills</h2>
      <div class="flex flex-wrap gap-2">
        <UBadge
          v-for="skill in skills"
          :key="skill"
          :label="skill"
          size="lg"
          variant="subtle"
        />
      </div>
    </UContainer>

    <UContainer id="contact" class="my-16 pb-16">
      <h2 class="mb-6 text-2xl font-semibold">Contact</h2>
      <div class="flex flex-wrap gap-3">
        <UButton v-for="link in contactLinks" :key="link.label" v-bind="link" />
      </div>
    </UContainer>
  </div>
</template>