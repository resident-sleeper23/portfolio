<script setup lang="ts">
import type { NavigationMenuItem } from "@nuxt/ui";

// Edit these to match the sections on your home page.
const headerItems: NavigationMenuItem[] = [
  { label: "Projects", to: "/#projects" },
  { label: "Skills", to: "/#about" },
  { label: "Contact", to: "/#contact" },
];

// Replace the links with your own profiles.
const socialLinks = [
  {
    label: "GitHub",
    icon: "i-simple-icons-github",
    to: "https://github.com/your-username",
  },
  {
    label: "LinkedIn",
    icon: "i-simple-icons-linkedin",
    to: "https://www.linkedin.com/in/your-username",
  },
];
</script>

<template>
  <div>
    <UHeader>
      <template #title>
        <NuxtLink to="/">Your Name</NuxtLink>
      </template>

      <UNavigationMenu :items="headerItems" />

      <template #right>
        <UColorModeButton />

        <UButton
          v-for="link in socialLinks"
          :key="link.label"
          :icon="link.icon"
          :to="link.to"
          :aria-label="link.label"
          class="hidden sm:inline-flex"
          color="neutral"
          target="_blank"
          variant="ghost"
        />
      </template>

      <template #body>
        <UNavigationMenu
          :items="headerItems"
          class="-mx-2.5"
          orientation="vertical"
        />
      </template>
    </UHeader>

    <UMain>
      <slot />
    </UMain>

    <UFooter>
      <template #left>
        <p class="text-muted text-sm">
          Copyright © {{ new Date().getFullYear() }} Your Name
        </p>
      </template>

      <template #right>
        <UButton
          v-for="link in socialLinks"
          :key="link.label"
          :icon="link.icon"
          :to="link.to"
          :aria-label="link.label"
          color="neutral"
          target="_blank"
          variant="ghost"
        />
      </template>
    </UFooter>
  </div>
</template>